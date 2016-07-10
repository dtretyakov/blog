# TeamCity Version Control
TeamCity supports following version control systems and features:

| Name | Agent Checkout| Branches | Versioned Settings
| -- | -- | -- | --
| AccuRev | - | - | -
| ClearCase | + | + | -
| CVS | - | + | -
| Git | + | + | +
| Mercurial | + | + | +
| Perforce | + | + | +
| StarTeam | - | - | -
| Subversion | + | - | +
| SourceGear Vault | - | - | -
| TFS | + | - | +
| Visual SourceSafe | - | - | -

*Agent Checkout* allows to receive source code from the repository directly on the TeamCity build agent.

*Versioned Settings* provides ability to store TeamCity project configuration files in the VCS.

## Create Version Control Plugin
If you want to know how to build TeamCity VCS plugin please read the [following page](https://confluence.jetbrains.com/display/TCDL/Version+Control+System+Plugin).