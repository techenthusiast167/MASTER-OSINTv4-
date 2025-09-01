# MASTER-OSINT - V4 - V5 - V6

Darknet OSINT Recon Probe - is a comprehensive open-source intelligence tool with 18 modules for digital reconnaissance and cybersecurity analysis. Built with Python, it provides a unified interface for various OSINT techniques.


- - - 

# Table of Contents

- Overview

- Virtual Environment
  
- Installation & Dependencies
  
- Module Guide
  
- API Setup
  
- Ethical Considerations
  
- Bug Reports & Contributions

- - - 

# Overview

Darknet OSINT Recon Probe is a comprehensive open-source intelligence tool with 18 modules for digital reconnaissance and cybersecurity analysis. Built with Python, it provides a unified interface for various OSINT techniques.

- - - 

# Create your virtual environment:

- virtualenv my_temp_venv
- source my_temp_venv/bin/activate



- - - 

# Installation & Dependencies

**Prerequisites**:

- Python 3.7+
  
- pip (Python package manager)

**Installation Steps**:

# 1. Install required dependencies:

    pip install requests beautifulsoup4 waybackpy spacy phonenumbers python-whois dnspython exifread tldextract

# 2. Download spaCy language model:

    python -m spacy download en_core_web_sm

# 3. Tool Installation

- Connect via the links below **(choose any version you want)** and install the the tool script manually using nano:
  
- **https://gist.github.com/techenthusiast167/45d802b026830981106af3b017c2e36d** - v4
- **https://gist.github.com/techenthusiast167/543719b32253663ed5b9d406ba8affef** - v5
- **https://gist.github.com/techenthusiast167/26484f737dc76841e7bdc11a6199a781** - v6
  
- **Example**:

      nano master_osintv4.py
  
- Press **Ctrl + O, Enter, and Ctrl + X** to save and exit


# 3. Make executable (Linux/macOS)

    chmod +x master_osintv4.py

# 4. Run the tool

    python master_osintv4.py


**Optional API Setup**


**Set environment variables for enhanced functionality**:

    export GITHUB_TOKEN='your_github_token_here'

    export HIBP_API_KEY='your_hibp_api_key_here' 
    
    export ABUSEIPDB_KEY='your_abuseipdb_key_here'


- - - 

# Module Guide

**Module 1: Image Geolocation (EXIF & Tactical Analysis)**

**Purpose**: Extract GPS coordinates and metadata from images to determine where a photo was taken and with what device.

**How to Use**:

1. Select option 1 from the main menu

2. Provide the path to an image file (JPEG, PNG, etc.)

3. The tool extracts EXIF data including GPS coordinates if available

4. If coordinates are found, it provides a Google Maps link

**Example**:

**Enter path to the target image**: /home/user/suspect_photo.jpg

  - Coordinates extracted:
  - Latitude: 40.7589
  - Longitude: -73.9851

  - Locate on Google Maps: https://www.google.com/maps/search/?api=1&query=40.7589,-73.9851

**Practical Applications**:

- Verifying location claims in investigations

- Geotagging evidence for legal cases

- Identifying camera sources in media analysis
  
- - - 

**Module 2: Social Media Deep Dive**

**Purpose**: Cross-platform username investigation across 30+ social media platforms.

**How to Use**:

1. Select option 2 from the main menu

2. Enter a username to investigate

3. Tool generates links to check that username across all platforms

**Example**:

**Enter target username**: john_doe123

[*] Profiles found for john_doe123:
FACEBOOK        --> https://facebook.com/john_doe123
TWITTER (X)     --> https://twitter.com/john_doe123
INSTAGRAM       --> https://instagram.com/john_doe123
... (30+ platforms)

**Practical Applications**:

- Digital footprint analysis
- Person of interest investigation
- Brand monitoring

- - - 

**Module 3: Email Breach & Source Sweep**

**Purpose**: Check email addresses in breach databases and public pastes.

**How to Use**:

1. Select option 3 from the main menu

2. Enter target email address

3. Tool checks HaveIBeenPwned database and scans paste sites
   
**Example**:

**Target email**: johndoe@example.com

[+] 3 breaches detected for johndoe@example.com:

  - LinkedIn on 2012-05-05
  - Adobe on 2013-10-04
  - MySpace on 2008-06-11

--- Scanning Pastebin Public Pastes ---

[i] Checking recent pastes for presence of email...
[+] Found 2 pastes containing target email:
  > https://pastebin.com/aBcDeFg1
  > https://pastebin.com/hIjKlMn2

**Practical Applications**:

- Account compromise assessment
- Digital footprint analysis
- Threat intelligence gathering

- - - 

