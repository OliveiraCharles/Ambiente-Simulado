#  Kali (Red Team Machine)

## Sumário

- [Preparação do Ambiente](#preparação-do-ambiente)
  - [Instalação](#instalação)
  - [Requisitos](#requisitos)
  - [Baixando a ISO](#baixando-a-iso)
  - [Configurando o Hyper-V](#configurando-o-hyper-v)
- [Criação da VM](#criação-da-vm)
  - [Criação do Ambiente virtual](#criação-do-ambiente-virtual)
  - [Instalando a .ISO](#instalando-a-.ISO)
  - [Configurando o Sistema](#configurando-o-sistema)


## Preparação do ambiente

### Instalação
Neste documento será apresentado o passo a passo para a instalação do sistema operacional Kali na máquina de _Red Team_, que para fins do projeto foi utilizado o Sistema Kali Linux 2022.4

### Requisitos

Os requisitos de instalação do Kali Linux variam dependendo do que você gostaria de instalar e de sua configuração.

Para requisitos do sistema:

1. Você pode configurar o Kali Linux como um servidor **Secure Shell (SSH) básico sem ambiente gráfico**, usando apenas:

   - 128 MB de RAM (512 MB recomendado) e 2 GB de espaço em disco.

1. Se você optar por instalar o **desktop Xfce4 padrão** e o **metapacote kali-linux-default**, você deve realmente configurar pelo menos:

   - 2 GB de RAM e 20 GB de espaço em disco.

1. Ao usar aplicativos com uso intensivo de recursos, como o **Burp Suite**, é recomendado pelo menos:

   - 8 GB de RAM (e ainda mais se for um aplicativo da Web grande!) Ou usar programas simultâneos ao mesmo tempo.

|   Máquina Virtual | Mínimo       | Recomendado |
| ----------------: | :-----:      | :---------: |
|    Processadores: |    2         |      4      |
|       Arquitetura | 32 / 64 bits |   64 bits   |
|      Memória RAM: |  128 MB      |    8 GB     |
|    Armazenamento: |  5 GB        |    20 GB    |
| Memória de vídeo: |  -           |    -        |


### Baixando a ISO

Acesse o site oficial do Sistema Operacional Kali https://www.kali.org

1º: Clicar na opção de Downloads.

![image](https://user-images.githubusercontent.com/105310922/206779801-24c2b0f4-7518-4d6b-8370-656371c23a07.png)

2º: Em seguida deverá ser escolhido para qual plataforma o sistema operacional será instalado.

![image](https://user-images.githubusercontent.com/105310922/206780020-dbee31c8-dddf-4048-93c8-acc7da9ef96d.png)

3º: Para nosso cenário em especial, será indicado a escolha da opção _Installer Images_, desta forma clicar na opção Installer para que seja inicializado o download da Imagem do sistema(.iso) do Kali Linux.
![image](https://user-images.githubusercontent.com/105310922/206780592-85e98dbf-f5be-4b83-9eec-95d060713d6f.png)

### Configurando o Hyper-V

1. [Habilite o Hyper-V](../Hyper-V/hyper-v.md)

## Criação da VM

### Criação do Ambiente virtual

1. Em **Gerenciador do Hyper-v** no menu da esquerda selecione item com o nome do _computador físico_
1. No menu de **Ações** à direita, clique na opção 'Novo > Máquina Virtual'
1. Em **Assistente de Nova Máquina Virtual**,

   1. **Antes de Começar**, leia as recomendações e clique no botão 'Avançar'.
   1. **Especificar Nome e Local**, dê um nome à nova Máquina Virtual e clique no botão 'Avançar'.
      - [ kali-linux ]
   1. **Especificar Geração**, selecione a geração desejada e clique no botão 'Avançar'.

      - [ ] Geração 1
      - [x] Geração 2

   1. **Atribuir Memória**, no campo _Memória de inicialização_ digite o valor desejado e clique no botão 'Avançar'.  
      Especifique a quantidade de memória a ser alocada na máquina virtual. É possível especificar uma quanbdade de 32MB até 251658240 MB. Para melhorar o desempenho, especifique mais do que o mínimo recomendado para o sistema operacional.
      - [8192]MB
   1. **Configurar Rede**, no campo _Conexão_ selecione qual comutador de rede deseja utilizar e clique no botão 'Avançar'.
      - Default Switch
   1. **Conectar Disco Rígido Virtual**

      - **Criar um disco Rígido Virtual**  
        Use esta opção para criar um disco rígido virtual de expansão dinâmica VHDX.

        1. Dê um nome ao _novo disco rígido virtual_ a ser criado
           - [ kali-linux.vhdx ]
        1. Selecione o local onde sera salvo o _novo disco rígido virtual_
           - [ C:\Users\Public\Documents\Hyper-V\Virtual Hard Disks\ ]
        1. Selecione o tamanho de armazenamento do _novo disco rígido virtual_ em GB (Máximo: 64TB)
           - [ 20 ] GB
        1. Clique no botão 'Avançar'.
        1. **Opções de instalação**

           - **Instalar um sistema operacional a partir de um arquivo de imagem**
             1. Insira o caminho do arquivo .ISO
                - [ C:\Users\...\ISO\Kali-Linux.ISO ]
             1. Clique no botão 'Avançar'.

   1. **Resumo**
      _Assistente de Nova Máquina Virtual_ concluído com êxito, Você está prestes a criar a máquina virtual a seguir.
      


### Instalando a .ISO

  1. Assim que a máquina for inicializada pela primeira vez, após o boot do Kali será necessário escolher o Modo de instalação, clique em **_"Graphic Install"_**  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  2. Em seguida, selecione o idioma desejada. Para este caso selecionaremos **_"Enligsh"_**  
  ![image](https://user-images.githubusercontent.com/105310922/207696452-ebf39793-aca8-4167-b8a5-c4f5e105b0df.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)
  
  1. Tela 1  
  ![image](https://user-images.githubusercontent.com/105310922/207695684-daade2cf-18e3-4e66-bc23-6ce339d96109.png)


### Configurando-o-sistema

  1. **Update:** Assim que o sistema inicializar, realize os updates de pacotes do repositório com o comando **sudo apt update** 
  1. **Upgrade:** Após realizar o update dos pacotes, certifique-se de realizar o upgrade pendente das aplicacções para sempre possuir as últimas versões com o comando **sudo apt upgrade** 



# [![Home][homeimage]][homelink] [![Top][topimage]](#)

[topimage]: https://img.shields.io/badge/-Voltar_ao_topo-grey
[homeimage]: https://img.shields.io/badge/-Home-blue
[homelink]: ./../../../README.md#

