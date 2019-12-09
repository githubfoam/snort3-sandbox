# snort3-sandbox
ubuntu1904
~~~~
test if Hyperscan works, from the build directory

cd ~/snort_src/hyperscan-5.2.0-build/
./bin/unit-hyperscan

vagrant@vg-snort-01:~$ /usr/local/bin/snort -V

   ,,_     -*> Snort++ <*-
  o"  )~   Version 3.0.0 (Build 266)
   ''''    By Martin Roesch & The Snort Team
           http://snort.org/contact#team
           Copyright (C) 2014-2019 Cisco and/or its affiliates. All rights reserved.
           Copyright (C) 1998-2013 Sourcefire, Inc., et al.
           Using DAQ version 3.0.0
           Using LuaJIT version 2.1.0-beta3
           Using OpenSSL 1.1.1b  26 Feb 2019
           Using libpcap version 1.8.1
           Using PCRE version 8.43 2019-02-23
           Using ZLIB version 1.2.11
           Using FlatBuffers 1.11.0
           Using Hyperscan version 5.2.0 2019-12-08
           Using LZMA version 5.2.4

Snort 3 on Ubuntu 18 & 19
<https://www.snort.org/documents>
BUILD SNORT
<https://github.com/snort3/snort3>
~~~~
CentOS80
~~~~

shell: ./configure_cmake.sh --prefix=/usr/local/snort >> /tmp/snort3_configure.out

[ 98%] Documents: building commands.txt with
[ 98%] Documents: building counts.txt with
/tmp/snort3/snort3/build/src/snort: error while loading shared libraries: libdaq.so.3: cannot open shared object file: No such file or directory
make[2]: *** [doc/CMakeFiles/all_built_sources.dir/build.make:80: doc/commands.txt] Error 127
make[2]: *** Deleting file 'doc/commands.txt'
make[2]: *** Waiting for unfinished jobs....
/tmp/snort3/snort3/build/src/snort: error while loading shared libraries: libdaq.so.3: cannot open shared object file: No such file or directory
make[1]: *** [CMakeFiles/Makefile2:6183: doc/CMakeFiles/all_built_sources.dir/all] Error 2
make: *** [Makefile:152: all] Error 2

shell: ./configure_cmake.sh --prefix=/usr/local/snort --enable-tcmalloc  >> /tmp/snort3_configure.out

[ 98%] Documents: building commands.txt with
/tmp/snort3/snort3/build/src/snort: error while loading shared libraries: libtcmalloc.so.4: cannot open shared object file: No such file or directory
/tmp/snort3/snort3/build/src/snort: error while loading shared libraries: libtcmalloc.so.4: cannot open shared object file: No such file or directory
make[2]: *** [doc/CMakeFiles/all_built_sources.dir/build.make:80: doc/commands.txt] Error 127
make[2]: *** Deleting file 'doc/commands.txt'
make[2]: *** Waiting for unfinished jobs....
make[1]: *** [CMakeFiles/Makefile2:6183: doc/CMakeFiles/all_built_sources.dir/all] Error 2
make: *** [Makefile:152: all] Error 2




Installing newer versions (>=7.x) of Ragel requires installing colm first. Prior versions, for example version 6.10, do not require installing colm. The steps will proceed with installing colm (0.13.0.7 ) and ragel (7.0.0.12).

There are two methods to make hyperscan aware of the Boost headers:
1) Symlink, or
2) PassingBOOST_ROOTpointing to the root directory of the Boost headers to cmake.

Snort 3 on CentOS8
<https://www.snort.org/documents>
BUILD SNORT
<https://github.com/snort3/snort3>
~~~~
