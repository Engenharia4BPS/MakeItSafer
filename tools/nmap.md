## **Nmap**
*Nmap é um utilitário de descoberta de rede e varredura de portas que permite a identificação e impressão digital de dispositivos em redes, usando um grande número de sintaxes para auxiliar na detecção de serviços e portas abertas.*

**Exemplos de uso:**
  1. Saber quais os endereços IP "ativos" numa determinada rede: 
  ```nmap -sP 192.168.100.0/24```
  2. Saber quais os portas abertas de uma máquina: `nmap -sT 192.168.100.1`
  3. Saber se um porta específico está aberto: `nmap -p 80 192.168.100.1`
  4. Saber o sistema operacional de uma determinada máquina: `nmap -o 192.168.100.1`
  5. Inventário de todas as máquinas da rede: `nmap -sS -O -T3 -oA invent 192.168.100.0/24`

**Instalar no OSX**
```
brew install nmap
```
**Referencias**
- :bookmark:  https://nmap.org
- :bookmark:  https://nmap.org/man/pt_BR/index.html
- :bookmark:  https://pplware.sapo.pt/tutoriais/nmap-5-exemplos-de-como-usar-este-poderoso-scanner-de-rede/


