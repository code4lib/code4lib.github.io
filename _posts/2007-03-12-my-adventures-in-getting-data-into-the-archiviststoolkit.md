---
excerpt: "<h3><a name=\"My_Adventures_in_Getting_Data_into_the_ArchivistsToolkit\"></a>My
  Adventures in Getting Data into the ArchivistsToolkit</h3>\r\n\r\n<p>Georgia Tech
  Archives is moving its accessions database from a home grown sql/php based archival
  database tool to the <a href=\"http://archiviststoolkit.org/\">Archivist's Toolkit</a>
  which was recently released. The easiest route I thought was to export the current
  data to two spreadsheets in csv format, clean it up, and import the results. It
  couldn't be that hard: just convert csv to Toolkit format. </p> \r\n\r\n<h4><a name=\"Get_The_Data_From_The_Old_Tool\"></a>Get
  The Data From The Old Tool</h4>\r\n\r\n<p>That was as easy as pushing the right
  buttons on phpmyadmn. We ended up with two tables; one described the donors, the
  other the accessions linked to donors by via donor ids.</p>"
categories: []
layout: page
title: My Adventures in Getting Data into the ArchivistsToolkit
created: 1173704410
---
<h3><a name="My_Adventures_in_Getting_Data_into_the_ArchivistsToolkit"></a>My Adventures in Getting Data into the ArchivistsToolkit</h3>

<p>Georgia Tech Archives is moving its accessions database from a home grown sql/php based archival database tool to the <a href="http://archiviststoolkit.org/">Archivist's Toolkit</a> which was recently released. The easiest route I thought was to export the current data to two spreadsheets in csv format, clean it up, and import the results. It couldn't be that hard: just convert csv to Toolkit format. </p> 

<h4><a name="Get_The_Data_From_The_Old_Tool"></a>Get The Data From The Old Tool</h4>

<p>That was as easy as pushing the right buttons on phpmyadmn. We ended up with two tables; one described the donors, the other the accessions linked to donors by via donor ids.</p> 
<h4><a name="Data_Cleanup"></a>Data Cleanup </h4>

<p> From the outset we planned to clean up data.  Initially we thought we had to purge double donor records but it turned that step wasn't actually necessary, so I skip the details here.  The cleanup incolved making accession numbers more regular, correcting typos that came to our attention when we saw all accessions/names in one big table, ... </p>

<h4><a name="Get_The_Archivists_Toolkit_up_and_running"></a>Get The Archivists Toolkit up and running</h4>

<p> Downloading and installing the Toolkit client on the Windows machines was a breeze. The same was unfortunately not true for my Ubuntu machine. First the installer refused to even do its magic dying with mysteries messages about not finding system libraries. The installer including the jre had the same problem. Luckily Jason Fowler posted his solution on the Toolkit's mailing list, see his <a href="http://neoarch.wordpress.com/2007/01/28/hint-on-configuring-the-archivists-toolkit-on-linux/">blog entry</a>.</p>

<p> The only thing I can add here: &ldquo;vi -b&rdquo; provides nice binary edit as well, or do <br/> <tt> cat [FileName] | sed "s/export LD_ASSUME_KERNEL/#xport LD_ASSUME_KERNEL/ </tt> </p>

<h4>The Simple Plan </h4>

<ol style="margin-left: .75cm; list-style-type: decimal;">

  <li >
    
    <p> Redefine column names in the csv files to match the names used in the Toolkit. </p> 
  </li>
  <li>
    
    <p>Write a Perl script to generate a Toolkit import file using the data from the csv files.  </p> 
 </li>


  <li>
    
    <p>Let the Toolkit read it. </p>

  </li>

</ol>

<p> It did not turn out to be that easy.</p>

<p> The Toolkit offers to import accessions and names data from a flat csv style file. It insists on tab delimination, which I found rather unreadable when I needed to check whether my script did generate the correct information.  </p> 

<p> In addition and more importantly, since this is a flat csv file in which each property can only head up one column it is not possible to link an accession to more than one donor/name.  Accessions and names in the Toolkit data model have a many-to-many relationship, a name can be linked to several donors and an accession can have multiple names linked to it.  Thus the import format is far less expressive than the actual data model supported. It also doesn't match well with the data institutions will want to import.  </p>

<p> In our not untypical case we have many donors that represent a person and a corporation, which need to be represented as two distinct name records in the Toolkit. Both records need to be linked to the accession that they donated. Given the Toolkit's import format this is not possible.  We had to devise a work around.  </p> 


