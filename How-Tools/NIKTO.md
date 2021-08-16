# **NIKTO**
Nikto e um scanner de vulnerabilidades de software livre acessado por CLI, usado para escanear servidores web em busca de arquivos perigosos, programas desatualizados e outros problemas. E capaz de fazer tanto analises genericas como analises especificas de servidor. Tambem faz a captura e exibicao de cookies HTTP.

**Exemplos de uso:**

-----------------------------------

**1. Varredura de um site na porta padrao 80:**
  - -h (host)
  - *Porta unica A varredura Nikto mais basica requer simplesmente um host para o destino, uma vez que a porta 80 e assumida se nenhuma for especificada. O host pode ser o IP ou o nome do host de uma maquina e e especificado usando a opcao -h (-host). Isso fara a varredura do IP 192.168.0.1 na porta TCP 80*

  **Comando**
  ```
  nikto -h www.webbsite.com
  ```

-----------------------------------

**2. Varredura de um site na porta especifica:**
  - -p (port)
  - *Para verificar uma porta diferente, especifique o numero da porta com a opcao -p (-port). Isso fara a varredura do IP 192.168.0.1 na porta TCP 443*

  **Comando**
  ```
  nikto -h 192.168.0.1 -p 443
  ```

-----------------------------------

**3. Varredura de um site em multiplas portas:**
  - -p (port)
  - *Nikto pode escanear varias portas na mesma sessao de escaneamento. Para testar mais de uma porta no mesmo host, especifique a lista de portas na opcao -p (-port). As portas podem ser especificadas como um intervalo (ou seja, 80-90) ou como uma lista delimitada por virgulas (ou seja, 80,88,90). Isso fara a varredura do host nas portas 80, 88 e 443. *

  **Comando**
  ```
  nikto -h 192.168.0.1 -p 80,88,443
  ```

-----------------------------------

**4. Utilizando o Nikto com o Tor Proxy:**
  - *Bem como muitas ferramentas destinadas a varreduras e scans, o Nikto gera muito trafego na rede ao fazer requisicoes ao alvo, deixando um vasta lista de logs nos Firewalls e servidores. Se voce esta realizando um hacking/pentest, a ultima coisa que voce deveria querer, e que um dispositivo de seguranca capture seu verdadeiro IP e possa tomar acoes desagradaveis com ele depois.*

Precisamos de tor e privoxy
Edite o /etc/privoxy/config
E procure pela linha que contenha: listen-address localhost:8118
Assim que encontra-la, substitua-a por: listen-address 127.0.0.1:8118

Apos isso, localize a linha que contenha: #forward-socks5 / 127.0.0.1:9050
...e apenas remova o # da frente da mesma, ficando: forward-socks5 / 127.0.0.1:9050

Agora, digite o seguinte comando para reiniciar o Tor e o Privoxy:
/etc/init.d/tor restart && /etc/init.d/privoxy restart && update-rc.d tor enable && update-rc.d privoxy enable

As configuracoes do Privoxy estao prontas, faltando apenas configurarmos o Nikto. Ainda no terminal, digite:

edit /etc/nikto.conf

E procure pela linha que diz:

  #Proxy settings -- still must be enabled by -useproxy
  #PROXYHOST=127.0.0.1
  #PROXYPORT=8080

Aqui, basta remover os # das duas ultimas linhas (visto que a primeira e um comentario) e, ao inves de 8080, substitua por 8118 (porta do privoxy), ficando assim:

  #Proxy settings -- still must be enabled by -useproxy
  PROXYHOST=127.0.0.1
  PROXYPORT=8118

Concluido essas configuracoes, ao realizar um scan com Nikto, basta apenas definir a opcao -useproxy, sem nenhum parametro para que todo o trafego gerado pelo Nikto passe pela rede Tor, mantendo assim o seu anonimato.

```
nikto -h https://website.com:8081 -useproxy
```

-----------------------------------
**Instalar no OSX**
```
brew install nikto
```

**Referencias**
- :bookmark:  https://cirt.net/Nikto2
- :bookmark:  https://github.com/sullo/nikto
- :bookmark:  https://www.nanoshots.com.br/2015/09/nikto-um-poderoso-scanner-de-servidores.html