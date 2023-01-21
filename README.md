# Security Event Detection and Analysis Automation tool

As a SOC Analyst, incident detection, analysis and mitigation is a rigorous task. The project aims at automating the detection, investigation & validation of possible Indicators of Compromise (IOCs) and perform various tasks including Phishing Email Analysis & Brand Monitoring to improve the potential security incident response. The main goal of utilizing this tool is to automate as many validation points as possible being performed by Enterprise Security Operations Team while working on any security incident including brand monitoring and possible phishing attack.

The tool also implements encryption(symmetric) so all your API keys are secret & safe and cannot be manipulated until the secret encryption key is used. You can anytime however edit your API keys if you have access to encryption key.


## Pre-requisites

    1. Python 3.x installed on the end system
    2. All dependencies mentioned in requirements.txt file.
    3. API keys from multiple threat intelligence platforms being used.

Features

Requirements.txt

How to Use

Pull Requests

Change Log & Future Updates

## Features

This tool can currently perform below tasks :

   - Reputation check of IP Addresses, Domains, URLs & File Hashes from :
       - Virustotal
       - Abuse IP DB
       - Alienvault OTXv2
       - Spyse
       - Phishtank
       - URL Scan
   - Performing DNS, Reverse DNS, WHOIS, ISP Lookups
   - Email Security Analysis (Phishing Email Analysis)
       - Verifying Email Address Reputation (Using Emailrep.io)
       - Analyzing a Phishing URL
       - Snadbox a malicious file attachment present in email
       - Email Header Analysis
       - General Guidelines to perform phishing email analysis to identify threats
   - Decoding Office365 Safelink URLs, UTF-8 Encoded or Base64 encoded URLs
   - Unshortening the shortened URLs
   - Performing File Sandboxing for file and its associates file hash reputation
   - Sanitization/Masking of Indicators of Compromise(IOCs) so that same can be sent safely over an email
   - Performing Brand Monitoring Analysis

Requirements.txt

   1. Python 3.x installed on machine
   2. Install all dependencies through requirements.txt file.

```
pip install -r requirements.txt
```
   3. Multiple threat intelligence platforms' APIs are being utilized in this script, hence API keys from these platforms are required to confirm full functionality of script. Create accounts using below links and capture the API Keys from the same. Further details on feeding keys to code will be discussed in How to Use section of README.md.

   - Virustotal API Key
   - Abuse IP DB API Key
   - Alienvault OTXv2 API Key
   - Spyse API Key
   - URL Scan IO API Key
   - Emailrep.io API Key

### How to Use

The script is simple to understand and use. It can be utilized to its full functionality without opening/editing source code. Isn't that great?

Here is how we achieved this :

1. Upon executing the main script for the first time, it will automatically direct you to configuration menu, where in you will be requested to enter the API keys of platforms used in the tool.
2. All subsequent executions will present you with the menu directly unless there is some issue with access to keys file.
3. All the API Keys are managed separately in API keys file. The API keys are also encrypted with Symmetric key encryption so same can't be manipulated unless you have access to encryption key.
4. The script is platform independent and the platform will be determined directly through script.
5. For complete code review and easy understanding, different modules have been created in different script code and same can be imported based on the requirements in other parts of the script. You only need to execute single script code i.e main_file.py and based on selection respective modules will function.

### 1. Getting Started

In order to start utilizing the tool, you just need to clone this repository.
```python
git clone https://github.com/akashyadav1507/security-event-detection-and-analysis-automation-tool/
```
Once cloned successfully, change directory to security-event-detection-and-analysis-automation-tool/Security Analysis Automation/.

### 2. Requirements.txt

Install all dependencies through requirements.txt file.
```
pip install -r requirements.txt
```

### 3. Running the script

Once the dependencies are installed successfully, the tool is ready for use. Run the script by executing

```python
python main_file.py
```
Upon successful execution of script for the first time, you will be directed to import your API Keys in to the tool. Check Requirements.txt step number 3 to generate the API Keys and import them during runtime.

### 4. Tool is ready!!

Once the API keys are successfully imported into the tool, the tool is ready to use. Simply navigate through the command options and perform almost all validation checks as you go along your security incident response process.

A simpler view of menu is given below for assistance :

    1. Python 3.x installed on machine
    1. Reputation/Blocklist Check (IPs, Domains, URLs, Hashes)
      i. Enter Respective entity to check for its reputation.
    2. DNS/WHOIS Lookup Options
      i. Reverse DNS Lookup
      ii. DNS Lookup
      iii. WHOIS Lookup
      iv. ISP Lookup
    3. Email Security (Phishing Email Analysis)
      i. Email Address Verification
      ii. Analyze a Phishing Site
      iii. Sandbox an Email Attachment
      iv. Email Header Analysis
      v. General GUidelines for Identification of Phishing Attack
    4. URL Decoding for Investigation
      i. Simple URL Decoder - UTF-8
      ii. Base64 Decoder
      iii. Office365 SafeLink Decoder
      iv. UnShorten the URL
    5. File Upload for Sandboxing
    6. Sanitization of IOCs for email
      i. Single Input
      ii. Upload a file with multiple values(Bulk Upload)
    7. Brand Monitoring & Analysis
      i. Check for Geography of URL
      ii. Check for main UI of URL/Social Media Account/Mobile App
      iii. Check for URL Reputation
    8. Help & Configuration/Re-configuration
      i. Help Menu
      ii. Configure or Re-configure API Keys


## Pull Requests

If you have any valuable suggestions & changes to add, feel free to make a pull request. Your contribution to the project is as important and appriciated as the inital release and I will make sure these are implemented with validation.

## Change Log & Future Updates

This is the First Version of tool. Below are few planned future updates :

    1. Bulk Validation of IOCs
    2. Tools supporting Red Team Exercises.

## Author

Akash Chaitanya Yadav
