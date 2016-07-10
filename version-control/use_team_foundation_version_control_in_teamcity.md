# Use Team Foundation Server in TeamCity
TeamCity supports integration with TFS Version Control (TFVC) in java and .net modes as follows:

| Mode | TFS | Platforms | Libraries
| -- | -- | -- | --
| Java | 2010+ | Linux, Mac OS X, and Windows | Bundled
| .Net | 2005+ | Windows | Need to install

*Java mode* based on Team Explorer Everywhere bits and works out the box.

*.Net mode* based on libraries shipped with Team Explorer and Visual Studio.

More information about TFS and Team Explorer compatibility can be found in the [TFS compatibility page](https://www.visualstudio.com/en-us/docs/setup-admin/requirements).

By default TeamCity tries to use .Net mode and if it not available falls back to Java mode. If you want to force TeamCity to use specific mode just define [internal property](https://confluence.jetbrains.com/display/TCDL/Configuring+TeamCity+Server+Startup+Properties) or [build configuration parameter](https://confluence.jetbrains.com/display/TCDL/Defining+and+Using+Build+Parameters+in+Build+Configuration) `teamcity.tfs.mode` with a value `java` or `.net`.

## Create a new TeamCity project from TFVC repository

All that you need to do it is copy link to the TFS project and open in TeamCity administration page `Create New Project from URL`, fill in project URL, username/password fields and click `Proceed`. Then you need to configure build steps and add a build trigger.

## TeamCity authentication in TFS
TeamCity supports following authentication options in TFs:
* Username/password pair
* Windows user identity via NTLM/Kerberos, leave black username/password fields

> Note: you should properly configure Kerberos libraries in your Linux distribution by following [Team Explorer Everywhere guideline](https://msdn.microsoft.com/en-us/library/gg475929(v=vs.120).aspx#Anchor_3).

## Store TeamCity project configuration settings in TFS
TeamCity provides great ability to store project configuration files in VCS. Learn more about [how it works](https://confluence.jetbrains.com/display/TCDL/Storing+Project+Settings+in+Version+Control).