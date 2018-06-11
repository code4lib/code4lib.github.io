---
categories: []
layout: page
title: ruby-marc 0.5.0 released
created: 1336416659
---
v0.5.0 

- Extensive rewrite of MARC::Reader (ISO 2709 binary reader) to 
  provide a fairly complete and consistent handing of char encoding
  issues in ruby 1.9. 

  - This code is well covered by automated tests, but ends up complex, 
    there may be bugs, please report them. 

  - May not work properly under jruby with non-unicode source 
    encodings. 

  - Still can't handle Marc8 encoding. 

  - May not have entirely backwards compatible behavior with regard to 
    char encodings under ruby 1.9.x as previous 0.4.x versions. Test 
    your code. In particular, previous versions may have automatically 
    _transcoded_ non-unicode encodings to UTF-8 for you. This version 
    will not do so unless you ask it to with correct arguments. 


`gem install ruby-marc -v 0.5.0 `

https://github.com/ruby-marc/ruby-marc
