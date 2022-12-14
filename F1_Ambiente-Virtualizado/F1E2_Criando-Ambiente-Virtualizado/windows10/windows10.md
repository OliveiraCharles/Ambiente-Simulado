# Instalação - Windows 10 (Blue Team Machine)

#### Neste documento será apresentado o passo a passo para a configuração do Sistema Operacional na máquina do Blue Team que para fins do projeto foi utilizado o Sistema Operacional Windows 10 Professional - 64 Bits

## Requisitos

> Sistema Operacional: Windows 10

|   Máquina Virtual | Mínimo  | Recomendado |
| ----------------: | :-----: | :---------: |
|    Processadores: |    2    |      4      |
|       Arquitetura | 64 bits |   64 bits   |
|      Memória RAM: |  2 GB   |    4 GB     |
|    Armazenamento: |  32 GB  |    32 GB    |
| Memória de vídeo: |  64 MB  |    64 MB    |

## Instalação

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

## Configurações

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













