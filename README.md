# EGR226_Midterm_Project

This video guides viewers on how to build their own malware analysis tool using AET( Antivirus Evasion Tool). The central theme is to create a lab environment that mimics antivirus scanning to analyze malware effectively. The video demonstrates the installation and configuration of both the AETserver on a Windows machine and the AETclient on a Kali machine. It also covers how to scan files and analyze the results through both the command line and a web interface. By following this tutorial, viewers can gain practical experience in signature-based malware detection and understand how antivirus solutions identify malicious code.
1. 🛠️ Setting Up Malware Scanning Lab
The lab will mimic anti-scan.me for scanning malware with preferred antivirus. 

The tool used is called AVET, which stands for Antivirus Reduction. 

AVET provides a detailed report of flagged bytes, indicating the exact locations in the scanned file. 

It offers advantages over TrID check and comes with documentation for supported files. 



2. 🛠️ Setting Up the A Server for Malware Analysis
Two sets of tools are required, with the first being the A server, installed on Windows 10 without an antivirus. 

The sample submissions must have the submission turned off to prevent global malware flags. 

Installation involves using Python and PIP, followed by executing `pip install -r requirements.txt`. 

Any Import errors can typically be resolved by installing the C++ version and its dependencies. 

It's suggested to configure the server as a service to avoid manual startup. 



3. 🚀 Setting Up the Malware Analysis Tool
The speaker references a config.js file that contains settings for the IP, port, and engine to be used. 

A simple string is presented, allowing flexibility in naming, although the speaker chooses to keep it unchanged. 

Running the command `Python server.py` initiates the server successfully. 

The server can be accessed via local host, displaying a confirmation message stating that MZ is running. 



4. 🛠️ Setting Up the Malware Analysis Tool
The speaker is preparing to generate malware and initiate a scan using their car machine. 

The first step involves downloading a tool from the GitHub repository, which is done using the `git clone` command. 

After cloning, the speaker navigates to the directory containing the necessary files. 

The documentation specifies the need to install certain requirements and the Radar 2 reverse engineering framework for Unix. 

Installation of the Radar 2 framework is completed in a new terminal session, and focus shifts to the terminal with the downloaded tool. 



5. 🛠️ Building and Configuring the Malware Analysis Tool
The configuration file defines important parameters like IP address, port, and engine name, with an example being set to "Defender" for Windows Defender. 

The tool allows for various operations, including scanning single files or all files in app uploads, with configurable scan speeds. 

A generated payload file ( reverse shell) is uploaded for scanning, but it must specify the correct server configuration to initiate the scan. 

The tool processes files in chunks, adjusting the chunk size based on the scanning results, which can lead to delays. 

The web interface simplifies tracking scan progress and results, displaying detected signatures and matches in a user-friendly manner. 

5.1. ️ Configuring the Malware Analysis Tool
The configuration process begins by defining settings in the O file, particularly the IP and port for the Windows machine. 

A password is optional and can be specified for secure access to the web interface. 

The engine can be named; in this case, it is referred to as Defender, reflecting the antivirus being used. 

After configuration, the requirements are installed using the command `pip 3 install -r requirements.txt`. 

The tool can scan a single file, all files in the app uploads, and allows speed customization for scanning processes. 

5.2. ️ File Scanning Process using msfvenom
A simple msfvenom reverse shell is generated to scan a file for analysis. 

The output file is named test.exz, with variations like TZ TXZ specified for the scan. 

An error occurs stating the server cannot be found due to the config file rename, indicating the need for precise server specifications. 

The scanning process scans larger chunks of data, adjusting size based on detected items, which requires time to complete. 

Upon completion, the output shows detected signatures, revealing the matches found from the scanning process. 

5.3. ️ Setting Up the Malware Analysis Tool
Python 3 initiates a Flask process for hosting the analysis tool on multiple interfaces. 

Users can navigate to the Local Host to access the analysis interface. 

The interface allows for file uploads, which require specifying servers defined in the configuration file. 

Scanned files show relevant details such as the date, type, and matched signatures after file uploads. 

Users can view scan results, including sections scanned and conclusions based on Windows Defender. 

5.4. Exploring File Scanning with the Tool
The presenter demonstrates the tool's functionality by uploading a file named t.exe for scanning, which aids in generating detailed results. 

The tool scans files in chunks, varying based on the file's content to optimize the scanning process and yield accurate results. 

It is highlighted that the tool can upload files as small as 460 bytes, showcasing its efficiency with minimal file sizes. 

The tool allows customization, enabling users to change the analysis to different antivirus (AV) options, enhancing its versatility. 

The speaker appreciates the tool's design, stating it efficiently identifies which chunks were processed and which were not. 

5.5. Acknowledgments and Process Overview
The speaker expresses heartfelt gratitude to viewers and highlights appreciation for their first Patreon, emphasizing the impact of this support. 

Patrons gain access to custom tools and notes prepared over the speaker's years of experience. 

The signature-based detection process is time-consuming, involving file splitting and scanning. 

Current discussions focus solely on signature-based detection, not addressing heuristics or behavior-based methods. 

The capability to transfer files for scanning is enabled by an MZ interface over HTTP, utilizing Windows APIs for scanning procedures. 

Viewers are encouraged to ask questions or request reviews of materials in the comments. 
