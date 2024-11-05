# Software Installer
There is a lot of information about the software installer. The source of the installation steps can be downloaded in the sources below.
## Functionality
With my current research I could find a lot of different things that could be changed.
Such as:
- Installing new maps using map on demand
- Connect with G-book software to install bought items (outdated since 2022)
- Further installation of software such as Karaoke songs, films, songs and games.

// This page is a very big todo still since I need to manually translate and set everything.


## Installation
The installation process is quite hard, compared to normal .exe installations.

The way I managed it:
Install a virtual machine with windowsXP installed. (also install a japanese language pack to safe you some headaches later on).

Go to the Internet Archive and install the GBook Software Installer. (link in sources)

When installing you will encounter one main error with an isscript.msi file. With the link off installengine.com. This is an installation breaking error and took me some time to find the solution.
For the solution I found [this reddit post](https://www.reddit.com/r/techsupport/comments/c6pull/comment/hi7zk0a/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button).
The isscript.msi file that needs to be installed can be found [here](https://web.archive.org/web/20050218191725/http://installengine.com/cert02/isengine/isscript.msi) in the internet archive.

Finally go to your `hosts` file in your virtual machine (C:\WINDOWS\system32\driver\etc\hosts) and add the following lines to the bottom of the file.

`www.installengine.com 127.0.0.1` 

`installengine.com 127.0.0.1` 

This will stop the installer from trying to reach the url and find it locally. 

Proceed with the installation according to the manual (in sources)

## Sources
G-Book SDDOWNLOAD tool:
http://g-book.com:80/downloads/SDDOWNLOADAPL/Windows/V1.20/GbookDlSetup.exe

Also can be found in this repo [here](./GbookDlSetup.exe)

G-Book SDDOWNLOAD tool manual:
https://g-book.com/downloads/SDDOWNLOADAPL/Manual/Windows/v1.20/GbookDLmanual.pdf

G-Book Maps on demand info
https://tconnect.jp/faq/mod/howto/2035.html

The reddit post that saved the installation:
https://www.reddit.com/r/techsupport/comments/c6pull/comment/hi7zk0a/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button

The file that needs to be installed:
https://web.archive.org/web/20050218191725/http://installengine.com/cert02/isengine/isscript.msi