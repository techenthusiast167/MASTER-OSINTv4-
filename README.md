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

