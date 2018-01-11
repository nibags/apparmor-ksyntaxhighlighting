# AppArmor Profiles Syntax Highlighting Definition File, for the KSyntaxHighlighting Framework

**Author:** Nibaldo González (<nibgonz@gmail.com>) (Valparaíso, Chile)

**Last Change:** January 2018

```
This file is part of the KSyntaxHighlighting Framework of KDE. 
Version 3 is included in KDE Frameworks 5.39.0 and higher.
```

## Description:

Add syntax highlighting to KDE text editors (as Kate, KWrite, KDevelop 
or any application that uses the KSyntaxHighlighting Framework) 
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
* Announcement: https://kate-editor.org/2016/11/15/ksyntaxhighlighting-a-new-syntax-highlighting-framework/


## Installation:

**NOTE:** KDE Frameworks 5.39.0 includes version 3 of the file `apparmor.xml`. Version 4 has not yet been published.

Copy the file `apparmor.xml` to `$HOME/.local/share/org.kde.syntax-highlighting/syntax/` (for local user) or `/usr/share/org.kde.syntax-highlighting/syntax/` (for all users).

Ex.: 
For local user:
```
mkdir -p $HOME/.local/share/org.kde.syntax-highlighting/syntax/
cp ./apparmor.xml $HOME/.local/share/org.kde.syntax-highlighting/syntax/
```
For all users:
```
sudo mkdir -p /usr/share/org.kde.syntax-highlighting/syntax/
sudo cp ./apparmor.xml /usr/share/org.kde.syntax-highlighting/syntax/
```

## Usage:

Syntax highlighting of AppArmor profiles is automatically applied to named files: 
`bin.*`, `sbin.*`, `usr.bin.*`, `usr.sbin.*`, `usr.lib.*`, `usr.lib64.*`, `usr.lib32.*`, `usr.libx32.*`, 
`usr.libexec.*`, `usr.local.bin.*`, `usr.local.sbin.*`, `usr.local.lib*`, `opt.*` & `etc.cron.*`.

You can also force the syntax highlighting, by writing a comment with: 
```
kate: syntax AppArmor Security Profile
```
