# Reconnaissance Guide

## 1. Finding Subdomains  
Techniques: Brute Force, Passive, Permutation  
Tools: `Subfinder`, `Amass`, `Assetfinder`, `crt.sh`, `Puredns`, `ffuf`, `gotator`, `oneforall`, `frogy`, `sudomy`, `chaos`, and Google dorking.

## 2. Extract Alive and Unique Subdomains from the Subdomain List  
Tools: `Httpx`, `httprobe`, and Unix commands `sort` & `uniq` for filtering unique subdomains.

## 3. Take Screenshots of Each Alive Subdomain  
Tools: `Aquatone`, `Eyewitness`

## 4. Crawl URLs of Alive Subdomains Passively and Actively  
Tools: `Waymore`, `Gau`, `Waybackurls`, `Gauplus`, `katana`, `hackcrawler`, and many more for active crawling.

## 5. Identify Potentially Vulnerable Endpoints (XSS, IDOR, SQLi, LFI, SSRF, etc.) from URL Lists  
Tools: `Gf`, with custom `Gf Patterns`.

## 6. Use Various Google or GitHub Dorks to Search for Sensitive Information  
Notes: Using the Google Hacking Database and searching specific keywords can reveal extensive lists (e.g., SQLi Google dork lists).

## 7. Find More Sensitive Information About the Target  
Sources/Tools:  
- `Shodan` (`shodanx`) for mapping internet-connected devices and systems.  
- `Censys` for attack surface discovery.  
- `app.netlas.io` for attack surface analysis.  
- `fullhunt` for attack surface enumeration.  
- `grep.app`  
- `SecurityTrails`  
- `zoomeye`, `binaryedge`, `fofa`

## 8. Gather DNS Information, WHOIS Records, Network Data, and More  
Tools: `dig`, `nslookup`, `whois`, `bgp.he.net`, `viewdns.info`, `icanlookup`, `robtex`, `sitereport.netcraft.com`, `dnsx`, and others.

## 9. Identify Web Technologies and Security Headers  
Tools: `Wappalyzer`, `BuiltWith`, `Netcraft`, [securityheaders.com](https://securityheaders.com/), and more.

## 10. JavaScript File Enumeration  
Notes: JavaScript files often contain sensitive information such as API keys, default credentials, and architectural insights, making them highly valuable.  
Tools: `getjs`, `subjs`, `Cariddi`, `katana`, `linkfinder`, and others.

## 11. Port Scanning  
Notes: Port scanning is critical for web pentesting and bug hunting to identify running services and their versions on target hosts. This helps find vulnerable services beyond standard web ports (80, 443). For example, discovering open SSH/FTP services can lead to further exploitation or brute-forcing attacks.  
Approach:  
- Use `Naabu` to scan multiple subdomains for open ports, then perform detailed scans with `nmap`.  
- For single domain scans, use various `nmap` scanning techniques.  
- For passive port scanning, use `smap`.  

Tools: `naabu`, `nmap`, `masscan`, `angryscanner`, `smap`, and others.

## 12. Content Discovery (Directory Brute-Forcing / Fuzzing)  
Notes: This process uncovers sensitive endpoints or directories by fuzzing subdomains or root domains, helping identify hidden files or nested directories.  
Tools: `ffuf`, `dirsearch`, `dirb`, `dirbuster`, `gobuster`, etc.

## 13. Finding Parameters  
Notes: Parameters are common locations for injection vulnerabilities. After completing steps 4 and 5, many parameters can be discovered passively, but active parameter discovery is essential to find more.  
Tools: `paramspider`, `arjun`, `ffuf`, and others.
