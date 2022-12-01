# Ambiente-Simulado
Ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques.
# Proposta

Construir um ambiente virtualizado para simulação de testes de invasão e monitoramento de ataques. O ambiente será composto por máquinas virtuais e sistemas embarcados onde dever ser possível o estudo cenários de ataques, ferramentas e monitoria de eventos.

# Imersão 
- A área de Segurança Cibernética é multidisciplinar e envolve o conhecimentos diversos como sistemas operacionais, ferramentas, desenvolvimento de softwares, dentre outros.  
- Assim a proposta do Desafio Lenovo é introduzir os alunos do programa Connors-Facens em um ambiente onde eles terão contato com cenários simplificados, mas coerentes, com o desafios e tecnologias utilizadas no dia a dia das empresas.  

# Fase 01
- As equipes deverão construir um ambiente virtualizado e um sistema de monitoramento de incidentes para este ambiente, que possibilite a criação de cenários de simulação e a detecção de incidentes nestes cenários. 
- Após a criação do ambiente serão propostos desafios de levantamento de vulnerabilidades, teste de invasão, exploração de vulnerabilidades, ataques de vírus que deverão ser detectados pelos sistemas de monitoramento.

# Ambiente de Simulação
![Ambiente Simulado](./propostaImg/ambienteSimulado.png)
## Descrição do ambiente
<!-- O ambiente deverá compor... -->

# Regras de conectividade do ambiente

- O Servidor Web e de DNS são acessíveis tanto na rede interna quanto externa. As demais máquinas não. 
- O computador de usuário (User Machine) pode acessar computadores fora da rede, mas não pode ser acessado remotamente. 
- O computador Blue Team pode acessar qualquer computador da rede interna. 
- O computador Red Team pode acessar apenas o Servidor Web e Servidor de DNS. 
- Todas as máquinas devem ter um endereço de IP Fixo. 
- As máquinas devem estar em uma rede sem acesso a internet e isolada das demais redes da Facens.