<h4>The Plan that worked </h4>
<p> Here follows,  without mentioning the false starts, how we did get our accessions data into the Toolkit: </p> 
<ol style="margin-left: 0.75cm; list-style-type: decimal;">

  <li >
    
    <p> I wrote a script that read an accessions csv file and generated a Toolkit import file selecting only those values from the csv file that are of interest to the Toolkit. This was straight forward.  We could have imported a csv file straight into the SQL database, but I was vary of importing 'bad' data, like dates in the future, accession numbers that don't live up to Toolkit standards, ... I wanted to leave the consistency checking to the Toolkit. </p>

  </li>

  <li >
    
    <p> Our archivist manually cleaned the donor information up. We ended up with a table that contained a name record for each person and each corporate donor. Where we previously had one record with a dual purpose we now had a name record for the corporation as well as the person. The archivist had to decide whether phone number, contact address information, and so forth applied to the person, the corporation, or both. There was no way around employing some human intelligence.</p> 
  </li>

  <li >
    
    <p> I added an option to my script to convert the donor name data into a Toolkit import file.  The donors could not be imported by themselves, so I generated fake accessions with numbers '9999.000.1', '9999.000.2', ... . One accession for each name. After importing this file and deleting the 'fake' accessions  all information about accessions and donors was in the Toolkit's database except for the way they are linked to each other.  </p>

  </li>

  <li >
    
    <p> With some more spreadsheet magic our archivist generated a Links table, which contained accession ids and name information. He basically had to replace donor ids in the accessions table with the full donor/name information. </p>

  </li>

  <li >
    
    <p> I added another option to the script that read the Links table from its csv file. For each link it </p> 
  </li>

<ul >

  <li >
    
    <p> checked whether the name information in the csv links table corresponded to a name in the csv names table (just to make sure the input data in the csv files was actually consistent)</p>

  </li>

  <li >
    
    <p> looked for an accession with the given id in the Toolkit database</p> 
  </li>

  <li >
    
    <p> searched for the name from the Links table in the Toolkit database </p> 
  </li>

  <li >
    
    <p> if everything went well it generated an SQL statement that would link the Toolkit's accession with the given name </p> 
  </li>
  </ul>

  <li >
    
    <p> Last we imported the generated sql file into the Toolkits database. </p> 
  </li>

</ol>


<h4 >The False Start</h4>

<p>In a first round I generated the donor and corporate name records by simply using name information like contact address, fax, email for both name records. I got to the point where the Toolkit informed me that all name records were imported successfully. In the next step of importing links my script complained about not finding many of the name records that were imported before.  It turned out that the Toolkit had quietly assumed that corporate record: </p>

    <p style="margin-left: 0.75cm;"> Georgia Tech , 404-898-0819</p>

<p>and&nbsp;</p>
    <p style="margin-left: 0.75cm;"> Georgia Tech , 786-234-1937</p>


<p>were the same. This is not an unreasonable assumption, but I would have liked to see a warning about the fact that the second record was not imported as a new corporate name. I was certainly glad my script had done some consistency checking.  </p> 

<h4>Looking back</h4>
<p> Obviously we had to decide how to match up properties from our legacy database with the ones in the Toolkit, which turned out to be easy because the Toolkit offers a complete list of choices.  </p> 
<p> 
Our legacy database's definition of a donor does not match perfectly with the Toolkit's definition of a name. So there was some unavoidable work and data massaging necessary here. 
</p> 
<p> The biggest complication we encountered was the fact that accessions are imported through only one table. Therefore accessions and donors can be imported only in pairs.  The Toolkit is smart enough to generate only one name where relevant name properties match across several accession import lines.  Thus it supports a many accessions to one donor type relationship but does not help in our case where we needed to import accessions that were linked to multiple donors. Having to work around this resctriction was the biggest obstacle to importing our data.  </p> 
<p> Now that I have this script in place we will also be able to add creator links to aceessions once we have that data cleaned up and arrannged in a suitable way.  </p>

 
<h4>One last remark &nbsp;</h4>

<p>The Toolkit provides an 'initialize-toolkit-database' script. I got tired of calling that program up (yes there are some pretty pictures), so I exported the data base right after setting it up. When I needed a fresh empty database I simply imported that file back in. </p>

<p style="font-weight: bold;">Attached</p>

<p> The script and its documentation can be browsed and downloaded from my website: <a href="http://www.mcmprogramming.com/toolkit/csvToTk">Browse</a>,  <a href="http://www.mcmprogramming.com/toolkit/csvToTk.tar">Download tar file</a>.  </p>

