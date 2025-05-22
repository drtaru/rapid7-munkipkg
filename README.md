# rapid7-munkipkg
Munkipkg example files to allow easy creation of single rapid7 pkg style installers for MacOS

## THIS PROJECT REQUIRES MUNKIPKG
Munkipkg can be obtained Here: https://github.com/munki/munki-pkg/tree/main

### UPDATE!
**UNTESTED, Updated per a request on the MacAdmins Slack, Please test before deployment**
Rapid7 has switched to supplying a pkg installer but it still requires a postinstall script to activate.  
Therefore it still makes sense to package everything together and run the respective installer and postinstall per architecture.
If you only have one architecture ion your fleet you can omit the pkg for the unused arch, Ex: Intel.

## Instructions:

* Modify `installRapid7/scripts/postinstall` and update pkgVersion="4.0.17.21" with the version from the package name you downloaded. Also update installToken="PASTETOKENHEREKEEPQUOTES" with your install token from the Rapid7 Agent download page. _EX: us:xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx_
* Replace both blank placeholders of `rapid7-insight-agent-xxx.pkg` in `installRapid7/private/tmp/rapid7`with copies downloaded from the Rapid7 Agent download page.
* Drop the entire `installRapid7` folder into the directory containing `munkipkg`
* Open a Terminal and navigate to the directory containing `munkipkg`
* Run the following command: `./munkipkg installRapid7`

**TEST**