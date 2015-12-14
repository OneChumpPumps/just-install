# Just Install

<img src="https://cdn.rawgit.com/lvillani/just-install/4953fdccb9614bbdb2b77991610db6b99b1757d1/misc/cube.svg" align="right" width="200" height="200"/>

_The simple package installer for Windows_

[![Build Status](http://img.shields.io/travis/lvillani/just-install.svg?style=flat)](https://travis-ci.org/lvillani/just-install/)
[![License](http://img.shields.io/badge/license-GPL%203.0-blue.svg?style=flat)](http://choosealicense.com/licenses/gpl-3.0/)
[![Semver](http://img.shields.io/badge/version-v3.1.0-blue.svg?style=flat)](https://github.com/lvillani/just-install/blob/master/CHANGELOG.md)
[![ML](https://img.shields.io/badge/ML-justinstall@librelist.com-orange.svg)](http://librelist.com/browser/justinstall)

--------------------------------------------------------------------------------

**NEW**: Subscribe to the mailing list by sending an email to <justinstall@librelist.com>

just-install is a simple program that automates software installation on Windows. [Unlike the
alternatives](http://lorenzo.villani.me/2013/04/08/just-install-my-stuff/), we strive to do one
simple thing and do it well: download a `setup.exe` and install it, without bothering the user.

To see the list of available packages head over to <http://just-install.it>.


## Installation

Run this command in a command prompt, as Administrator:

```batch
msiexec.exe /i http://go.just-install.it
```

If you like more traditional means of installation then download
[just-install.msi](http://go.just-install.it) and double click the file to install it yourself.


## Usage

To install a package:

    just-install firefox

To view a list of available packages:

    just-install list

To update the list of available packages:

    just-install update

To forcibly re-download an installer and re-run it:

    just-install -f firefox

To force installation of a package for a specific architecture (use "x86" or "x86_64"):

    just-install -a x86 go

In case you are lost, help is always few keystrokes away:

    just-install --help


## Contributing Packages

See [CONTRIBUTING.md](CONTRIBUTING.md)


## Frequently Asked Questions

### Why did you write this?

I needed something to automate software installation on Windows VMs at my workplace. The
alternatives at that time required either too much work to bootstrap themselves, were too slow,
buggy or didn't include the software I wanted. I needed something that could be installed with one,
memorable command, was self-contained, and could be launched from an unattended setup script.


### What's wrong with the alternatives?

* Chocolatey's biggest sin is that it requires PowerShell on the target system. This makes it
  ridiculously difficult to install on some operating system: on Windows XP it is a multi-stage
  ordeal where you first have to install .NET 2.0, then install PowerShell, then .NET 4 and after
  that you can finally install Chocolatey itself. Yes, we still have some software that has to work
  on Windows XP, which means that we have some VMs that we need automate.
* Ninite is great but it's closed source and there's no obvious way to add a custom package.
* Npackd is probably the most promising of the bunch, but the last time I tried it, it wanted to do
  some funny stuff such as handling un-installations and it had a tendency to shuffle files around.

I wanted something simple, something that would download an installer and run it silently. That's
why I wrote just-install. You can find a complete rationale
[on my blog post](http://lorenzo.villani.me/2013/04/08/just-install-my-stuff/)




## Credits

Cube icon derived from the one available from [Ionicons](http://ionicons.com/).
