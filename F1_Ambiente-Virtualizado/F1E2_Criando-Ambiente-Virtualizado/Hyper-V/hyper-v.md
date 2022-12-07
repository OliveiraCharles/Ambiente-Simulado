# Configurando o Hyper-V

Um servidor de virtualização é um computador físico que oferece os recursos necessários à execução de máquinas virtuais. Você pode usar o Gerenciador do Hyper-V para criar, configurar e gerenciar as máquinas virtuais em um servidor de virtualização.

Você pode usar máquinas virtuais para executar cargas de trabalho dferentes. Cada máquina virtual é executada em um ambiente de execução isolado, o que oferece a você a flexibilidade para executar sistemas operacionais e aplicativos dferentes em um computador físico.

O Hyper-V fornece a virtualização de hardware. Isso significa que cada máquina virtual é executada em hardware virtual. O Hyper-V permite que você crie discos rígidos virtuais, comutadores virtuais e um número de outros dispositivos virtuais que podem ser adicionados a máquinas virtuais.

## Ativando o Hyper-V

1. Na **barra de tarefas** clique no 'botão iniciar'
1. No **campo de pesquisa** do _menu iniciar_ digite: 'recursos'
1. Nos **resultados da pesquisa** clique na opção 'Ativar ou desativar recursos do Windows'
1. Em **Recursos do Windows**:

   1. utilize o _botão de rolagem_ do mouse até encontrar a opção 'Hyper-V'
   1. marque a _caixa de seleção_ referente a ativação do 'Hyper-V'
   1. clique no botão 'Ok'
   1. quando solicitado clique no botão 'Reiniciar agora'

## Gerenciando o Hyper-V

1. Na **barra de tarefas** clique no 'botão iniciar'
1. No **campo de pesquisa** do _menu iniciar_ digite: 'gerenciador'
1. Nos **resultados da pesquisa** clique na opção 'Gerenciador do Hyper-V'

### Criando um Comutador Virtual (Placa de Rede)

1. Em **Gerenciador do Hyper-v** no menu da esquerda selecione item com o nome do _computador físico_
1. No menu de **Ações** à direita clique na opção 'Gerenciador de comutador virtual'
1. Em **Gerenciador de comutador virtual para _computador físico_** no _menu comutadores virtuais_ selecione a opção 'Novo comutador de rede virtual'
1. Em **Criar comutado virtual**

   1. selecione o tipo de comutador virtual que deseja criar:

      - **Externo** (Bridge)

        Cria um comutador virtual que se associa ao adaptador de rede físico de forma que as máquinas virtuais possam acessar uma rede fisica.

      - **Interno** (Rede NAT)

        Cria um comutador virtual que só pode ser usado pelas máquinas 'virtuais em execução neste computador físico e entre as máquinas virtuais e o computador físico. Um comutador virtual interno não fornece conectividade para conexão de rede fisica.

      - **Particular** (NAT)

        Cria comutador virtual que só pode ser usado pelas máquinas virtuais que são executadas nesse computador físico.

   1. Clique no botão 'Criar Comutador Virtual'

1. Em **Propriedades do comutador virtual**,

   1. No campo _Nome:_, dê um nome ao 'novo comutador virtual'.
   1. Em _Tipo de conexão_, selecione qual placa de rede instalada no computador físico deseja utilizar.
   1. Clique no botão 'aplicar'.
   1. Quando solicitado _Aplicar Alterações de Rede_, clique no botão 'Sim'.

### Criando uma VM (Máquina Virtual)

1. Em **Gerenciador do Hyper-v** no menu da esquerda selecione item com o nome do _computador físico_
1. No menu de **Ações** à direita, clique na opção 'Novo > Máquina Virtual'
1. Em **Assistente de Nova Máquina Virtual**,

   1. **Antes de Começar**, leia as recomendações e clique em 'Avançar'.
   1. **Especificar Nome e Local**, dê um nome à nova Máquina Virtual e clique em 'Avançar'.
   1. **Especificar Geração**, selecione a geração desejada e clique em 'Avançar'.

      - [***] Algumas versões de linux exigem que seja selecionado a geração 2.

   1. **Atribuir Memória**, no campo _Memória de inicialização_ digite o valor desejado e clique em 'Avançar'.
   1. **Configurar Rede**, no campo _Conexão_ selecione qual comutador de rede deseja utilizar e clique em 'Avançar'.
   1. **Conectar Disco Rígido Virtual**

      - **Criar um disco Rígido Virtual**  
        Use esta opção para criar um disco rígido virtual de expansão dinâmica VHDX.

        1. Dê um nome ao _novo disco rígido virtual_ a ser criado
        1. Selecione o local onde sera salvo o _novo disco rígido virtual_
        1. Selecione o tamanho de armazenamento do _novo disco rígido virtual_ em GB (Máximo: 64TB)
        1. Clique em 'Avançar'.

      - **Usar um disco virtual existente**  
        Use esta opção para anexar disco rígido virtbual existente, no formato VHD ou VHDX.

        1. Selecione o local do _disco rígido virtual existente_
        1. Clique em 'Avançar'.
        1. **Opções de instalação**
           - **Instalar um sistema operacional mais tarde**
             1. Clique em avançar.
           - **Instalar um sistema operacional a partir de um arquivo de imagem**
             1. Insira o caminho do arquivo .ISO
             1. Clique em avançar.
           - **Instalar um sistema operacional em un servidor de instalação baseado em rede**
             1. Clique em avançar.

      - **Anexar um _disco rígido virtual_ mais tarde**  
        Use esta opção para ignorar agora esta etapa e anexar, mais tarde, um disco rígido virtual existente.

        1. Clique em 'Avançar'.

   1. **Resumo**
      _Assistente de Nova Máquina Virtual_ concluído com êxito, Você está prestes a criar a máquina virtual a seguir.

      1. Confirme as informações do resumo:

         Descrição:  
          |||
         |---|---|
         |Nome:|Nova Máquina Virtual|
         |Geração:| Geração 1|
         |Memória:|4096 MB|
         |Rede:|Rede Privada Nome da Rede|
         |Disco Rígido:|C:\Users\Public\Documents\Hyper-V\Virtual Hard Disks\Nova Máquina Virtual.vhdx (VHDX, expansão dinâmica)|
         |Sistema Operacional:|Será instalado de C:\Caminho da ISO\Sistema Operacional.iso|

      1. Clique no botão 'Concluir'

1. A _Nova Máquina Virtual_ vai aparecer no painel central do **Gerenciador do Hyper-V** descrito como 'Máquinas Virtuais'
