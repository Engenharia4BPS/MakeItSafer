## **Nikto**
*Nikto is a vulnerability scanner used to inspect web server configurations to detect thousands of potential issues, including misconfigurations, out-of-date patches, and version-specific problems that could otherwise allow attackers to gain unauthorized access.*

**Exemplos de uso:**
  1. Varredura de um site na porta padrão 80: `nikto -h www.webbsite.com`
  2. Varredura de um site na porta especifica: `nikto -h www.webbsite.com -p 443`
  3. Varredura de um site em um grupo de portas: `nikto -h www.webbsite.com -p 80,88,443`

**Instalar no OSX**
```
brew install nikto
```

**Referencias**
- :bookmark:  https://cirt.net/Nikto2
- :bookmark:  https://github.com/sullo/nikto
- :bookmark:  https://www.nanoshots.com.br/2015/09/nikto-um-poderoso-scanner-de-servidores.html



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
