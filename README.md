# Syntax Highlighting Definition File for AppArmor Profiles, for KatePart

**Author:** Nibaldo González (<nibgonz@gmail.com>) (Valparaíso, Chile)

**Last Change:** September 2017

*This file is part of the KDE's Kate project.*

## Description:

Add syntax highlighting to KDE text editors (as Kate and KWrite) 
for the **AppArmor Security Profiles**.

The file `apparmor.xml` contains the definition of the syntax highlighting. 
If you want to test the highlighting, you can find a sample AppArmor profile 
in the `test` folder.

## About Syntax Highlighting Files of KatePart:

Syntax highlighting definition files of KatePart consist of XML files 
that are compiled in the KDE Frameworks libraries.

However, these XML files can also be stored in:

	/usr/share/katepart5/syntax/
	/home/<user>/.local/share/katepart5/syntax/
	/usr/share/kde4/apps/katepart/syntax/  [old]

For more details on the syntax highlighting, visit:
* Documentation: https://docs.kde.org/stable5/en/applications/katepart/highlight.html
* Official Repository: https://phabricator.kde.org/source/syntax-highlighting/

## Installation:

Copy the `apparmor.xml` file to: `/usr/share/katepart5/syntax/` or `~/.local/share/katepart5/syntax/`.

E.g.:

	`sudo cp ./apparmor.xml /usr/share/katepart5/syntax/`
	`cp ./apparmor.xml ~/.local/share/katepart5/syntax/`
