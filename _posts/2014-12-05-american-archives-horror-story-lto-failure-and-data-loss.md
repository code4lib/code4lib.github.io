---
categories:
- code4lib 2015
layout: post
title: 'American (Archives) Horror Story: LTO Failure and Data Loss'
created: 1417819240
permalink: /conference/2015/fraimow/
---
- Rebecca Fraimow, rebecca\_fraimow@wgbh.org, NDSR Resident, WGBH
- Casey Davis, casey\_davis@wgbh.org, Project Manager, American
Archive of Public Broadcasting, WGBH

Here’s a story to send shivers down archival spines: when transferring
video files off LTO for the American Archive project, WGBH got an
initial failure rate of 57%. After repeat tries, the rates improved;
still, an unnervingly large percentage of files were never able to be
transferred successfully. Even more unnerving, going public with our
horror story got a big response from other archives using LTO -- it
seems like many institutions are having similarly scary results. What
are the real risks with LTO tape? Are there steps that archives should
be taking to better circumvent those risks? This presentation will share
information about LTO storage failures across archives world and discuss
the process of investigating the problem at WGBH by testing different
methods of data retrieval from LTO (direct and networked downloads,
individual file retrieval and bulk data dump, use of LTO 4 and LTO 6
decks) and using checksum comparisons and file analysis and
characterization tools such as ffprobe, mediainfo and exiftool to
analyze failed files. We'll also present whatever results we’ve managed
to turn up by the time of Code4Lib!
