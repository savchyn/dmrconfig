<img src="https://travis-ci.org/savchyn/dmrconfig.svg?branch=master" alt="Build Status" />

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/8598d8b5b4674f348483b6ba57fa4f56)](https://app.codacy.com/app/savchyn/dmrconfig?utm_source=github.com&utm_medium=referral&utm_content=savchyn/dmrconfig&utm_campaign=Badge_Grade_Dashboard)
[![codecov](https://codecov.io/gh/savchyn/dmrconfig/master/graph/badge.svg)](https://codecov.io/gh/savchyn/dmrconfig)
DMRconfig is a utility for programming digital radios via USB programming cable.
Supported radios:

 * TYT MD-380, Retevis RT3, RT8
 * TYT MD-2017, Retevis RT82 (untested)
 * TYT MD-UV380
 * TYT MD-UV390, Retevis RT3S (untested)
 * TYT MD-9600 (untested)
 * Zastone D900 (untested)
 * Zastone DP880 (untested)
 * Radtel RT-27D (untested)

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

Update database of contacts from CSV file:

    dmrconfig -u [-t] file.csv

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
