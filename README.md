<p align="center">
<img src="https://img.shields.io/badge/Python-3-brightgreen.svg?style=plastic">
<img src="https://img.shields.io/badge/OSINT-red.svg?style=plastic">
<img src="https://img.shields.io/badge/Web-red.svg?style=plastic">
</p>

<p align="center">
  <a href="https://twitter.com/krishnanandivelugu"><b>Twitter</b></a>
  <span> - </span>
  <a href="https://t.me/kriShna"><b>Telegram</b></a>
  <span> - </span>
  
</p>

infoget is an **automatic web reconnaissance** tool written in python. infoget is to provide an **overview** of the target in a **short** amount of time while maintaining the **accuracy** of results. Instead of executing **several tools** one after another infoget can provide similar results keeping dependencies

## Available In

<p align="center">
  <a href="https://www.kali.org/news/kali-linux-2020-4-release/">
    <img width="150px" hspace="10px" src="https://i.imgur.com/yQRrCtC.png" alt="kali linux infoget">

</p>

## Featured

### Python For OSINT

## Features

infoget provides detailed information such as :

* Header Information

* Whois

* SSL Certificate Information

* Crawler
  * html
    * CSS
    * Javascripts
    * Internal Links
    * External Links
    * Images
  * robots
  * sitemaps
  * Links inside Javascripts
  * Links from Wayback Machine from Last 1 Year

* DNS Enumeration
  * A, AAAA, ANY, CNAME, MX, NS, SOA, TXT Records
  * DMARC Records

* Subdomain Enumeration
  * Data Sources
    * BuffOver
    * crt.sh
    * ThreatCrowd
    * AnubisDB
    * ThreatMiner
    * Facebook Certificate Transparency API
      * Auth Token is Required for this source, read Configuration below
    * VirusTotal
    	* API Key is Required
    * CertSpotter

* Traceroute
  * Protocols
    * UDP
    * TCP
    * ICMP

* Directory Searching
  * Support for File Extensions
  * Directories from Wayback Machine from Last 1 Year

* Port Scan
  * Fast
  * Top 1000 Ports
  * Open Ports with Standard Services

* Export
  * Formats
    * txt
    * xml
    * csv

## Tested on

* Kali Linux


> infoget is a tool for **Pentesters** and it's designed for **Linux** based Operating Systems, other platforms like **Windows** and **Termux** are **NOT** supported.

## Installation

### Kali Linux

```
sudo apt install infoget
git clone https://github.com/anonymous-7339/infoget.git
cd FinalRecon
pip3 install -r requirements.txt
```
### Other Linux

```bash
git clone https://github.com/anonymous-7339/infoget.git
cd FinalRecon
pip3 install -r requirements.txt
```
## Usage

python3 infoget.py -h

usage: infoget.py [-h] [--headers] [--sslinfo] [--whois] [--crawl] [--dns] [--sub]
                     [--trace] [--dir] [--ps] [--full] [-t T] [-T T] [-w W] [-r] [-s]
                     [-sp SP] [-d D] [-e E] [-m M] [-p P] [-tt TT] [-o O]
                     url
infoget - The Web Recon Tool You Will Need | krishna_7339_

positional arguments:
  url         Target URL

optional arguments:
  -h, --help  show this help message and exit
  --headers   Header Information
  --sslinfo   SSL Certificate Information
  --whois     Whois Lookup
  --crawl     Crawl Target
  --dns       DNS Enumeration
  --sub       Sub-Domain Enumeration
  --trace     Traceroute
  --dir       Directory Search
  --ps        Fast Port Scan
  --full      Full Recon

Extra Options:
  -t T        Number of Threads [ Default : 30 ]
  -T T        Request Timeout [ Default : 30.0 ]
  -w W        Path to Wordlist [ Default : wordlists/dirb_common.txt ]
  -r          Allow Redirect [ Default : False ]
  -s          Toggle SSL Verification [ Default : True ]
  -sp SP      Specify SSL Port [ Default : 443 ]
  -d D        Custom DNS Servers [ Default : 1.1.1.1 ]
  -e E        File Extensions [ Example : txt, xml, php ]
  -m M        Traceroute Mode [ Default : UDP ] [ Available : TCP, ICMP ]
  -p P        Port for Traceroute [ Default : 80 / 33434 ]
  -tt TT      Traceroute Timeout [ Default : 1.0 ]
  -o O        Export Output [ Default : txt ] [ Available : xml, csv ]
```

```bash
# Check headers

python3 infoget.py --headers <url>

# Check ssl Certificate

python3 infoget.py --sslinfo <url>

# Check whois Information

python3 infoget.py --whois <url>

# Crawl Target

python3 infoget.py --crawl <url>

# Directory Searching

python3 infoget.py --dir <url> -e txt,php -w /path/to/wordlist

# full scan

python3 infoget.py --full <url>
```

