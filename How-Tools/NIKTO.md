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

**Instalar no OSX**
```
brew install nikto
```

**Referencias**
- :bookmark:  https://cirt.net/Nikto2
- :bookmark:  https://github.com/sullo/nikto
- :bookmark:  https://www.nanoshots.com.br/2015/09/nikto-um-poderoso-scanner-de-servidores.html