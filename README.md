[![Build Status](https://travis-ci.org/savchyn/dmrconfig.git?branch=master)](https://travis-ci.org/savchyn/dmrconfig) 
[![codecov](https://codecov.io/gh/savchyn/atmos/dmrconfig/master/graph/badge.svg)](https://codecov.io/gh/savchyn/dmrconfig)

{<img src="https://travis-ci.org/savchyn/dmrconfig.svg?branch=master" alt="Build Status" />}[https://travis-ci.org/savchyn/dmrconfig]


DMRconfig is a utility for programming digital radios via USB programming cable.
Supported radios:

 * TYT MD-380 (not tested)
 * TYT MD-2017 (not tested)
 * TYT MD-UV380


## Usage

Read codeplug from the radio and save it to file 'device.img',
and also save text configuration to 'device.conf':

    dmrconfig -r [-t]

Write codeplug to the radio:

    dmrconfig -w [-t] file.img

Configure the radio from text file.
Previous codeplug is saved to 'backup.img':

    dmrconfig -c [-t] file.conf

Show configuration from the codeplug file:

    dmrconfig file.img

Apply configuration from text file to the codeplug file:

    dmrconfig -c file.img file.conf

Option -t enables tracing of USB protocol.


## Sources

Sources are distributed freely under the terms of Apache 2.0 license.
You can download sources via GIT:

    git clone https://github.com/sergev/dmrconfig


To build on Linux or Mac OS X, run:

    make
    make install


Regards,
Serge Vakulenko
KK6ABQ
