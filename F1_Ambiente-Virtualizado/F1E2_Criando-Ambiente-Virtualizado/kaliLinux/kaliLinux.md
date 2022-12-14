#  Kali (Red Team Machine)


## Sumário

- [Preparação do Ambiente](#Preparação-do-ambiente)
  - [Baixando a ISO](#baixando-a-iso)
  - [Configurando o Hyper-V](#configurando-o-hyper-v)
- [Criação da VM](#criação-da-vm)
  - [Requisitos Mínimos](#requisitos-mínimos)
  - [Criando uma VM](#criando-uma-vm-máquina-virtual)
  - [Instalando a .ISO](#instalando-o-sistema-operacional-iso)
  - [Configurando o Sistema](#configurando-o-sistema)


## Instalação
Neste documento será apresentado o passo a passo para a configuração do sistema operacional na máquina de usuário, que para fins do projeto foi utilizado o Sistema Operacional Windows 7 Ultimate - 64 BifARRRUMAAAAAAAAAAAAAAAAAAAAAAAARRRRRRRRRRRRRRRRRRRR

## Requisitos

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
|      Memória RAM: |  512 MB      |    8 GB     |
|    Armazenamento: |  5 GB        |    20 GB    |
| Memória de vídeo: |  -           |    -        |



## Preparação do ambiente

## Baixando a ISO

Acesse o site oficial do Sistema Operacional Kali https://www.kali.org

1º: Clicar na opção de Downloads.

![image](https://user-images.githubusercontent.com/105310922/206779801-24c2b0f4-7518-4d6b-8370-656371c23a07.png)


2º: Em seguida deverá ser escolhido para qual plataforma o sistema operacional será instalado.

![image](https://user-images.githubusercontent.com/105310922/206780020-dbee31c8-dddf-4048-93c8-acc7da9ef96d.png)

3º: Para nosso cenário em especial, será indicado a escolha da opção _Installer Images_, desta forma clicar na opção Installer para que seja inicializado o download da Imagem do sistema(.iso) do Kali Linux.
![image](https://user-images.githubusercontent.com/105310922/206780592-85e98dbf-f5be-4b83-9eec-95d060713d6f.png)

## Configurando o Hyper-V

Acesse o site oficial do Sistema Operacional Kali https://www.kali.org

1º: Clicar na opção de Downloads.


2º: Em seguida deverá ser escolhido para qual plataforma o sistema operacional será instalado.


3º: Para nosso cenário em especial, será indicado a escolha da opção _Installer Images_, desta forma clicar na opção Installer para que seja inicializado o download da Imagem do sistema(.iso) do Kali Linux.


# Criação da VM


2º - Em seguida realize a criação de um ambiente virtual no Hyper-V. Utilizando o tutorial do link a seguir:
[Criando Marquina virtual](./../../F1E2_Criando-Ambiente-Virtualizado/Hyper-V/hyper-v.md/#criando-uma-vm-máquina-virtual)


Criando uma VM (Máquina Virtual)
Em Gerenciador do Hyper-v no menu da esquerda selecione item com o nome do computador físico

No menu de Ações à direita, clique na opção 'Novo > Máquina Virtual'

Em Assistente de Nova Máquina Virtual,

Antes de Começar, leia as recomendações e clique no botão 'Avançar'.

Especificar Nome e Local, dê um nome à nova Máquina Virtual e clique no botão 'Avançar'.

[ windows-server-2016 ]
Especificar Geração, selecione a geração desejada e clique no botão 'Avançar'.

 Geração 1

# [![Home][homeimage]][homelink] [![Top][topimage]](#)

[topimage]: https://img.shields.io/badge/-Voltar_ao_topo-grey
[homeimage]: https://img.shields.io/badge/-Home-blue
[homelink]: ./../../../README.md#

