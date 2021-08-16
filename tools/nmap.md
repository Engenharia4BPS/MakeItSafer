## **Nmap**
*Nmap é um utilitário de descoberta de rede e varredura de portas que permite a identificação e impressão digital de dispositivos em redes, usando um grande número de sintaxes para auxiliar na detecção de serviços e portas abertas.*

**Exemplos de uso:**

-----------------------------------

**1. Saber quais os endereços IP "ativos" numa determinada rede:**
  - -sP (Scan usando Ping)
  - *Esta opcao diz ao Nmap para somente executar um scan usando o ping (descoberta de hosts), e entao mostrar os hosts disponiveis que responderam ao scan. Nenhum teste adicional (tais como escaneamento de portas e detecao de SO) e executado.*

  **Comando**
  ```
  nmap -sP 192.168.100.0/24
  ```

-----------------------------------

**2. Saber quais os portas abertas de uma máquina:**
  - -sT (scan TCP connect)
  - *O scan TCP connect e o scan padrao do TCP quando o scan SYN nao e uma opcao. Esse e o caso quando o usuario nao tem privilegios para criar pacotes em estado bruto ou escanear redes IPv6. Ao inves de criar pacotes em estado bruto como a maioria dos outros tipos de scan fazem, o Nmap pede ao sistema operacional para estabelecer uma conexao com a maquina e porta alvos enviando uma chamada de sistema connect(). Essa e a mesma chamada de alto nivel que os navegadores da web, clientes P2P, e a maioria das outras aplicacoes para rede utilizam para estabelecer uma conexao. E parte da interface de programacao conhecida como API de Sockets de Berkeley. Ao inves de ler as respostas em pacotes em estado bruto diretamente dos fios, o Nmap utiliza esta API para obter informacoes do estado de cada tentativa de conexao.*

  **Comando:**
  ```
  nmap -sT 192.168.100.1
  ```

-----------------------------------

**3. Saber se um porta especifica está aberta:**
  - -p <faixa de portas> (Escaneia apenas as portas especificadas)
  - *Esta opcao especifica quais portas que voce deseja escanear e prevalece sobre o padrao. Numeros de portas individuais sao suportadas, bem como as faixas separadas por um hifen (p.ex.: 1-1023). Os valores iniciais e/ou finais da faixa podem ser omitidos, o que faz com que o Nmap use 1 e 65535, respectivamente. Por exemplo, o argumento -p U:53,111,137,T:21-25,80,139,8080 escanearia as portas UDP 53, 111 e 137, bem como as portas TCP listadas.*
  
  **Comando:**
  ```
  nmap -p 80 192.168.100.1
  ```
  
-----------------------------------

**4. Saber o sistema operacional de uma determinada maquina:**
  - -O (Habilita a deteccao de SO)
  - *Habilita a detecao de SO, como discutido acima. Alternativamente, voce pode usar -A para habilitar tanto a deteccao de SO quanto a deteccao de versao.*

**Comando:**
````
nmap -o 192.168.100.1
```

-----------------------------------

**5. Inventario de todas as maquinas da rede:**
  - -O (Habilita a deteccao de SO)
  - -T <Paranoid|Sneaky|Polite|Normal|Aggressive|Insane> (Estabelece um padrão de temporização)
  - -oA <nome-base> (Saída para todos os formato)

**Comando:**
````
nmap -sS -O -T3 -oA invent 192.168.100.0/24
```

-----------------------------------

**Instalar no OSX**
```
brew install nmap
```
**Referencias**
- :bookmark:  https://nmap.org
- :bookmark:  https://nmap.org/man/pt_BR/index.html
- :bookmark:  https://pplware.sapo.pt/tutoriais/nmap-5-exemplos-de-como-usar-este-poderoso-scanner-de-rede/