**Module 4: Email Verification & Intel**

**Purpose**: Validate email addresses and gather associated intelligence.

**How to Use**:

1. Select option 4 from the main menu

2. Enter email address for verification

3. Uses Hunter.io API to verify email

4. validity and find associated data

**Example**:

**Enter email for verification***: johndoe@example.com

--- Hunter.io API Query ---
Status   : valid
Result   : deliverable
Score    : 78
Disposable: No
MX Records: Present
SMTP Check: True
Source Domains (Top 3):
  - example.com (https://example.com/contact)
  - company.com (https://company.com/about)

**Practical Applications**:

- Lead validation
- Fraud prevention
- Identity verification

- - - 

**Module 5: Domain Intelligence**

**Purpose**: Comprehensive domain investigation including WHOIS, DNS, and subdomains.

**How to Use**:

1. Select option 5 from the main menu

2. Enter domain name or URL

3. Tool performs WHOIS lookup, DNS
enumeration, and subdomain discovery

**Example**:

**Give domain or URL: example.com**

--- WHOIS Information ---
Registrar    : GoDaddy.com, LLC
Created      : 1995-08-15 04:00:00
Domain Age   : 10235 days
Expires      : 2024-08-14 04:00:00

--- DNS Records (A / MX / NS) ---
A Records:
  - 93.184.216.34

[*] Harvesting subdomains from crt.sh...
[+] Subdomain haul: 15 found:
 - www.example.com
 - mail.example.com
 - blog.example.com
 - shop.example.com

**Practical Applications**:

- Attack surface mapping
- Brand protection
- Infrastructure assessment

- - - 

**Module 6: Metadata Extraction**

**Purpose**: Extract hidden metadata from files.

**How to Use**:

1. Select option 6 from the main menu

2. Provide path to any file (images, documents, etc.)

3. Tool extracts EXIF and file system metadata

**Example**:

Target file path: document.pdf

EXIF Metadata:
Image Make                    : Canon
Image Model                   : Canon EOS 5D Mark IV
Image DateTime                : 2023:05:15 14:30:22
GPS Latitude                  : 40.7589
GPS Longitude                 : -73.9851
Software                      : Adobe Photoshop 2023

**Practical Applications**:

- Document verification
- Source identification
- Forensic analysis

- - - 

**Module 7: Google Dorking**

**Purpose**: Advanced Google search techniques to find hidden information.

**How to Use**:

1. Select option 7 from the main menu

2. Enter Google dork query or use provided examples

3. Tool opens Google search with the specialized query

**Example**:

Your dork query: site:example.com filetype:pdf "confidential"
Deploying search...
[Opens Google with: site:example.com filetype:pdf "confidential"]

**Practical Applications**:

Vulnerability discovery
Information gathering
Competitive intelligence

- - - 

**Module 8: Instagram Recon**

**Purpose**: Instagram profile investigation.

**How to Use**:

1. Select option 8 from the main menu

2. Enter Instagram username

3. Tool scrapes available public information

**Example**:

**Enter Instagram username**: davidbombal

Profile Title: David Bombal (@davidbombal) • Instagram photos and videos
Description: 447K Followers, 130 Following, 4,475 Posts - David Bombal (@davidbombal) on Instagram: "Twitter: @davidbombal YouTube: https://www.youtube.com/davidbombal"
Twitter: @davidbombal
YouTube: https://www.youtube.com/davidbombal
Profile URL: https://www.instagram.com/davidbombal/
Status: Profile exists

- - - 

**Practical Applications**:

- Social media investigation
- Identity verification
- Influence mapping

- - - 

**Module 9: Port Scan**

**Purpose**: Network reconnaissance through port scanning.

**How to Use**:

1. Select option 9 from the main menu

2. Enter IP address or domain name

3. Tool scans common ports for availability

**Example**:

**Enter target IP or domain**: example.com

Scanning example.com (93.184.216.34)...
[+] Port 80 (http) is open
[+] Port 443 (https) is open
[-] Port 21 (ftp) is closed
[-] Port 22 (ssh) is closed

Open ports found:
Port 80 (http)
Port 443 (https)


**Practical Applications**:

- Network security assessment
- Service discovery
- Attack surface analysis

- - - 

**Module 10: GitHub Recon**

**Purpose**: Gather intelligence on GitHub users and their activities.

**How to Use**:

1. Select option 10 from the main menu

2. Enter GitHub username

3. Tool retrieves profile information and statistics

**Example**:

**Enter GitHub username**: torvalds

GitHub User Information:
Username: torvalds
Name: Linus Torvalds
Bio: N/A
Public Repos: 7
Public Gists: 0
Followers: 175000
Following: 0
Created At: 2011-09-25T18:44:36Z
URL: https://github.com/torvalds
Location: Portland, OR
Company: Linux Foundation


**Practical Applications**:

- Developer background checks
- Code repository analysis
- Talent acquisition research


- - - 

**Module 11: Website Metadata & Entity Scraper**

**Purpose**: Extract metadata and entities from multiple websites.

**How to Use**:

1. Create a file called urls.txt with one URL per line

2. Select option 11 from the main menu

3. Tool processes all URLs and extracts metadata, emails, and entities

**Example urls.txt**:

https://example.com
https://example.org
https://example.net

**Output**:

[SCRAPING] https://example.com
Title        : Example Domain
Meta Tags    : 5 found
Emails       : 2 found
Persons      : 3 found
Locations    : 1 found

**Practical Applications**:

- Competitive intelligence
- Contact information gathering
- Content analysis

- - -

**Module 12: Phone Number Hack-Recon**

**Purpose**: Validate phone numbers and gather associated intelligence.

**How to Use**:

1. Select option 12 from the main menu

2. Enter full phone number with country code

3. Tool validates and provides carrier/location information

**Example**:

**Enter full phone number**: +14155551234

Valid Number  : True
Intl Format   : +1 415-555-1234
Nat Format    : (415) 555-1234
Geo Location  : California, United States
Carrier       : Verizon Wireless
Type          : Mobile

--- Suggested Google Dorks ---
  "+14155551234" OR "(415) 555-1234"
  "14155551234" OR "4155551234"

**Practical Applications**:

- Phone number validation
- Carrier identification
- Investigation lead generation

- - - 

**Module 13: Reverse Image Missions**

**Purpose**: Deploy reverse image searches across multiple engines.

**How to Use**:

1. Select option 13 from the main menu

2. Tool displays multiple reverse image search engines

3. Manually visit each engine to upload your image
   
**Example**:

Google Images         >> https://images.google.com/
TinEye                >> https://tineye.com/
Yandex                >> https://yandex.com/images/
Bing Visual           >> https://www.bing.com/images/discover
Baidu                 >> https://image.baidu.com/
SauceNAO              >> https://saucenao.com/
ImgOps                >> https://imgops.com/

**Practical Applications**:

- Image source identification
- Fake profile detection
- Copyright investigation

- - - 

**Module 14: GEOINT OPS (Satellite & Map Assault)**

**Purpose**: Geospatial intelligence through satellite and map analysis.

**How to Use**:

1. Select option 14 from the main menu

2. Enter coordinates (lat,lon) or location name

3. Tool opens Google Satellite and OpenStreetMap views

**Example**:

**Enter coords (lat,lon) or location name**: 40.7589,-73.9851

[+] Valid coordinate input: 40.7589, -73.9851
Opening Google Satellite Map...
Opening OpenStreetMap view...

**Practical Applications**:

- Location verification
- Area analysis
- Strategic planning

- - - 

**Module 15: Wayback Machine Domination**

**Purpose**: Access historical versions of websites.

**How to Use**:

1. Select option 15 from the main menu

2. Enter URL with http/https

3. Tool retrieves archived snapshots

**Example**:

**Enter URL (include http/https): https**://example.com

[+] 1247 archives located. Listing top 10:
 [1] http://web.archive.org/web/20230115000000/https://example.com (Captured: 2023-01-15 00:00:00, HTTP 200)
 [2] http://web.archive.org/web/20221201000000/https://example.com (Captured: 2022-12-01 00:00:00, HTTP 200)

**Practical Applications**:

- Historical website analysis
- Content change tracking
- Evidence preservation

- - - 

**Module 16: IP GeoBlacklist Recon**

**Purpose£*: IP address investigation and reputation checking.

**How to Use**:

1. Select option 16 from the main menu

2. Enter IP address

3. Tool provides geolocation and abuse reports

**Example**:

**Target IP**: 8.8.8.8

IP         : 8.8.8.8
Hostname   : dns.google
City       : Mountain View
Region     : California
Country    : US
Loc        : 37.4056,-122.0775
Org        : AS15169 Google LLC
Postal     : 94043
Timezone   : America/Los_Angeles

--- AbuseIPDB Report ---
Abuse Confidence Score : 0%
Total Reports (90d)    : 0
Status                 : No significant abuse reports

£*Practical Applications**:

- IP reputation checking
- Threat intelligence
- Network monitoring

- - - 

**Module 17: Threat Intel Feeds**

**Purpose**: Access real-time threat intelligence sources.

**How to Use**:

1. Select option 17 from the main menu

2. Tool displays available threat intelligence sources

3. Choose to open all in browser or manually visit

**Example**:

**Available Threat Intelligence Sources**:

AlienVault OTX                          : https://otx.alienvault.com/
CISA Known Exploited Vulnerabilities    : https://www.cisa.gov/known-exploited-vulnerabilities-catalog
ThreatFox IOC Database                  : https://threatfox.abuse.ch/
MalwareBazaar                           : https://bazaar.abuse.ch/

Open all in browser? (y/N): y
[Opens all threat intelligence sources]

**Practical Applications**:

- Threat monitoring
- Vulnerability assessment
- Security research

- - - 


**Module 18: REDDIT RECON (Subreddit & User Analysis)**

**Purpose**: Comprehensive Reddit intelligence gathering.

**How to Use**:

1. Select option 18 from the main menu

2. Choose analysis type (User, Subreddit, or Search)

3. Follow prompts for specific investigation

**Example**:

**Select analysis type (1-3)**: 2
Enter subreddit name: cybersecurity

[*] Analyzing subreddit: r/cybersecurity
[*] Fetching subreddit information...
✓ Subreddit information retrieved
   Name: r/cybersecurity
   Subscribers: 1,250,000
   Created: 2010-05-15 14:22:10

=== SUBREDDIT SUMMARY ===
Subreddit: r/cybersecurity
Subscribers: 1,250,000
Active Users: 15,250
Description: A community for cybersecurity professionals and enthusiasts to share news...
Hot Posts Analyzed: 50
Avg Hot Score: 245.32
Avg Hot Comments: 42.15

**Practical Applications**:

- Community analysis
- Trend monitoring
- Influence mapping

- - - 

**Module 19: REPORT BUG**

**Purpose**: Provide feedback and report issues.

**How to Use**:

1. Select option 19 from the main menu

2. Follow guidelines for reporting issues

3. Visit GitHub issues page if needed

**Practical Applications**:

- Tool improvement
- Bug reporting
- Feature requests

- - - 

**Module 20: EXIT THE MATRIX**

+*Purpose**: Cleanly exit the application.

**How to Use**:

1. Select option 20 from the main menu

2. Tool displays exit message and closes

**Example**:

- Exiting DARKNET OSINT SUITE. Stay concealed, operator.

- - - 

# API Setup

**Required APIs for Full Functionality**:

**1. GitHub Token** (Optional but recommended)

**Purpose**: Higher rate limits for GitHub reconnaissance

**Get it**: https://github.com/settings/tokens

**Scopes**: repo, read:org, read:user, user:email


**2. Have I Been Pwned (Recommended)**

**Purpose**: Email breach checking

**Get it**: https://haveibeenpwned.com/API/Key

**Free tier**: 1 request/1.5 seconds


**3. AbuseIPDB (Optional)**

**Purpose**: IP reputation checking

**Get it**: https://www.abuseipdb.com/api

**Free tier**: 1,000 requests/day


# Setup Commands:


# Linux/macOS

    export GITHUB_TOKEN='your_token_here'
    export HIBP_API_KEY='your_key_here'
    export ABUSEIPDB_KEY='your_key_here'


- - - 

# Ethical Considerations

#### Legal Compliance:

- Use only on systems you own or have explicit permission to test

- Comply with local laws and regulations

- Respect terms of service of online platforms

- Use for legitimate security research only
  
#### Prohibited Activities:

- Unauthorized access to systems

- Harassment or stalking individuals

- Commercial exploitation without permission

- Data scraping violating ToS

- Any illegal activities

#### Responsible Disclosure:

- Report vulnerabilities to affected parties
  
- Allow reasonable time for fixes
  
- Do not expose sensitive data publicly
  
- Follow responsible disclosure guidelines

#### Bug Reports & Contributions

**Reporting Issues**:

1. Check existing issues on GitHub
  
2. Create detailed bug report including:
   
- OS and Python version
  
- Exact error messages
  
- Steps to reproduce
  
- Expected vs actual behavior
  
#### Contribution Guidelines:

1. Fork the repository

2. Create feature branch

3. Follow existing code style

4. Add tests for new features

5. Submit pull request with description

#### Feature Requests:

- Suggest new modules or improvements

- Provide use cases and examples

- Consider implementation complexity

#### Support

**Documentation**:

- Video tutorials on YouTube…

- Example usage scenarios…
Community:

**Discord community**:…
GitHub Discussions for questions

**Troubleshooting**:

- Check all dependencies are installed
  
- Verify API keys are correctly set

- Ensure sufficient permissions

- Check internet connectivity

- - - 

**Disclaimer**: This tool is for educational and authorized security testing purposes only. I am not responsible for misuse of this tool. Always obtain proper authorization before conducting any security assessments.

