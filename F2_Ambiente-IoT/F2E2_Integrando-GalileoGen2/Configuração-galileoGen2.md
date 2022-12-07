# Sumario

- [ Requisitos](#requisitos)
- [Instalando o Sistema Operacional](#instalando-sistema-operacional)
  - [Baixando Imagem](#1-baixe-imagem-do-so-poky-sdcard111tarbz2)
  - [Preparando SD Card](#2-prepare-cartão-sd)
  - [Instalação do SO](#3-instalação-do-so)
- [Comunicação via SSH](#comunicação-ssh)
- [Configuração de IP Fixo](#configurando-ip-fixo)
- [Configurando a Arduino IDE](#configure-a-ide-do-arduino)
- [Configuração do Syslog](#configurando-syslog)

# Requisitos

- Kit intel Galileo gen2
  - Placa: [Intel® Galileo Gen 2 Board](https://www.intel.com/content/www/us/en/products/sku/83137/intel-galileo-gen-2-board/specifications.html)
  - Fonte: 9V/1,5A
  - Cabo: USB
  - CAbo de rede: Cat5
- SD Card
  - Size: 8GB
- Imagem do Sistema Operacinal
  - File: sdcard.1.1.1.tar.bz2
  - Size: 49.1 MB
  - SHA1: B2E10B4C61E476E1EDCC61DC304F7728F9AFB307
  - Link: [Intel® Galileo - Board Support Package](https://www.intel.com/content/www/us/en/download/17523/intel-galileo-board-support-package.html)
- Arduino IDE
  - Link: [www.arduino.cc](https://www.arduino.cc/en/software)
  - Doc: [Arduino IDE 2 Tutorials](https://docs.arduino.cc/software/ide-v2)

# Instalando o **Sistema Operacional**

1. Baixe **Imagem do Sistema Operacinal**

   - File: sdcard.1.1.1.tar.bz2
   - Size: 49.1 MB
   - SHA1: B2E10B4C61E476E1EDCC61DC304F7728F9AFB307
   - Disponível em: [Intel® Galileo - Board Support Package](https://www.intel.com/content/www/us/en/download/17523/intel-galileo-board-support-package.html)

1. Prepare o **SD Card**

   1. Formate o **SD Card**.<!-- [***] Qual formato? -->
   1. Descompacte a **Imagem do Sistema Operacinal** (sdcard.1.1.1.tar.bz2).
   1. Copie os arquivos descompactados para a pasta raiz do **SD Card**.
   1. Ejete o **SD Card**.

1. Instalação do Sistema Operacinal

   1. Com a placa **intel Galileo gen2** desligada, insira o **SD Card** (com o Sistema Operacinal) na placa **intel Galileo gen2**.

   1. Utilizando a fonte de alimentação, alimente a placa **intel Galileo gen2**.

   1. Com a placa **intel Galileo gen2** energizada, conecte o cabo **micro USB** e o **cabo de rede**

   1. Em **gerenciador de dispositivos** (do host), agaurde reconhecer a porta serial (COM).

# Configurando o **Arduino IDE**

1. Execute a **Arduino IDE**

1. Em Tools > Boards > Boards manager.

   - Pesquise por 'galileo' (intel i586 boards by intel) e instale os drivers.

1. Em Tolls > Board > Intell i586 boards.

   - Selecione intel galileo gen2.

1. Em Tools > Port.

   - Selecione a porta (COM) reconhecida no **gerenciador de dispositivos**.

# Configurando **IP Fixo**

- Neste exemplo utilizaremos:

  |                      |               |
  | -------------------- | ------------- |
  | IP Computador local: | 192.168.1.17  |
  | IP Galileo:          | 192.168.1.100 |
  | Máscara de SubRede:  | 255.255.255.0 |

  ##### Obs.: Certifique-se de os endereços de IP estarem na mesma faixa. <!-- Precisamos melhorar isso -->

1. Copie o código abaixo e cole no **Arduino IDE**.

```C
void setup()
{
  String ip = "192.168.1.100";          // Alterar para mesma faixa de ip do host
  String mascara = "255.255.255.0";     // Alterar para mesma faixa de Subrede do host
  String comandoStr = ("ifconfig eth0 " + ip + " netmask " + mascara);

  int comandoLen = comandoStr.length() + 1;
  char comando[comandoLen];

  comandoStr.toCharArray(comando, comandoLen);
  system("telnetd -l /bin/sh");
  system(comando);
}

void loop()
{
   system("ifconfig > /dev/ttyGS0");
   sleep(20);
}
```

2. Faça _upload_ do código;

   - Em **Arduino IDE** clique no botão 'Upload'
   - Aguarde a mensagem _Tranfer complete_

3. Confirme alteração de IP realizada no Galileo;

   - Em Tools > Serial Monitor

     - _Set_ **_baud rate_** para **115200**.
     - Aguarde mensagem com o IP da interface **eth0**.

4. Verifique a Conexão;

   - Em CMD pingue o ip configurado na placa **intel galileo gen2** utilizando o comando:

     ```cmd
     ping 192.168.1.100
     ```

# Configurando syslog

1. Execute a conexão SSH;

   1. Em CMD execute o comando:

   ```cmd
   ssh root@192.168.1.100
   ```

   1. Quando solicitado digite '_yes_'

   1. Deverá aparecer a seguinte mensagem de confirmação:
      ![Imagem](../../img/galileo/SSH-confirm.png) <!-- Precisamos de uma foto que possua o endereço IP igual ao do exempo para não gerar confusão  -->

1. Configure o arquivo Syslog-startup.conf.busybox

   1. No terminal do Galileo digite o comando:

      ```cmd
      vi etc/syslog-startup.conf.busybox
      ```

   1. Edite o arquivo alterando os atributos conforme a imagem:
      ![syslog-config](../../img/galileo/syslog-config.png)

## [[ Voltar ao Topo ]](#sumario)
