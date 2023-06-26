# rapid7-munkipkg
Munkipkg example files to allow easy creation of rapid7 pkg style installers for MacOS

#### THIS PROJECT REQUIRES MUNKIPKG
Munkipkg can be obtained Here: https://github.com/munki/munki-pkg/tree/main


* Modify `installRapid7/scripts/postinstall` and replace both instances of `%PASTETOKENHERE%` with your install token from the Rapid7 Agent download page. _EX: us:xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx_
* Replace both blank placeholders of `agent_installer-xxx.sh` in `installRapid7/private/tmp/rapid7`with copies downloaded from the Rapid7 Agent download page.
* Drop the entire `installRapid7` folder into the directory containing `munkipkg`
* Open a Terminal and navigate to the directory containing `munkipkg`
* Run the following command: `./munkipkg installRapid7`
