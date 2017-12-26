# Syntax Highlighting Definition File for AppArmor Profiles, for KSyntaxHighlighting

**Author:** Nibaldo González (<nibgonz@gmail.com>) (Valparaíso, Chile)

**Last Change:** December 2017

```
This file is part of the KSyntaxHighlighting Framework of KDE. 
Included in KDE Frameworks 5.39.0 and higher.
```

## Description:

Add syntax highlighting to KDE text editors (as Kate, KWrite or any application that uses the KSyntaxHighlighting Framework) 
for the **AppArmor Security Profiles**.

The file `apparmor.xml` contains the definition of the syntax highlighting. 
If you want to test the highlighting, you can find a sample AppArmor profile 
in the `test` folder.

**NOTE:** KDE Frameworks 5.39 includes version 3 of the file `apparmor.xml`. Version 4 is still in beta.

## About Syntax Highlighting Files of KSyntaxHighlighting:

Syntax highlighting definition files consist of XML files 
that are compiled in the KSyntaxHighlighting library of KDE Frameworks. 

However, these XML files can also be stored in:

	$HOME/.local/share/org.kde.syntax-highlighting/syntax/
	/usr/share/org.kde.syntax-highlighting/syntax/

For more details of KSyntaxHighlighting Framework, visit:
* Official Repository: https://phabricator.kde.org/source/syntax-highlighting/
* Documentation: https://docs.kde.org/stable5/en/applications/katepart/highlight.html
* Announcement: https://kate-editor.org/2016/11/15/ksyntaxhighlighting-a-new-syntax-highlighting-framework/


## Installation:

Copy the file `apparmor.xml` to:
* For local user: `$HOME/.local/share/org.kde.syntax-highlighting/syntax/`
```
mkdir -p $HOME/.local/share/org.kde.syntax-highlighting/syntax/
cp ./apparmor.xml $HOME/.local/share/org.kde.syntax-highlighting/syntax/
```
* For all users: `/usr/share/org.kde.syntax-highlighting/syntax/`
```
sudo mkdir -p /usr/share/org.kde.syntax-highlighting/syntax/
sudo cp ./apparmor.xml /usr/share/org.kde.syntax-highlighting/syntax/
```

Version 3 of this file comes installed by default in KDE Frameworks 5.39.
