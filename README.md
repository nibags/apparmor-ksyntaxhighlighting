# AppArmor Profiles Syntax Highlighting Definition File for Kate

**Author:** Nibaldo González (<nibgonz@gmail.com>)

**Last Change:** September 2018

```
This file is part of the KDE's KSyntaxHighlighting Framework.
```
**Last version:** Version 7 is included in KDE Frameworks 5.51.0+. 

**Old versions:** Version 6 is included in KDE Frameworks 5.50.0+, version 5 in KDE Frameworks 5.43.0+ and version 3 in KDE Frameworks 5.39.0+. 


## Description:

Add syntax highlighting to KDE text editors (as Kate, KWrite, KDevelop 
or any application that uses the KSyntaxHighlighting or KTextEditor Framework) 
for the **AppArmor Security Profiles**.

The file `apparmor.xml` contains the definition of the syntax highlighting. 
If you want to test the highlighting, you can find a sample AppArmor profile 
in the `test` folder.

## About XML Files of Syntax Highlighting Definition:

The syntax highlighting definition files, of the KSyntaxHighlighting Framework, 
consist of XML files that are compiled in the KDE Frameworks libraries.

However, these XML files can also be stored in:

	$HOME/.local/share/org.kde.syntax-highlighting/syntax/
	/usr/share/org.kde.syntax-highlighting/syntax/

For more details of KSyntaxHighlighting Framework, visit:
* Official Repository: https://phabricator.kde.org/source/syntax-highlighting/
* Documentation: https://docs.kde.org/stable5/en/applications/katepart/highlight.html


## Installation:

If you do not have the latest version of KDE Frameworks, you can manually install the latest `apparmor.xml` file. 

Copy the file `apparmor.xml` to `$HOME/.local/share/org.kde.syntax-highlighting/syntax/` (for local user) or `/usr/share/org.kde.syntax-highlighting/syntax/` (for all users).

Ex.: 
For local user:
```bash
mkdir -p $HOME/.local/share/org.kde.syntax-highlighting/syntax/
cp ./apparmor.xml $HOME/.local/share/org.kde.syntax-highlighting/syntax/
```
For all users:
```bash
sudo mkdir -p /usr/share/org.kde.syntax-highlighting/syntax/
sudo cp ./apparmor.xml /usr/share/org.kde.syntax-highlighting/syntax/
```

## Usage:

Syntax highlighting of AppArmor profiles is automatically applied to named files: 
`bin.*`, `sbin.*`, `usr.bin.*`, `usr.sbin.*`, `usr.lib.*`, `usr.lib64.*`, `usr.lib32.*`, `usr.libx32.*`, 
`usr.libexec.*`, `usr.local.bin.*`, `usr.local.sbin.*`, `usr.local.lib*`, `opt.*`, `etc.cron.*`, `snap.*`, `snap-update-ns.*` & `snap-confine.*`.

You can also force the syntax highlighting, by writing a comment with: 
```
kate: syntax AppArmor Security Profile;
```
<!-- kate: syntax Markdown; -->
