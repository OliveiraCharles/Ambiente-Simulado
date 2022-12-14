# Ambiente-Simulado

- [Proposta](#proposta)
- [Imersão](#imersão)
- [Fase 01](#fase-01)
- [Ambiente de Simulação](#ambiente-de-simulação)
- [Regras de Conectividade do Ambiente](#regras-de-conectividade-do-ambiente)
- [Tutoriais](#tutoriais)

Ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques.

# Proposta

Construir um ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques. O ambiente será composto por máquinas virtuais e sistemas embarcados onde dever ser possível o estudo cenários de ataques, ferramentas e monitoria de eventos.

# Imersão

- A área de Segurança Cibernética é multidisciplinar e envolve o conhecimentos diversos como sistemas operacionais, ferramentas, desenvolvimento de softwares, dentre outros.
- Assim a proposta do Desafio é introduzir os alunos em um ambiente onde eles terão contato com cenários simplificados, mas coerentes, com o desafios e tecnologias utilizadas no dia a dia das empresas.

# Fase 01

- As equipes deverão construir um ambiente virtualizado e um sistema de monitoramento de incidentes para este ambiente, que possibilite a criação de cenários de simulação e a detecção de incidentes nestes cenários.
- Após a criação do ambiente serão propostos desafios de levantamento de vulnerabilidades, teste de invasão, exploração de vulnerabilidades, ataques de vírus que deverão ser detectados pelos sistemas de monitoramento.

# Ambiente de Simulação

![Ambiente Simulado](./img/readme/ambienteSimulado.png)

# Regras de conectividade do ambiente

1. O Servidor Web e de DNS são acessíveis tanto na rede interna quanto externa. As demais máquinas não.
1. O computador de usuário (User Machine) pode acessar computadores fora da rede, mas não pode ser acessado remotamente.
1. O computador Blue Team pode acessar qualquer computador da rede interna.
1. O computador Red Team pode acessar apenas o Servidor Web e Servidor de DNS.
1. Todas as máquinas devem ter um endereço de IP Fixo.
1. As máquinas devem estar em uma rede sem acesso a internet e isolada das demais redes.

# Tutoriais

Neste repositório estão presentes os paso a passo de toda preparação do **Ambiente Simulado**, listados abaixo para fácil localização:

- F1 Criando o **Ambiente Simulado**
  - [Habilitando e configurando o **Hyper-V** (Gerenciador do ambiente virtual)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/Hyper-V/hyper-v.md)
  - [Instalando o **Windows 10** (Blue Team Machine)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/windows10/windows10.md)
  - [Instalando o **Kali Linux 2022** (Red Team Machine)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/kaliLinux/kaliLinux.md)
  - [Instalando o **pfSense** (Firewall)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/pfSense/pfSense.md)
  - [Instalando o **Servidor DNS**\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/dnsServer/dnsServer.md)
  - [Instalando o **Windows 7** (User Machine)\*](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/windows7/windows7.md)
  - [Instalando o **Metasploitable 2** (Web Server + DB)\*](metasploitable2.md)
  - [Instalando o **Windows Server 2016** (Servidor de autenticação LDAP, Arquivos e E-mail)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/winServer/winServer.md)
  - [Instalando o **Elastic Search v7.x** (SIEM)](./F1_Ambiente-Virtualizado/F1E2_Criando-Ambiente-Virtualizado/ELK/ELK.md)
- F2 Criando **ambiente IoT**
  - [Configurando **Intel® Galileo Gen 2 Board**](./F2_Ambiente-IoT/F2E2_Integrando-GalileoGen2/galileoGen2.md)


##### \*Documentação em desenvolvimento, consulte a branch **develop** pode ser que já esteja disponível por lá ;)