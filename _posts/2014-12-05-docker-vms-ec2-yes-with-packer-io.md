---
categories: []
layout: page
title: Docker? VMs? EC2? Yes! With Packer.io
created: 1417819312
---
- Kevin S. Clarke, ksclarke@gmail.com, Digital Library Programmer,
UCLA

There are a lot of exciting ways to deploy a software stack nowadays.
Many of our library systems are fully virtualized. Docker is a
compelling alternative, and there are also cloud options like Amazon's
EC2. This talk will introduce Packer.io, a tool for creating identical
machine images for multiple platforms (e.g., Docker, VMWare, VirtualBox,
EC2, GCE, OpenStack, et al.) all from a single source configuration. It
works well with Ansible, Chef, Puppet, Salt, and plain old Bash scripts.
And, it's designed to be scriptable so that builds can be automated.
This presentation will show how easy it is to use Packer.io to bring up
a set of related services like Fedora 4, Grinder (for stress testing),
and Graphite (for charting metrics). As an added value, all the
buzzwords in this proposal will be defined and explained!
