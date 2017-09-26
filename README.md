# Syntax Highlighting Definition File for AppArmor Profiles, for Editors Kate and KWrite

Author: Nibaldo González (<nibgonz@gmail.com>) (Valparaíso, Chile)

Last Change: September 17, 2017

## Description:

Add syntax highlighting to KDE text editors (as Kate and KWrite) 
for the **AppArmor Security Profiles**.
	
**Note:** [September 16, 2017] The syntax highlighting file for AppArmor Profiles 
(appamor.xml + test files) is part of KatePart.

## About Syntax Highlighting Files:

Syntax highlighting definition files of KatePart consist of XML files 
that are compiled in the KDE Frameworks libraries.

However, these XML files can also be stored in:

	/usr/share/katepart5/syntax/
	/usr/share/kde4/apps/katepart/syntax/

For more details on the syntax highlighting, visit:
* Official Repository: https://phabricator.kde.org/source/syntax-highlighting/
* Documentation: https://docs.kde.org/stable5/en/applications/katepart/highlight.html

## Installation:

Copy the *.xml files to: `/usr/share/katepart5/syntax/`

E.g.: `sudo cp ./apparmor.xml /usr/share/katepart5/syntax/`
