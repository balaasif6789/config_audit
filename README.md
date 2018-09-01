# config_audit

Source: http://www.vulnerabilityassessment.co.uk/nipper.htm

Nipper
 
Nipper is a Network Infrastructure Configuration Parser. Nipper takes a network infrastructure device configuration, processes the file and details security-related issues with detailed recommendations. Nipper was previous known as CiscoParse.
 
It is available from here.
 
Syntax

nipper.exe [Options]

--input=<file> Specifies a device configuration file to process. For CheckPoint Firewall-1 configurations, the input should be the conf directory.

--output=<file> | --report=<file> Specified an output file for the report.

--csv=<file> Want to output the network filtering configuration to a CSV file?.

--version Displays the program version.
 
--help[=<topic>] Show the online help or show the additional help on the topic
specified. The help topics are; GENERAL, DEVICES, DEVICES-ADV,REPORT, REPORT-ADV, REPORT-SECT, REPORT-HTML, REPORT-LATEX,AUDIT-ACL, AUDIT-PASS, AUDIT-ADV or CONFIG-FILE.
 
--force Force Nipper to bypass any configuration type checks.
 
--location=<edge | internal> Where is the device located.
 
--model=<device model> Specify a device model, such as 7200VXR for a Cisco 7200VXR.
 
Nipper supports a number of different report formats. They are:
 
--html HTML (default)
--latex Latex
--text Text
--xml XML
 
The device types currently supported by nipper are specified using the following command line parameters:
 
CMD Option Device Type:
 
--ios-switch Cisco IOS-based Switch
--ios-router Cisco IOS-based Router (default)
--ios-catalyst Cisco IOS-based Catalyst
--pix Cisco PIX-based Firewall
--asa Cisco ASA-based Firewall
--fwsm Cisco FWSM-based Router
--catos Cisco CatOS-based Catalyst
--nmp Cisco NMP-based Catalyst
--css Cisco Content Services Switch
--screenos Juniper NetScreen Firewall
--passport Nortel Passport Device
--sonicos SonicWall SonicOS Firewall
--fw1 CheckPoint Firewall-1 Firewall
 
Example:
The example below will process a Cisco IOS-based router configuration file called ios.conf and output the report to a file called report.html.

nipper.exe --ios-router --input=ios.conf --output=report.html
