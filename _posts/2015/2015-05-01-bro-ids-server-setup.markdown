---
layout: post
title: "How To - Bro IDS Server Setup"
date: '2015-05-01 1:30'
tags: bro ids security
---

## What is Bro used for?

The Bro network monitoring platform has one of the dumbest names, but most powerful set of plugin capabilities.


## Who uses Bro?

I mean it cant really be used with a name like 'Bro,' right?
- CERN
- Major Universities

### Installation Guide

##### 1. To install the required dependencies, you can use:

- RPM/RedHat-based Linux

  - `sudo yum install cmake make gcc gcc-c++ flex bison libpcap-devel openssl-devel python-devel swig zlib-devel`

- DEB/Debian-based Linux

  - `sudo apt-get install cmake make gcc g++ flex bison libpcap-dev libssl-dev python-dev swig zlib1g-dev`

##### 2. Optional Dependencies

- Bro can make use of some optional libraries and tools if they are found at build time:

  - C++ Actor Framework (CAF) version 0.14 (<http://actor-framework.org>)
  - LibGeoIP (for geolocating IP addresses)
  - sendmail (enables Bro and BroControl to send mail)
  - curl (used by a Bro script that implements active HTTP)
  - gperftools (tcmalloc is used to improve memory and CPU usage)
  - jemalloc (<http://www.canonware.com/jemalloc/>)
  - PF_RING (Linux only, see Cluster Configuration)
  - ipsumdump (for trace-summary; <http://www.cs.ucla.edu/~kohler/ipsumdump>)

##### 3. Installing Bro



##### 4. Post Install

- Configuring the runtime env
  - `export PATH=/usr/local/bro/bin:$PATH`
