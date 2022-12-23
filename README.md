# chapt11exerPHP

Textbook: PHP and MySQL for Dynamic Web Sites: Visual QuickPro Guide (5th Edition) Written by Larry Ullman

This chapter has multiple parts, and several need additional information. Read through these instructions, and read Chapter 11 in the textbook as directed.

## Task 1: Sending Email

Sending email can be difficult because there are so many different email servers and systems. Current XAMPP versions include the SMTP server "sendmail". The computers in the classroom use Chrome. The instructions included here are for gmail accounts and Chrome. If you do not already have a gmail account, create one for this assignment.

First, read the section about sending email in the book, and create the email.php file as detailed in the book. NOTE: in the form code for the textarea tag, make sure there are no extra spaces between the textarea tag and its closing tag. That is, don't make the code "pretty" by spacing things out or pressing Enter to move some of the PHP code down to a new line. The spaces will be part of the textarea, when it should be completely empty. When you click into the textarea in the web browser, the cursor should go to the upper left corner of the box. If it goes anywhere else inside that box, you have spaces between the opening and closing textarea tags, and need to remove them.

Second, read this (https://github.com/bell-kevin/chapt11exerPHP/blob/main/EmailNotes.pdf) document about setting up the sendmail option Download this document about setting up the sendmail optionand make the changes specified. NOTE: It is very important that you make a copy of the php.ini and sendmail.ini files before you begin editing them. Make sure you have a copy of the original files, because trying to recreate them if there are mistakes in editing will be complex. Always keep a copy of the original files as a backup. UPDATE: https://support.google.com/accounts/thread/173280862?hl=en Links to an external site.Google got rid of the less secure apps feature around the end of May this year. Log into your Gmail account and enable 2-step verification. This will allow you to create an app password for Mail. Use this app password in place of your account password in the sendmail.ini. UPDATE of the UPDATE: However, the section of the updated paragraph "Use this app password in place of your account password in the sendmail.ini and php.ini". You only need to update the password in the sendmail.ini file. (see the sendmail.ini file in this repo. for example help)

The php.ini doesn't need updating and may cause some confusion in the future when a student tries to find the place to put the password, but it doesn't exist. Thanks!

Third, start the Apache server and run the email.php script. It presents a form to fill out, and when you click the Submit button, it should respond as outlined in the book, and send an email to your email account.

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/PXL_20221222_210617215.jpg)

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/bb8869e1-ade6-4288-a990-92e97139ff01.png)

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/folders.png)

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/forbid.png)

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/shell.png)

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/internetDiagram.jpg)

Once that is working, you need to make some changes to the email that is generated. The book's script displays the name and comments from the contact form. The email sent using the sendmail server will be from your email account and to your email account, so there is no way to know the user's email address. In the email.php script, add the email address between those fields. Write a comment that is more than 70 characters long, to test the wordwrap function. Take a screenshot of the email you receive. It should resemble this:

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/Capture1.PNG)

Submission: Please take and submit .png screenshots showing your working code running in a browser and your source code for 11.1, 11.2, 11.4, 11.5, and 11.6; place all files in a .zip file.

## Info. on How to Install XAMPP:

If you are working on a classroom computer it is best to install XAMPP on your own flash drive.

If you are working on your personal computer it is best to install XAMPP on your computer.

Warning: The process of installing the XAMPP software can take 45 minutes to more than 1 hour.

In this exercise, you will accomplish two specific tasks required to proceed further in this course.  First, you will download and install the XAMPP software suite onto a USB flash drive (or your computer). Second, you will download and install a sample SQL database which you will use through the XAMPP software suite to complete further exercises in this course. This exercise goes way beyond the material presented in the textbook and you will need to make sure you read carefully and understand both the "big picture" and the specific steps contained in this exercise.

