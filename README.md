bcfg2-boilerplate
=================

A basic configuration for bcfg2 server node intended to give a flying start to understanding the config management system.

One-liner attempt:
------------------

BCFG2 requires clients to be listed in Metadata/clients.xml and added to 
groups in Metadata/groups.xml, where these groups will be assigned bundles
found in Bundler/{bundlename}.xml, where these bundles contain Paths to files,
Packages defined in Pkgmgr/{packagename}.xml and Services found in Rules/*.xml.



References
=================

In the order to view them:

http://trac.mcs.anl.gov/projects/bcfg2/wiki/AudioVideo#a2009-11-05-UsenixLISA2009Bcfg2BoF-Video1h00m58s
http://videobin.org/+lk/pc.ogg
http://docs.bcfg2.org/getting_started/index.html
http://trac.mcs.anl.gov/projects/bcfg2/wiki/ServerSideOverview
http://docs.bcfg2.org/contents.html

Issues
=================

Svcmgr ain't workin
-------------------

Basically, I was struggling getting Service tag to work in my Bundle because
I was failing to get the Svcmgr generator plugin to work. Then when I did,
I realised I was still getting errors because I hadn't actually started the 
services in the first place!

Ultimately, should use Rules plugin to define Services.

http://thread.gmane.org/gmane.comp.sysutils.bcfg2.devel/1746
