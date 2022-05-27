
Subversion - Overview
=====================

# Overview



### Overview




 


Subversion software offers a versioning and a revision control system distributed under a free 
license. It is used to maintain current and historical versions of files such as source code, web pages, and 
documentation.


This plug-in includes one step which has no input properties:


* [Import Version](#import_version)



### Compatibility


The subversion client must be installed on the server. All subversion configurations are supported.
 



### Step palette


To access this plug-in in the palette, click **Source and Repositories** > **Subversion**.


###
 Installation


This plug-in is installed when installing IBM UrbanCode Deploy. When new plug-in versions are available,
 follow the [installation instructions](https://www.urbancode.com/resource/installing-plug-ins-in-urbancode-products/ 
"Installing plug-ins in UrbanCode Deploy") to update the plug-in.


### History


#### Version 18


* Fixing APAR 
PH20603:AUTOMATED COMPONENT VERSION IMPORTS ARE FAILING FROM SUB VERSION SOURCE CONFIG PLUGIN DUE TO IMPORTING ALREADY 
ARCHIVED VERSION.


#### Version 17


* Fixing CVE:CVE-2019-4233


#### Version 16


* Updates to property descriptions.



#### Version 15


* APAR PI89045: add support for setting isFinished flag flag when importing versions.


#### 
Version 14


* Fixes APAR PI87707, a regression where the user who requested a manual version import was not being 
tracked.


#### Version 13


* Fixes APAR PI79140. Successfully import new versions when run in a non-English language.



#### Version 12


* Fixes APAR PI40551. Now uses working directory for temporary artifact storage.


#### Version 11



* Fixes APAR PI28680. Added check to see if tag exists in repository before creating version.


#### Version 10


* 
Support property file encryption.


#### Version 9


* Fixes APAR PI57417. Plug-in now checks the agent settings for 
acceptance of self signed certificates.


#### Version 8


* PI58856 Version import can fail if versions exist and 
repository url is changed in the source configuration.


#### Version 7


* Fix for APAR PI55824 Subversion source 
config import failed after upgrading to UCD 6.2.0.2.
* Added checks for null proxy server property values.


#### 
Version 6


* Adds support for configuring a proxy server for version imports.


#### Version 5


* Adding debugging 
information to version import logs.


#### Version 4


* Fixes APAR PI47863. Clean up temp files correctly after import.



#### Version 3


* Including fix for PI42041 running out of disk space can cause subversion source configuration to 
create incomplete versions.


#### Version 2


* Fixes running a process after creating a version.


#### Version 1


* 
Initial release of Subversion source configuration plugin.


|Back to ...||Latest Version|Subversion ||||
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Deploy Plugins](../README.md)|[21.1131553]()|[Readme](README.md)|[Usage](usage.md)|[Steps](steps.md)|[Downloads](downloads.md)|