XAMPP is an open-source project that produces a suite of software that allows the Apache web server, MySQL relational database software, and the languages Perl and PHP to be loaded under several operating systems. The X stands for "cross-platform / any operating system" , the A for Apache, the M for MariaDB, and the PP for Perl and PHP. This collection of software was originally developed to run under the Linux or Unix operating systems and has become the dominant Internet hosting platform. When running under Linux, it is known as LAMP (you may recall accessing the department's "LAMP" server as part of your Web Fundamentals course). XAMPP was originally developed to provide Windows and Mac web developers a "test bed" development environment to test their work prior to live deployment to the Internet on a LAMP server.

ApacheFriends.Com touts: "XAMPP is an easy to install Apache distribution containing MySQL, PHP, and Perl. Just download and start the installer. It's that easy." ... and for the most part, it can be that simple. When a program is installed under a Windows operating system, one typically uses an "installer" application to place all of the files in the right place and to create/modify the appropriate entries in the Windows registry. Since you will need to use XAMPP on multiple classroom machines, you need a "portable" version of the XAMPP suite that can be installed and exist on a USB flash drive, and most importantly can move from classroom PC to classroom PC (machine-independent install). A machine-independent install is not quite as simple as running the installer, but it is almost that simple.

Once you get XAMPP up and running, you will need to access the Apache Web Server, MySQL, and PHP capability and install the sample SQL database used by the textbook for chapter exercises. Typically, SQL databases need to be installed and reside on a single database server. This is the main reason you need a portable version of XAMPP on a USB flash drive. In order for your MySQL server to reliably find its "data repository" or location where a MySQL RDMS stores its databases, your USB flash drive must maintain a consistent drive letter identity when moved from computer to computer.  

The installation process that follows is not particularly difficult, but it is exacting and unforgiving. Pay close attention to details.

Preparing the USB Flash drive:
You will need to install the XAMPP software and your database on a USB Flash Drive. It would be best if the flash drive was completely empty and utilized for the purposes of this coursework alone. Failure to abide by this advice may result in loss of data or other unforeseen negative outcomes, you have been warned!

Insert your USB flash drive into the workstation, making sure that the drive is recognized and available for use.

 
### Installing XAMPP on a USB Flash drive:
1. Download xampp  

If you are using Microsoft Windows operating system, in a new browser window, go to https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/.
In the middle of the screen, you should see a list of releases for xampp. Pick the latest release.  As of this posting 7.2.12 was the latest release.

There are a number of types of downloads you can pick.  Portable vs. Non-Portable.  Non-Portable has a few applications you will not need in this course.  We will use the portable version.  You do not have administrative rights to run the .exe files on the classroom computers so this leaves you with two options, a .7z file and a .zip file.  Either one is fine, if you do not know what 7-Zip is click the .zip file.  The file should download when you click on it.

When the file is downloaded uncompress the files (right-click > 7-Zip > Extract Here).  This should give you a xampp folder.  Move the xampp folder to your flash drive.  The folder is about 500 MB so this will take a few minutes.

2. Setting up the environment

   A. Open the xampp folder.
   
   B. Click on the setup_xampp.bat file.  The batch file will do a number of updates to the files in the folder; for example, getting the OS of the computer and updating all the configuration files for the drive letter of the flash drive.    

3. Start the XAMPP Control Panel by clicking on the xampp-control.exe file.

![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/OpenXAMPP.PNG)

 4. Start the Apache Web server and MySQL database by clicking on the associated start buttons.
 
![p](https://github.com/bell-kevin/chapt11exerPHP/blob/main/pictures/control-panel-started.PNG)

5. Open a web browser and navigate to http://localhost Links to an external site.and you should be redirected to the PHP server dashboard.

6. To close XAMPP, you must stop the Apache Server and the MySQL Server by clicking the Stop buttons.  To close the control panel you need to click the "Quit" button.

Important: when you installed XAMPP on your flash drive, all of the configuration files were mapped to the drive assigned to the flash drive at the time of installation. If you plug the flash drive in and the computer assigns the drive a different letter, you can update the configuration files by running the setup_xampp.bat file in the xampp folder on your flash drive.

I have seen flash drive become corrupted while using xampp.  It is best practice to safely eject your flash drive before removing it.  To safely remove the flash drive you must stop Apache, MariaDB, and the Control Panel.  If you close the control panel from the X in the upper right-hand corner of the control panel it will run in the background.  You will need to open the running process in the hidden icon on the taskbar right-click the control panel icon and click quit.

== We're Using GitHub Under Protest ==

This project is currently hosted on GitHub.  This is not ideal; GitHub is a
proprietary, trade-secret system that is not Free and Open Souce Software
(FOSS).  We are deeply concerned about using a proprietary system like GitHub
to develop our FOSS project. I have a [website](https://bellKevin.me) where the
project contributors are actively discussing how we can move away from GitHub
in the long term.  We urge you to read about the [Give up GitHub](https://GiveUpGitHub.org) campaign 
from [the Software Freedom Conservancy](https://sfconservancy.org) to understand some of the reasons why GitHub is not 
a good place to host FOSS projects.

If you are a contributor who personally has already quit using GitHub, please
email me at **bellKevin@pm.me** for how to send us contributions without
using GitHub directly.

Any use of this project's code by GitHub Copilot, past or present, is done
without our permission.  We do not consent to GitHub's use of this project's
code in Copilot.

![Logo of the GiveUpGitHub campaign](https://sfconservancy.org/img/GiveUpGitHub.png)
