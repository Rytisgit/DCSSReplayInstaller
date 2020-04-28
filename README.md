# DCSSReplayInstaller

## to generate your own installer 

### Prerequisites (from https://github.com/iswix-llc/iswix-tutorials)

* Microsoft Visual Studio
   * 2010 or higher. (2015 or 2017 highly reccomended.)
   * [Community Edition](https://www.visualstudio.com/vs/community/) or higher. 
   * Express Edition will not work.
* Windows Installer XML [3.11](http://wixtoolset.org/releases/)  or higher. 
   * Although IsWiX has project templates for WiX v4, WiX v4 is an alpha status experimental rewrite of WiX and will not work.
* WiX Toolset Visual Studio Extension
   * Install one [extension](http://wixtoolset.org/releases/) for each version of Visual Studio you wish to use. 
* IsWiX [4.11](https://github.com/iswix-llc/iswix/releases) or higher.
   * Will automatically target all of your Visual Studio installations without the need forseperate extension downloads.

#### update DCSSReplayInstallerMM.wxs line 5

` <?define SourceDir="C:\source\ttyrecPlayer\ttyrecTiles"?>
`

#### to your DCSSReplay source folder

### You also need to have built the main project with release configuration at least once

### If you Added/Removed any files from Extra folder, or created/deleted any projects you will need to update DCSSReplayInstallerMM.wxs by going to visual studio Tools/Launch IsWix Opening the DCSSReplayInstallerMM.wxs file in the configurator and updating the files in Files and Folders tab. 

### Finally bump up the version and Rebuild the DCSSReplayInstaller Solution as Release and the installer should appear in the bin folder.
