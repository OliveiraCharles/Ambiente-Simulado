# Sumário
- [Script de Port Scan](#script-de-port-scan)
- [Acesso via SSH](#acesso-via-ssh)

# Script de Port Scan

Fonte: [Script pronto](https://medium.com/@walderlansena/criando-um-scan-de-portas-em-python-85363bd5227e)

- No ambiente da placa de ataque crie um arquivo em branco com seguinte comando:
  ``` bash
  touch nomescript.py
  ```
- Abra o arquivo pelo editor "vi"
  ``` bash
  vi nomescript.py
  ```
- Com arquivo aberto no editor "vi" aperte a tecla "I" para habilitar a edição
- Insira o seguinte código:
  ``` Python
    import socket
    import sys

    if len(sys.argv) < 2:
        print('\n Use: python3 leopardscan.py [IP]')
        exit(1)

    ports = [21, 22, 80, 8080, 443, 53, 3306, 3389] # Lista das portas a serem verificadas

    for i in ports:
        client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        client.settimeout(0.1)
        try:
            response = client.connect_ex((sys.argv[1], i))
            if response == 0:
                print('PORT: ' + str(i) + ' OPEN')
        except:
            print('[ERROR] HOST NOT FOUND')
            exit(1)
    ```
- Apos inserido o código basta apertar as seguintes teclas:
  - ESC -> Tecla para encerrar edição
  - :w -> Comando para salvar o arquivo
  - ENTER -> Execução do :w
  - :q -> Comando para fechar o editor (vi)
  - ENTER -> Execução do :q
  
- Execute o srcipt através do comando:
  ```Bash
    python ./nomescript.py <ColoqueIPdoAlvo>
  ```
- Verifique quais portas o script retornou como abertas no terminal da placa.
  
# Acesso via SSH
**O recurso de SSH está disponível nas placas com Sistema Operacional expandido.**
##### **Tal etapa só é possível se o Port Scan indicar que a porta 22, comumente utilizada no serviço SSH estiver aberta.**

- No terminal da placa execute o seguinte comando:
  ``` bash
  ssh usuario@ipdoalvo
  ```
  - Obs.: No ambiente simulado todas as placas possuíam apenas um usuário disponível, o próprio root.
  - Caso haja uma senha para acesso ela será requisitada após a confirmação do fingerprint da placa.
