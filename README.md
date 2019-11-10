RCP2GEMS.exe for easier use  
==================
The python version is now converted as an executable to make using easier for people that are not comfortable with console. If you are struckling with console grab an installer from python folder but notice that it has limited features. To use the programm select your log file and "open with..." RCP2GEMS.exe. The program will then convert and rename the file automatically. At the moment the minimum satellites value is set to 2 but in **future** there will be some kind settings section where it would be possible to change it.


RCP2GEMS
========

Conversion script that converts the RaceCapture/Pro CSV file format to a format compatible with the GEMS Data Analysis Software http://www.gems.co.uk/

Requires:

* Perl (tested with Perl 5.18.2)
* Text::CSV Perl module 

Usage:

    rccsv2gems.pl INPUTFILENAME OUTPUTFILENAME --minsats=X --disable-gps-cleanup
        (optional)  --minsats=X where X is the minimum number of gps satellites required for valid data (sets lat/long to null if GpsSats value is less than min) Default is 4.
        (optional)  --disable-gps-cleanup disables the cleanup per the GpsSats value. Useful when you don't care or don't have the GpsSats column logged.


Installing Dependencies
=======================

This script requires a Perl add-on module for processing CSV files, the native file format for RaceCapture/Pro. To install this module, issue the command:

    > cpan Text::CSV

First time example 
==================

##Initial Conversion
Here's an example using demo log file. Assuming requirements are met, issue the following command:

    > perl rccsv2gems.pl RCP_Demo.LOG  RCP_Demo_dlog.csv

##Intermediate conversion
Now, open dlog99, select file->import, follow the instructions to select the RCP_Demo_dlog.csv you created in the previous step, and save it as a .stf file

##Opening in GEMS
Finally, load GEMS and load the .stf file you created in the the last step



