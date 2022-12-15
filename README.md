# Ambiente-Simulado

Ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques.

# Sumário

- [Proposta](#proposta)
  - [Imersão](#imersão)
  - [Fase 01](#fase-01)
  - [Ambiente de Simulação](#ambiente-de-simulação)
  - [Regras de Conectividade do Ambiente](#regras-de-conectividade-do-ambiente)
- [Workshops](#workshops)
- [Tutoriais](#tutoriais)

# Proposta

Construir um ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques. O ambiente será composto por máquinas virtuais e sistemas embarcados onde dever ser possível o estudo cenários de ataques, ferramentas e monitoria de eventos.

## Imersão

- A área de Segurança Cibernética é multidisciplinar e envolve o conhecimentos diversos como sistemas operacionais, ferramentas, desenvolvimento de softwares, dentre outros.
- Assim a proposta do Desafio é introduzir os alunos em um ambiente onde eles terão contato com cenários simplificados, mas coerentes, com o desafios e tecnologias utilizadas no dia a dia das empresas.

## Fase 01

- As equipes deverão construir um ambiente virtualizado e um sistema de monitoramento de incidentes para este ambiente, que possibilite a criação de cenários de simulação e a detecção de incidentes nestes cenários.
- Após a criação do ambiente serão propostos desafios de levantamento de vulnerabilidades, teste de invasão, exploração de vulnerabilidades, ataques de vírus que deverão ser detectados pelos sistemas de monitoramento.

## Ambiente de Simulação

![Ambiente Simulado](./img/readme/ambienteSimulado.png)

## Regras de conectividade do ambiente

1. O Servidor Web e de DNS são acessíveis tanto na rede interna quanto externa. As demais máquinas não.
1. O computador de usuário (User Machine) pode acessar computadores fora da rede, mas não pode ser acessado remotamente.
1. O computador Blue Team pode acessar qualquer computador da rede interna.
1. O computador Red Team pode acessar apenas o Servidor Web e Servidor de DNS.
1. Todas as máquinas devem ter um endereço de IP Fixo.
1. As máquinas devem estar em uma rede sem acesso a internet e isolada das demais redes.

## F1E1 Workshops

- [**ELK Stack**](./F1_Ambiente-Virtualizado/F1E1_Workshops/ELK_Stack)
- [**Kali Linux**](./F1_Ambiente-Virtualizado/F1E1_Workshops/KaliLinux)
- [**Linux**](./F1_Ambiente-Virtualizado/F1E1_Workshops/Linux)
- [**pfSense**\*](./F1_Ambiente-Virtualizado/F1E1_Workshops/pfSense/)
- [**Windows Server**](./F1_Ambiente-Virtualizado/F1E1_Workshops/WindowsServer/Workshop.md)

Neste repositório está apresentada toda documentação técnica do projeto

## F1E2 Criando o **Ambiente Simulado**
  - [Habilitando e configurando o **Hyper-V** (Gerenciador do ambiente virtual)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Hyper-V/hyper-v.md/#)
  - [Instalando o **Windows 10** (Blue Team Machine)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Máquina%20Blue%20Team/Windows_10.md)
  - [Instalando o **Kali Linux 2022** (Red Team Machine)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Máquina%20Red%20Team/Kali_Linux.md)
  - [Instalando o **pfSense** (Firewall)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Firewall/pfSense.md)
  - [Instalando o **Servidor DNS**\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Servidor%20DNS/dnsServer.md)
  - [Instalando o **Windows 7** (User Machine)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Máquinas%20Clientes/Windows_7.md)
  - [Instalando o **Metasploitable 2** (Web Server + DB)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Servidor%20Web/metasploitable2.md)
  - [Instalando o **Windows Server 2016** (Servidor de autenticação LDAP, Arquivos e E-mail)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Active%20Directory/01%20Instalação%20Windows%20Server%202016.md)
  - [Instalando o **ELK Stack** (SIEM)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/SIEM/ELK.md)
## F1E3 Simulação
  - RASCUNHO
  
## F2E1 Entendendo "Galileo Gen2"
  - RASCUNHO

## F2E2 Integrando "Galileo Gen2"
  - [Configurando **Intel® Galileo Gen 2 Board**](./F2_Ambiente-IoT/F2E2_Integrando-GalileoGen2/galileoGen2.md)

## F2E3 Simulando Ambiente Galileo Gen2"
  - RASCUNHO

##### \*Documentação em desenvolvimento, consulte [status do projeto](./docStatus.md) ou a branch **develop** pode ser que já esteja disponível por lá ;).

# [![](https://img.shields.io/badge/-Voltar%20ao%20topo-grey)](#)
