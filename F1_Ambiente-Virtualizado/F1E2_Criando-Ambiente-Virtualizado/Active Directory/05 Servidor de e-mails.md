# Configuração do servidor de e-mail

Tutorial: https://www.youtube.com/watch?v=5JA6KpSGbXc&ab_channel=ManudoKiller
- [Baixando arquivos necessários](#baixando-arquivos-necessários)
- [Instalando os programas](#instalando-os-programas)
  - [Instalação do hMailServer](#instalação-do-hmailserver)
  - [Instalação do Mozilla ThunderBird](#instalação-do-mozilla-thunderbird)
- [Configurando os programas](#configurando-os-programas)
  - [Configuração do hMailServer](#configuração-do-hmailserver)
  - [Configuração do Mozilla ThunderBird](#configuração-do-mozilla-thunderbird)



## Baixando arquivos necessários

Para realizar a configuração do servidor de e-mail, serão necessários os softwares hMailServer e Mozilla Thunderbird.

1. O download do hMailServer pode ser feito através do link: https://www.hmailserver.com/download
1. O download do Mozilla Thunderbird pode ser feito através do link: https://www.thunderbird.net/pt-BR/

## Instalando os programas

A instalação do hMailServer deve ser realizada na máquina do Windows Server, de acordo com a documentação proposta, enquanto o Mozilla Thunderbird deve ser instalado nas máquinas que terão o aplicativo de e-mail instaladas.

### Instalação do hMailServer

Tendo realizado o download, basta executar o arquivo de instalação e prosseguir com a instalação normalmente, sendo necessário registrar uma senha que posteriormente será utilizada para acessar o servidor criado.

### Instalação do Mozilla ThunderBird

Tendo realizado o download, basta executar o arquivo de instalação e prosseguir com a instalação normalmente, até que seja possível iniciar o software.

## Configurando os programas

Finalizada a etapa de instalação, cada um dos softwares necessita ser configurado corretamente para que a troca de e-mails seja possível de ser realizada.

### Configuração do hMailServer

1. Para configurar o hMailServer, é necessário conectar ao servidor através da senha configurada durante a instalação, em seguida, deve-se adicionar um domínio e selecionar um nome para este domínio.
1. Deve-se então realizar a criação das contas de e-mail que serão utilizadas, através das abas "accounts" e "general", configurando o endereço de email de cada conta pertencente a este domínio e as respectivas senhas, bem como o nome de cada usuário.

### Configuração do Mozilla Thunderbird

1. Ao executar o programa, é solicitado o endereço de email para que seja configurada a caixa de correio.
1. Durante esta etapa é necessário indicar o IP da máquina do Windows Server, no qual o servidor SMTP está presente na aba de "Servidor", e deve-se configurar as portas SMTP como 25, porta padrão do protocolo SMTP e IMAP como 143, porta padrão do protocolo IMAP. Na aba de nome de usuário, o endereço de email configurado no hMailServer deve ser indicado.
1. Finalizado o passo anterior, será necessário indicar a senha que foi configurada no usuário indicado através do hMailServer.
1. Ao realizar a conexão, será criada uma caixa de e-mail que poderá se comunicar com as demais máquinas da rede interna através do servidor de SMTP.
