# Note

- [Commands](#Commands)
  - [Information Gathering](#Information-Gathering)
    - [Nmap](#Nmap)
  - [Web Application Enumeration](#Web-Application-Enumeration)
    - [gobuster](#gobuster)
    - [ffuf](#ffuf)
    - [dirsearch](#dirsearch)

## Commands

### Information Gathering 

#### Nmap
```
sudo nmap -A -T4 <ip> -oN nmap.txt
```

### Web Application Enumeration

#### gobuster
```
gobuster dir -u <url> -w <wordlists> -o gobuster.txt 
gobuster dir -u <url> -w <wordlists> -x php,html,txt 
gobuster vhost -u <url> --append-domain -w <wordlists> 
```
#### ffuf
```
ffuf -u http://example.com/FUZZ -w <wordlists>
//subdomain
ffuf -u <url> -w <wordlists> -H "Host:FUZZ.example.com" -mc 200
ffuf -u <url> -w <wordlists> -H "Host:FUZZ.example.com" -ac
```
#### dirsearch
```
dirsearch -u <url> -t 50 -i 200
```


