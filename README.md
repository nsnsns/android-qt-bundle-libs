android-qt-bundle-libs
======================
The Necessitas Qt project is often used to compile and get Qt apps running on Android platform.
The way Necessitas handles shared libraries (.so files) is by using a system-wide service 
called "Ministro" to download and manage Qt shared libraries on the device.

This project aims to provide a template and demonstrate a approach to bundling Qt shared libraries with a app's APK.

Please be aware that Qt's LGPL license demands that all free users of Qt dynamically link to shared libraries such
that shared libraries can be updated-- and possibly replaced if desired by *any user* without breaking the application.
(for more on LGPL, see:  http://en.wikipedia.org/wiki/GNU_Lesser_General_Public_License )


If using current version of this OR any other similar way of bundling libs-- please ensure that you either distribute/ 
publish source code OR buy a commercial android-Qt license OR otherwise find a way to respect LGPL.


*****
(possibly TLDR background info)
*****
Disadvantages of Necessitas' default approach to managing shared Qt Libraries:
1. Often after downloading a (possibly paid) app from Google-play-- the app demands Ministro+dozens of megabytes 
of shared libs to be installed-- which takes a lot of time and energy from a user.

2. Often Download of dozens of MBs of Qt shared libs-- takes many minutes-- after paying and downloading 
app apk on Google-play leads to people losing their chance to get a refund on a app within 15 minutes 
of paying.

3. If a user-- who may buy commercial Android-QT to personally fix bugs-- wants to see if changes in Qt libs 
will help fix bugs etc-- then the current approach of managing shared libraries through ministro doesnt give 
him this option.

AIM of this project is to allow Qt shared libraries

Some Background:
This project was originally released by Nalin Savara on the KDE Community wiki below-- on sept.6th, 2012.
http://community.kde.org/KDE_Community_Wiki:Community_portal

***DESCRIPTION AS PUBLISHED ON THE KDE COMMUNITY PORTAL WIKI***

Bundling libraries with Qt Android apps is often important because many times it is too inconvenient to 
download libraries OR for example when internet access is expensive or not available.

Attached project shows how to bundle libraries with a Qt Android Project.

http://community.kde.org/File:AndroidQt-BundlingQtLibs.zip

Regarding the attached ZIP file: - includes the following libraries for armv5 build: QtCore, QtNetwork, 
QtSystemInfo, QtGui (add or subtract depending on allowed filesize and dependancies.

- includes the ability to handle back button and after asking user Quit: yes/no; quits when 
back button is pressed.

- still needs ministro as a dependancy-- but doesnt make ministro download libraries. todo: edit QtActivity.java to remove ministro dependancy and upload (if I do) OR mail to me-- and I'll update the project.

For comments, questions, queries; drop me a email: nsnsns(at)gmail(dot)com -- and I'll do my best to help.

However, I am often busy- so please first do try to first ask in Android-Qt mailing list; and please also do try to help others in community and do try to contribute your code-changes to make the android-qt effort even better.

Thank you and do feel free to say hello: nsnsns(at)gmail(dot)com OR add me on linkedin: http://www.linkedin.com/in/nsnsns

My special thanks to XumuK ; Izaar for their earlier efforts to help peoeple bundling libraries. XumuK thanks for helping me; and Izaar thanks for your tutorial and sharing code.

Good Luck...

Nalin Savara Thursday, 6th Sept, 2012

ps: code is meant for; tested on and builds with Necessitas QtCreator Alpha3 -- in time, guys do try to submit a newer better version of this... that works with Alpha4


