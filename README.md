mod_bcg729
==========

FreeSWITCH G.729A module using the opensource bcg729 implementation by Belledonne Communications.

Simple G.729A codec for FreeSWITCH using the Belledonne Communications G.729A GPLv2 implementation.
Please see http://www.linphone.org/eng/documentation/dev/bcg729.html for further informations.

The module is a modified version of fsg729 ( https://code.google.com/p/fsg729/ ) which
uses the Intel IPP libraries, updated to use a different codec implementation and get rid of Intel stuff.

As of Jan 1 2017, G.729 is a royalty free codec: http://www.sipro.com/G729.html

You can get a faster and supported G.729A codec by purchasing licenses
directly from FreeSWITCH guys http://www.freeswitch.org .
This will have the side effect to support the FreeSWITCH project ;)

Installation
============
```
cd /usr/src
wget https://github.com/tridcatij/mod_bcg729/archive/master.zip
unzip master.zip

cd mod_bcg729-master

make
make install
```

Open file
```
nano /usr/local/freeswitch/conf/autoload_configs/modules.conf.xml
```
and make following changes
```
<!--<load module="mod_g729"/>-->
<load module="mod_bcg729"/>
```

Add codec to the vars.xml and restart FS.

If you're using ASTPP, just add G729 in the current SIP profile.
