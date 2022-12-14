# Windows 10 (Blue Team Machine)

## Sumário

- [Preparação do Ambiente](#preparação-do-ambiente)
  - [Instalação](#instalação)
  - [Requisitos](#requisitos)
  - [Baixando a ISO](#baixando-a-iso)
  - [Configurando o Hyper-V](#configurando-o-hyper-v)
- [Criação da VM](#criação-da-vm)
  - [Criação do Ambiente virtual](#criação-do-ambiente-virtual)
  - [Instalando a .ISO](#instalando-a-iso)

## Preparação do ambiente

### Instalação

Neste documento será apresentado o passo a passo para a configuração do Sistema Operacional na máquina do Blue Team, que para fins do projeto foi utilizado o Sistema Operacional Windows 10 Professional - 64 Bits

### Requisitos

> Sistema Operacional: Windows 10

|   Máquina Virtual | Mínimo  | Recomendado |
| ----------------: | :-----: | :---------: |
|    Processadores: |    2    |      4      |
|       Arquitetura | 32 bits |   64 bits   |
|      Memória RAM: |  2 GB   |    4 GB     |
|    Armazenamento: |  32 GB  |    32 GB    |
| Memória de vídeo: |  64 MB  |    64 MB    |

### Baixando a ISO

1. Baixe o Windows 10

   Para começar, primeiro você precisa ter uma **licença** para instalar o Windows 10. Você pode então fazer download e executar a ferramenta de criação de mídia.

1. Faça o [download](https://go.microsoft.com/fwlink/?LinkId=691209) e execute a _ferramenta de criação de mídia_.

   > **Note**: Você precisa ser administrador para executar esta ferramenta.

1. Se você concordar com os termos de licença, selecione Aceitar.
1. Na página _O que você deseja fazer?_ selecione Criar mídia de instalação para um outro computador e selecione Avançar.
   Selecione o idioma, a edição e a arquitetura (64 bits ou 32 bits) do Windows 10.

   - [x] Windows 10 (64 bits)

1. Selecione a mídia que você deseja usar:

   - [ ] Pen drive.

     > Conecte um pen drive vazio com, pelo menos, 8GB de espaço. Todo conteúdo do pen drive será excluído.

   - [x] Arquivo ISO.

     > Salve um arquivo ISO em seu computador, que pode ser usado para criar um DVD. Depois que o arquivo é baixado, você pode ir até o local em que o arquivo foi salvo ou selecionar Abrir gravador de DVD e seguir as instruções para gravar o arquivo em um DVD.

1. Depois que a mídia de instalação estiver criada, siga as etapas [Criando uma maquina virtual](./../Hyper-V/hyper-v.md#criando-uma-vm-máquina-virtual) utilizando o tutorial do Hyper-V para usá-las.

   > Após concluir as etapas para instalar o Windows 10, verifique se você tem todos os drivers de dispositivo necessários instalados. Para verificar se há atualizações agora, selecione o botão Iniciar, acesse Configurações > Atualização e Segurança > Windows Update e selecione Verificar se há atualizações.

### Configurando o Hyper-V

1. [Habilite o Hyper-V](../Hyper-V/hyper-v.md)

## Criação da VM

### Criação do Ambiente Virtual

Em seguida realize a criação de um ambiente virtual no Hyper-V (clique no link asseguir para verificar o procedimento)  
[Criando Ambiente Virtual | Hyper-V](./../../F1E2_Criando-Ambiente-Virtualizado/Hyper-V/hyper-v.md/#criando-uma-vm-máquina-virtual)

### Instalando a ISO


Após o Boot do Sistema Operacional será apresentada a primeira tela do sistema onde serão solicitadas as configurações de linguagem, local, hora e teclado. Para este projeto foi aplicado as respectivas configurações abaixo:

![image](https://user-images.githubusercontent.com/105310922/207738459-fbf43d01-74e6-4155-a586-7305af14cf69.png)


Após o Boot do Sistema Operacional será apresentada a primeira tela do sistema onde serão solicitadas as configurações de linguagem, local, hora e teclado. Para este projeto foi aplicado as respectivas configurações abaixo:

- **_Language to install:_** English  
- **_Time and currency format:_** Portuguese(Brazil)  
- **_Keyport or input method:_** Portuguese(Brazilian ABTN2) 

A seguir clique em **_"Next"_**  
![image](https://user-images.githubusercontent.com/105310922/207738548-68a66efe-69c8-41d0-a4c6-25408b3c556a.png)

Clique em **_Install Now:_**  
![image](https://user-images.githubusercontent.com/105310922/207738584-a4e57b83-aa97-4624-acbb-ed94c1699603.png)

![image](https://user-images.githubusercontent.com/105310922/207738806-a80475e3-fecf-4ae5-a855-d9729cc5e203.png)

![image](https://user-images.githubusercontent.com/105310922/207738914-6758ad76-e93f-41c4-86af-dd6237159cf8.png)


Na tela a seguir, **aceite os termos** de licença, e clique em **_Next_**
![image](https://user-images.githubusercontent.com/105310922/207738986-f8d301ee-af5d-416e-b2a3-3f6b4a7726ad.png)

Selecione a opção **_Custom (advanced)_**
![image](https://user-images.githubusercontent.com/105310922/207739051-df95a438-6154-4bed-98ea-cfff578201af.png)

Selecione o Disco a ser instalado o Sistema operacional e clique em **_"Next"_**
![image](https://user-images.githubusercontent.com/105310922/207739125-2015760c-21c8-4d58-a11e-36b7e0ae8e05.png)

Aguarde as configurações do Sistema Operacional serem carregadas...  
![image](https://user-images.githubusercontent.com/105310922/207739326-02bc1ff3-e502-4638-98ce-46e4d9798691.png)


![image](https://user-images.githubusercontent.com/105310922/207739442-36be25b4-478b-473a-bfc5-7d2a2b7e8e56.png)
![image](https://user-images.githubusercontent.com/105310922/207739520-ac94a9a7-f7c5-411d-86b0-e7804d72f120.png)
![image](https://user-images.githubusercontent.com/105310922/207739564-b732526c-18cf-4c75-899c-2bd806d9c1f5.png)
![image](https://user-images.githubusercontent.com/105310922/207739617-90ab37d7-a917-4ad3-86ab-d74187cddbfb.png)
![image](https://user-images.githubusercontent.com/105310922/207739671-37021eb4-49ac-4890-a167-85e03d1449fb.png)
![image](https://user-images.githubusercontent.com/105310922/207739702-b7298f9f-6331-4259-be8c-41e077d31912.png)
![image](https://user-images.githubusercontent.com/105310922/207739770-e6e133b5-793a-432b-9d98-9e62bae1a260.png)
![image](https://user-images.githubusercontent.com/105310922/207739832-3c6bf9a4-5e47-4b5c-a6ba-4f5fb2d7c9ef.png)

![image](https://user-images.githubusercontent.com/105310922/207740173-cf133deb-1672-48e5-a2d1-2e3ee9fed9d3.png)
![image](https://user-images.githubusercontent.com/105310922/207740270-71d7ba8d-2e07-4493-8743-1107c93f59ed.png)
![image](https://user-images.githubusercontent.com/105310922/207740332-41f39ebc-f1e9-440a-92fc-5ae15dc0a5af.png)
![image](https://user-images.githubusercontent.com/105310922/207740394-658bd7ea-1c7e-4af0-8a8d-6b7d1c3570d9.png)

![image](https://user-images.githubusercontent.com/105310922/207740476-cdecdb16-bdeb-40f5-aae8-16eb48e0d36a.png)
![image](https://user-images.githubusercontent.com/105310922/207740551-d3974867-dadb-46f6-96ec-3b5fe49ae6ea.png)
![image](https://user-images.githubusercontent.com/105310922/207740610-92c10149-092c-4fc0-afb1-4a010d3809c0.png)
![image](https://user-images.githubusercontent.com/105310922/207740677-4f3b74ea-e01b-4979-80b3-2cac1cceea27.png)
![image](https://user-images.githubusercontent.com/105310922/207740728-2f15b80f-858c-4f4e-b6f8-6cd58d1b4c43.png)
![image](https://user-images.githubusercontent.com/105310922/207740786-03156782-8575-491f-acd1-74a17adce2ed.png)




Após o sistema carregar todos os arquivos necessários o mesmo deverá será reinicilizado  


Em seguida será apresentada a primeira tela de configuração do sistema onde deverá ser informado o nome da máquina. Para nosso projeto consideramos o nome da máquina como **_User_**  


Na tela seguinte, o usuário deverá informar a senha bem como a confirmação de senha, em seguida de uma dica de lembrete para a mesma. Após o preenchimento, clicar em **_Next_**


Na tela de ativação da tela de produto, selecione a opção **_Skip_**


Clique em "Use recommended settings"  


Selecione a **_Time Zone_** desejada e clique em **_Next_**


Nesta tela deverá selecionado o tipo de conexão de rede. Para este projeto como se trata de um ambiente simulado, foi configurado o tipo de rede "Residencial" através da opção **_Home Network_**

Após a realização de todas as configurações, o Sistema Operacional Windows 7 será inicializado e estará pronta para o uso.

![image](https://user-images.githubusercontent.com/105310922/207740855-c5233427-1fdf-48fe-ba5c-b3e4ef31fad5.png)




# [![Home][homeimage]][homelink] [![Top][topimage]](#)
[topimage]: https://img.shields.io/badge/-Voltar_ao_topo-grey
[homeimage]: https://img.shields.io/badge/-Home-blue
[homelink]: ./../../../README.md#













