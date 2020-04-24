# AppArmor Profiles Syntax Highlighting Definition for Kate (KSyntaxHighlighting Framework)

![Example of AppArmor profile syntax highlighting](https://raw.githubusercontent.com/nibags/apparmor-ksyntaxhighlighting/master/test/images/apparmor-preview.png)

**Author:** Nibaldo González (<nibgonz@gmail.com>)

**Last Change:** June 2019

**Last Version:** Version 9 is included in KDE Frameworks 5.60.0+ and is based on AppArmor 2.13.3.

    This file is part of the KDE's KSyntaxHighlighting Framework.


## Description:

Add syntax highlighting to KDE text editors (such as Kate, KWrite, KDevelop 
or any application that uses the KSyntaxHighlighting or KTextEditor Framework) 
for the **AppArmor Security Profiles**.

The `apparmor.xml` file contains the definition of the syntax highlighting. 
If you want to test the highlighting, you can find a sample AppArmor profile 
in the `test` folder.

For details on the syntax of AppArmor profiles, visit:
* AppArmor Documentation: https://gitlab.com/apparmor/apparmor/wikis/Documentation
* Man Page of apparmor.d: http://manpages.ubuntu.com/manpages/cosmic/en/man5/apparmor.d.5.html
* AppArmor Repository: https://gitlab.com/apparmor

## About XML Files of Syntax Highlighting Definition:

The syntax highlighting definition files, of the KSyntaxHighlighting Framework, 
consist of XML files that are compiled in the KDE Frameworks libraries.

However, these XML files can also be stored in:

<table>
    <tr>
        <td>For local user</td>
        <td>$HOME/.local/share/org.kde.syntax-highlighting/syntax/</td>
    </tr>
    <tr>
        <td>For all users</td>
        <td>/usr/share/org.kde.syntax-highlighting/syntax/</td>
    </tr>
    <tr>
        <td>For <a href="https://flathub.org/apps/details/org.kde.kate">Kate's Flatpak package</a></td>
        <td>$HOME/.var/app/org.kde.kate/data/org.kde.syntax-highlighting/syntax/</td>
    </tr>
    <tr>
        <td>For <a href="https://snapcraft.io/kate">Kate's Snap package</a></td>
        <td>$HOME/snap/kate/current/.local/share/org.kde.syntax-highlighting/syntax/</td>
    </tr>
</table>

For more details of KSyntaxHighlighting Framework, visit:
* Official Repository: https://phabricator.kde.org/source/syntax-highlighting/
* Documentation: https://docs.kde.org/trunk5/en/applications/katepart/highlight.html

## Installation:

If you do not have the latest version of KDE Frameworks, you can manually install 
the latest `apparmor.xml` file.

Copy the `apparmor.xml` file to the directory of the XML syntax definition files,
mentioned in the previous section.

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
For Kate's Flatpak package:
```bash
mkdir -p $HOME/.var/app/org.kde.kate/data/org.kde.syntax-highlighting/syntax/
cp ./apparmor.xml $HOME/.var/app/org.kde.kate/data/org.kde.syntax-highlighting/syntax/
```
For Kate's Snap package:
```bash
mkdir -p $HOME/snap/kate/current/.local/share/org.kde.syntax-highlighting/syntax/
cp ./apparmor.xml $HOME/snap/kate/current/.local/share/org.kde.syntax-highlighting/syntax/
```

## Usage:

Syntax highlighting of AppArmor profiles is automatically applied to named files: 
`bin.*`, `sbin.*`, `usr.bin.*`, `usr.sbin.*`, `usr.lib.*`, `usr.lib64.*`, `usr.lib32.*`, 
`usr.libx32.*`, `usr.libexec.*`, `usr.local.bin.*`, `usr.local.sbin.*`, `usr.local.lib*`, 
`opt.*`, `etc.cron.*`, `snap.*`, `snap-update-ns.*` & `snap-confine.*`.

You can also force the syntax highlighting, by writing a comment with:

    kate: syntax AppArmor Security Profile;


## List of Versions:

<table>
    <tr>
        <th>apparmor.xml<br>Version</th>
        <th>Date</th>
        <th>KDE<br>Frameworks</th>
        <th>AppArmor<br>Support</th>
        <th>Relevant Changes</th>
    </tr>
    <tr>
        <td>9</td>
        <td>Jun. 20, 2019</td>
        <td>5.60.0</td>
        <td>2.13.3</td>
        <td><ul>
            <li>Add new network domain keywords.</li>
            <li>Fixes: remove unsupported "to" operator for link rules and only highlight the "in" operator in mount rules. Only highlight valid numbers in rlimit rules.</li>
        </ul></td>
    </tr>
    <tr>
        <td>8</td>
        <td>Apr. 02, 2019</td>
        <td>5.58.0</td>
        <td>2.13.2</td>
        <td><ul>
            <li>Do not highlight variable assignments and alias rules within profiles.</li>
            <li>Remove one indentation.</li>
        </ul></td>
    </tr>
    <tr>
        <td>7</td>
        <td>Sep. 15, 2018</td>
        <td>5.51.0</td>
        <td>2.13.0</td>
        <td><ul>
            <li>Update itemData's style for the new Solarized color schemes of Kate.</li>
            <li>Fixed freezing of Kate when using this highlighter in open rules, after the update to KF5.50.0.</li>
        </ul></td>
    </tr>
    <tr>
         <td>6</td>
         <td>Jul. 24, 2018</td>
         <td>5.50.0</td>
         <td>2.13.0</td>
         <td><ul>
            <li>Add "if exists" in Include rules.</li>
            <li>Multiple fixes and improvements.</li>
        </ul></td>
    </tr>
    <tr>
        <td>4 & 5</td>
        <td>Jan. 25, 2018</td>
        <td>5.43.0</td>
        <td>2.12.0</td>
        <td><ul>
            <li>Add keywords of network and mount rules, default abstractions, default variables and others.</li>
            <li>Do not allow comments within rules and in variable assignment lines.</li>
        </ul></td>
    </tr>
    <tr>
        <td>2 & 3</td>
        <td>Sep. 24, 2017</td>
        <td>5.39.0</td>
        <td>2.11.0</td>
        <td><ul>
            <li>Each rule has its own context.</li>
            <li>The profile label is highlighted in the profile header and the profile transition rules.</li>
        </ul></td>
    </tr>
    <tr>
        <td>1</td>
        <td></td>
        <td></td>
        <td></td>
        <td>Initial version, not published.</td>
    </tr>
</table>

<!-- kate: syntax Markdown; -->
