## **Nmap**
*Nmap is a network discovery and port-scanning utility that allows for the identification and fingerprinting of devices across networks, using a large number of syntaxes to aid in detecting services and open ports.*

**Exemplos de uso:**
  1. Saber quais os endereços IP "ativos" numa determinada rede: `nmap -sP 192.168.100.0/24`
  2. Saber quais os portas abertas de uma máquina: `nmap -sT 192.168.100.1`
  3. Saber se um porta específico está aberto: `nmap -p 80 192.168.100.1`
  4. Saber o sistema operacional de uma determinada máquina: `nmap -o 192.168.100.1`
  5. Inventário de todas as máquinas da rede: `nmap -sS -O -T3 -oA invent 192.168.100.0/24`

**Instalar no OSX**
```
brew install nmap
```
**Referencias**
###### - :bookmark:  https://nmap.org
- :bookmark:  https://nmap.org/man/pt_BR/index.html
- :bookmark:  https://pplware.sapo.pt/tutoriais/nmap-5-exemplos-de-como-usar-este-poderoso-scanner-de-rede/


## **Nikto**
###### :bookmark:  https://github.com/sullo/nikto

*Nikto is a vulnerability scanner used to inspect web server configurations to detect thousands of potential issues, including misconfigurations, out-of-date patches, and version-specific problems that could otherwise allow attackers to gain unauthorized access.*

```
brew install nikto
```

## **SQLmap**
###### :bookmark:  https://sqlmap.org

*SQLmap is an open source application that allows for the detection and exploitation of SQL injection vulnerabilities in database servers using structured query language. The tool can also be used to automate attacks, as well.*

```
brew install sqlmap
```

## **Zed Attack Proxy (ZAP)**
  ###### :bookmark:  https://www.zaproxy.org

*Another open source security scanner, OWASP's ZAP tool is used to test a web application's security though a multitude of tools, including a proxy server to capture encrypted and unencrypted traffic, Fuzzer, and much more.*

```
brew install caskroom/cask/brew-caskbrew cask install owasp-zap
```

## **Recon-ng**
  ###### :bookmark:  https://github.com/lanmaster53/recon-ng

*This reconnaissance framework is designed to conduct open source information gathering that leverages community-supported modules that provide additional resources to search, such as social media networks, using powerful (and secure) API tools. The data obtained can then be leveraged in other complementary tools to test vulnerabilities or exploit them.*

```
brew install recon-ng
```

## **The Harvester**
- :bookmark:  https://github.com/laramies/theHarvester
- :bookmark:  https://tools.kali.org/information-gathering/theharvester

*The Harvester is an information-gathering application that serves to use publicly available information and databases to obtain information, including domains, 
hostnames, emails, employee directory info--anything that establishes putting together a holistic picture of the target.*

```
brew install theharvester
```

## **TestSSL**
###### :bookmark:  

*This scanner works as both an information-gathering tool that assess which security protocols and ciphers are being used on a server, including their configurations and which ports the service(s) are running on.*

```
brew install testssl
```

## **Empire**
###### :bookmark:  

*A post-exploitation framework, this tool leverages PowerShell to make connections and create/run scripts on remote machines within memory while evading network detection, making this capable of running modules and cmdlets remotely under the radar.*

```
brew install empire
```

## **John the Ripper**
###### :bookmark:  

*This password cracking utility is part of any security tester's toolkit. It's designed to detect weak passwords in many different platforms, including Windows, Linux, and macOS among a dozen others – using password lists (dictionary attack) or a fast, variable speed attempts to crack more complex passwords (brute force attack).*

```
brew install john
```

## **Bettercap**
###### :bookmark:  

*Often referred to as a Swiss Army Knife for security software, Bettercap offers a framework of security testing that provides myriad tools for testing wireless networks (both Wi-Fi and Bluetooth), network sniffing, proxies, and spoofers for man-in-the-middle attacks.*

```
brew install bettercap
```
