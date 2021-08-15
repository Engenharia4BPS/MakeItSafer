## **Nmap**
*Nmap é um utilitário de descoberta de rede e varredura de portas que permite a identificação e impressão digital de dispositivos em redes, usando um grande número de sintaxes para auxiliar na detecção de serviços e portas abertas.*

**Exemplos de uso:**
1. Saber quais os endereços IP "ativos" numa determinada rede: 
  - -sP (Scan usando Ping)
  - *Esta opção diz ao Nmap para somente executar um scan usando o ping (descoberta de hosts), e então mostrar os hosts disponíveis que responderam ao scan. Nenhum teste adicional (tais como escaneamento de portas e deteção de SO) é executado.*

  **Comando**
  ```
  nmap -sP 192.168.100.0/24
  ```
-----------------------------------  
2. Saber quais os portas abertas de uma máquina: 
  - -sT (scan TCP connect)
  - *O scan TCP connect é o scan padrão do TCP quando o scan SYN não é uma opção. Esse é o caso quando o usuário não tem privilégios para criar pacotes em estado bruto ou escanear redes IPv6. Ao invés de criar pacotes em estado bruto como a maioria dos outros tipos de scan fazem, o Nmap pede ao sistema operacional para estabelecer uma conexão com a máquina e porta alvos enviando uma chamada de sistema connect(). Essa é a mesma chamada de alto nível que os navegadores da web, clientes P2P, e a maioria das outras aplicações para rede utilizam para estabelecer uma conexão. É parte da interface de programação conhecida como API de Sockets de Berkeley. Ao invés de ler as respostas em pacotes em estado bruto diretamente dos fios, o Nmap utiliza esta API para obter informações do estado de cada tentativa de conexão.*

  **Comando:**
  ```
  nmap -sT 192.168.100.1
  ```

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


