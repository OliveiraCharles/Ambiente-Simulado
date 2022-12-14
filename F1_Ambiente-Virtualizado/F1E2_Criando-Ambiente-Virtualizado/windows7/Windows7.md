# Instalação - Windows 7 (User Machine)

#### Neste documento será apresentado o passo a passo para a configuração do sistema operacional na máquina de usuário, que para fins do projeto foi utilizado o Sistema Operacional Windows 7 Ultimate - 64 Bits

## Requisitos

> Sistema Operacional: Windows 7 Ultimate - 64 Bits

|   Máquina Virtual | Mínimo  | Recomendado |
| ----------------: | :-----: | :---------: |
|    Processadores: |    2    |      4      |
|       Arquitetura | 64 bits |   64 bits   |
|      Memória RAM: |  1 GB   |    4 GB     |
|    Armazenamento: |  5 GB   |    16 GB    |
| Memória de vídeo: |  64 MB  |    64 MB    |



**1º** - Acesse o link oficial da Microsoft e baixe o arquivo de Imagem do Sistema Operacional de sua preferência (**Obs:** Para este projeto foi utilzada a imagem Windows 7 Ultimate - 64 bits, conforme descrição)
 
**_Downloads(ISO)_**

- _Windows 7 Ultimate x64:_ 
https://download.microsoft.com/download/5/1/9/5195A765-3A41-4A72-87D8-200D897CBE21/7601.24214.180801-1700.win7sp1_ldr_escrow_CLIENT_ULTIMATE_x64FRE_en-us.iso

- _Windows 7 Ultimate x86:_
https://download.microsoft.com/download/1/E/6/1E6B4803-DD2A-49DF-8468-69C0E6E36218/7601.24214.180801-1700.win7sp1_ldr_escrow_CLIENT_ULTIMATE_x86FRE_en-us.iso

- _Windows 7 Professional x64:_ 
https://download.microsoft.com/download/0/6/3/06365375-C346-4D65-87C7-EE41F55F736B/7601.24214.180801-1700.win7sp1_ldr_escrow_CLIENT_PROFESSIONAL_x64FRE_en-us.iso

- _Windows 7 Professional x86:_  
https://download.microsoft.com/download/C/0/6/C067D0CD-3785-4727-898E-60DC3120BB14/7601.24214.180801-1700.win7sp1_ldr_escrow_CLIENT_PROFESSIONAL_x86FRE_en-us.iso

2º - Em seguida realize a criação de um ambiente virtual no Hyper-V e clique em Nova Máquina
[Criando Marquina virtual](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Hyper-V/hyper-v.md#criando-uma-vm-máquina-virtual)

3º - Após o Boot do Sistema Operacional será apresentada a primeira tela do sistema onde serão solicitadas as configurações de linguagem, local, hora e teclado. Para este projeto foi aplicado as respectivas configurações abaixo:

- **_Language to install:_** English  
- **_Time and currency format:_** Portuguese(Brazil)  
- **_Keyport or input method:_** Portuguese(Brazilian ABTN2) 

A seguir clique em **_"Next"_**

![image](https://user-images.githubusercontent.com/105310922/207499323-1569b082-3307-475b-b457-c2d30211c4a9.png)

4º - Clique em **_Install Now:_**  
![image](https://user-images.githubusercontent.com/105310922/207500361-bee655e9-bcd8-4095-b559-9393fcc6fb95.png)

5º - Na tela a seguir, **aceite os termos** de licença, e clique em **_Next_**
![image](https://user-images.githubusercontent.com/105310922/207501003-35b577a4-d91f-4a42-bf0d-765167c0fab6.png)

6º - Selecione a opção **_Custom (advanced)_**
![image](https://user-images.githubusercontent.com/105310922/207501336-72939d9b-3a16-4151-a5d8-aa98e2301260.png)

7º Selecione o Disco a ser instalado o Sistema operacional e clique em **_"Next"_**
![image](https://user-images.githubusercontent.com/105310922/207501901-9b95cce2-b99c-43e2-b8c0-6f7cfadf6b0a.png)

8º Aguarde as configurações do Sistema Operacional serem carregadas...  
![image](https://user-images.githubusercontent.com/105310922/207503941-deaffe5d-f651-41f8-bbe5-c1c61710f278.png)

9º - Após o sistema carregar todos os arquivos necessários o mesmo deverá será reinicilizado  
![image](https://user-images.githubusercontent.com/105310922/207503991-fb63cfdc-b8f2-494f-9085-98faad13ef80.png)

10º - Em seguida será apresentada a primeira tela de configuração do sistema onde deverá ser informado o nome da máquina. Para nosso projeto consideramos o nome da máquina como **_User_**  
![image](https://user-images.githubusercontent.com/105310922/207504211-986ed36b-1e5c-457f-81f4-1616aa14cb1a.png)

11º - Na tela seguinte, o usuário deverá informar a senha bem como a confirmação de senha, em seguida de uma dica de lembrete para a mesma. Após o preenchimento, clicar em **_Next_**
![image](https://user-images.githubusercontent.com/105310922/207504283-2fd9fb48-8838-4fbf-9827-807117c14477.png)

12º - Na tela de ativação da tela de produto, selecione a opção **_Skip_**
![image](https://user-images.githubusercontent.com/105310922/207504436-d30e157f-3f0b-42e3-acac-93246622208d.png)

13º - Clique em "Use recommended settings"  
![image](https://user-images.githubusercontent.com/105310922/207504484-74b77ad2-acfc-4f4c-b971-147344a41cb2.png)

14º - Selecione a **_Time Zone_** desejada e clique em **_Next_**
![image](https://user-images.githubusercontent.com/105310922/207504547-4e80e448-b899-4d24-9e73-bfb32cd7c0cd.png)

15º - Nesta tela deverá selecionado o tipo de conexão de rede. Para este projeto como se trata de um ambiente simulado, foi configurado o tipo de rede "Residencial" através da opção **_Home Network_**
![image](https://user-images.githubusercontent.com/105310922/207504614-d61e1b87-7d92-4776-8fec-115271388e94.png)

16º - Após a realização de todas as configurações, o Sistema Operacional Windows 7 será inicializado e estará pronta para o uso.
![image](https://user-images.githubusercontent.com/105310922/207504662-37c37bd3-014b-4938-83e8-db597c7970bc.png)

# [![Home][homeimage]][homelink] [![Top][topimage]](#)
[topimage]: https://img.shields.io/badge/-Voltar_ao_topo-grey
[homeimage]: https://img.shields.io/badge/-Home-blue
[homelink]: ./../../../README.md#














