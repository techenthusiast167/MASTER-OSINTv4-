# MASTER-OSINTv4

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
- **https://gist.github.com/techenthusiast167/45d802b026830981106af3b017c2e36d** v4
- **https://gist.github.com/techenthusiast167/543719b32253663ed5b9d406ba8affef** v4.0
  
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

**1. Image Geolocation**

- **Purpose**: Extract GPS metadata from images

#### Example: Analyze travel photos for location data

#### Input: path/to/image.jpg

#### Output: Coordinates and Google Maps link ( if any )

- - - 

**2. Social Media Deep Dive**

- **Purpose**: Find profiles across 30+ platforms


#### Example: Investigate username "johnsmith"

#### Input: username

#### Output: List of profile URLs across social media

- - - 

**3. Email Breach & Source Sweep**

- **Purpose**: Check email breaches and Pastebin exposure

#### Example: Verify email security

#### Input: email@example.com  

#### Output: Breach history and exposed instances

- - - 

**4. Email Verification & Intel**

- **Purpose**: Validate email existence and gather intelligence


#### Example: Verify professional email

#### Input: name@company.com

#### Output: Validation results and associated domains

- - - 

**5. Domain Intelligence**

- **Purpose**: Comprehensive domain analysis


#### Example: Investigate suspicious domain

#### Input: example.com

#### Output: WHOIS data, DNS records, subdomains

- - - 

**6. Metadata Extraction**

- **Purpose**: Extract EXIF and file metadata


#### Example: Analyze document metadata

##### Input: document.pdf

#### Output: Creation dates, author, software used

- - - 

**7. Google Dorking**

- **Purpose**: Advanced search techniques


#### Example: Find exposed documents

#### Input: "site:company.com filetype:pdf"

#### Output: Google search results

- - - 

**8. Instagram Recon**

- **Purpose**: Profile investigation


#### Example: Analyze public profile

#### Input: username

#### Output: Profile information and statistics

- - - 

**9. Port Scan**

- **Purpose**: Network reconnaissance


#### Example: Check server security

#### Input: example.com OR 192.168.1.1

#### Output: Open ports and services

- - - 

**10. GitHub Recon**

- **Purpose**: Developer intelligence


#### Example: Research developer activity

#### Input: github_username

#### Output: Profile info, repositories, activity

- - - 

**11. Website Metadata Scraper**

- **Purpose**: Extract website data


#### Example: Analyze multiple websites

#### Input: urls.txt file with target URLs

#### Output: Metadata, emails, entities in JSON/CSV

- - - 

**12. Phone Number Recon**

- **Purpose**: Phone intelligence


#### Example: Verify phone number

#### Input: +1234567890

#### Output: Carrier, location, validation

- - - 

**13. Reverse Image Search**

- **Purpose**: Image investigation


#### Example: Find image sources

#### Input: (Opens multiple search engines)

#### Output: Browser opens with search results

- - - 

**14. Geospatial Intelligence**

- **Purpose**: Location analysis


#### Example: Map coordinates

#### Input: 40.7128,-74.0060 OR "New York City"

#### Output: Satellite and map views

- - - 

**15. Wayback Machine**

- **Purpose**: Historical website data


#### Example: Archive research

#### Input: https://example.com

#### Output: Historical snapshots and changes

- - - 

**16. IP Blacklist Check**

- **Purpose**: IP reputation analysis


#### Example: Check suspicious IP

#### Input: 192.168.1.100

#### Output: Geolocation and abuse reports

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

