# Sumário

- [Preparo do Ambiente](#preparo-do-ambiente)
  - [Baixando a ISO](#baixando-a-iso)
  - [Configurando o Hyper-V](#configurando-o-hyper-v)
- [Criação da VM](#criação-da-vm)
  - [Requisitos Mínimos](#requisitos-mínimos)
  - [Criando uma VM](#criando-uma-vm-máquina-virtual)
  - [Instalando a .ISO](#instalando-o-sistema-operacional-iso)
  - [Configurando o Sistema](#configurando-o-sistema)

## Preparo do ambiente

### Baixando a ISO

### Configurando o Hyper-V

1. [Habilite o Hyper-V](../Hyper-V/hyper-v.md)

## Criação da VM

### Requisitos mínimos

|                      |                                                                                                |
| -------------------- | ---------------------------------------------------------------------------------------------- |
| Artquitetura:        | 64 bits                                                                                        |
| Processamento:       | 1,4GHz                                                                                         |
| RAM:                 | 512MB \*(800MB durante a instalação)                                                           |
| Armazenamento:       | 32GB                                                                                           |
| Sistema Operacional: | Será instalado de C:\Users\...\ISO\Windows_Server_2016_Datacenter_EVAL_en-us_14393_refresh.ISO |
|                      |                                                                                                |

### Criando uma VM (Máquina Virtual)

1. Em **Gerenciador do Hyper-v** no menu da esquerda selecione item com o nome do _computador físico_
1. No menu de **Ações** à direita, clique na opção 'Novo > Máquina Virtual'
1. Em **Assistente de Nova Máquina Virtual**,

   1. **Antes de Começar**, leia as recomendações e clique no botão 'Avançar'.
   1. **Especificar Nome e Local**, dê um nome à nova Máquina Virtual e clique no botão 'Avançar'.
      - [ windows-server-2016 ]
   1. **Especificar Geração**, selecione a geração desejada e clique no botão 'Avançar'.

      - [x] Geração 1

      - [***] Algumas versões de linux exigem que seja selecionado a geração 2.

   1. **Atribuir Memória**, no campo _Memória de inicialização_ digite o valor desejado e clique no botão 'Avançar'.  
      Especifique a quantidade de memória a ser alocada na máquina virtual. É possível especificar uma quanbdade de 32MB até 251658240 MB. Para melhorar o desempenho, especifique mais do que o mínimo recomendado para o sistema operacional.
      - [4096]MB
   1. **Configurar Rede**, no campo _Conexão_ selecione qual comutador de rede deseja utilizar e clique no botão 'Avançar'.
      - Default Switch
   1. **Conectar Disco Rígido Virtual**

      - **Criar um disco Rígido Virtual**  
        Use esta opção para criar um disco rígido virtual de expansão dinâmica VHDX.

        1. Dê um nome ao _novo disco rígido virtual_ a ser criado
           - [ windows-server-2016.vhdx ]
        1. Selecione o local onde sera salvo o _novo disco rígido virtual_
           - [ C:\Users\Public\Documents\Hyper-V\Virtual Hard Disks\ ]
        1. Selecione o tamanho de armazenamento do _novo disco rígido virtual_ em GB (Máximo: 64TB)
           - [ 32 ] GB
        1. Clique no botão 'Avançar'.
        1. **Opções de instalação**

           - **Instalar um sistema operacional a partir de um arquivo de imagem**
             1. Insira o caminho do arquivo .ISO
                - [ C:\Users\...\ISO\Windows_Server_2016_Datacenter_EVAL_en-us_14393_refresh.ISO ]
             1. Clique no botão 'Avançar'.

   1. **Resumo**
      _Assistente de Nova Máquina Virtual_ concluído com êxito, Você está prestes a criar a máquina virtual a seguir.

      1. Confirme as informações do resumo:

         Descrição:

         |                      |                                                                                                         |
         | -------------------- | ------------------------------------------------------------------------------------------------------- |
         | Nome:                | windows-server-2016                                                                                     |
         | Geração:             | Geração 1                                                                                               |
         | Memória:             | 4096 MB                                                                                                 |
         | Rede:                | Default Switch                                                                                          |
         | Disco Rígido:        | C:\Users\Public\Documents\Hyper-V\Virtual Hard Disks\windows-server-2016.vhdx (VHDX, expansão dinâmica) |
         | Sistema Operacional: | Será instalado de C:\Users\...\ISO\Windows_Server_2016_Datacenter_EVAL_en-us_14393_refresh.ISO          |
         |                      |                                                                                                         |

      1. Clique no botão 'Conluir'

   1. A _Nova Máquina Virtual_ vai aparecer no painel central do **Gerenciador do Hyper-V** descrito como 'Máquinas Virtuais'

### Instalando o Sistema Operacional .ISO

1. Clique 2x na VM criada
1. Na janela de Conexão de Máquina Virtual clique no botão 'Iniciar'
   - Certifique-se que existe memória didponível no computador físico.
1. Selecione as opções de preferencia de linguagem Tempo e moeda corrente:

   - _Language to install:_ [English (United States)]
   - _Time and Currency format:_ [English (United States)]
   - _Keyboard or input method:_ [Portuguese (Brazil ABNT2)]  
     Clique no botão '_Install now_'.

1. Em **Windows Setup** selecione a versão do sistema operacional que deseja instalar:

   - **[ ] Windows Server 2016 Standars evaluation**
     ##### **Descrição:** Essa opção (recomendada) reduz o gerenciamento e a manutenção instalando apenas o que é necessário para executar a maioria das funções e aplicativos do servidor. Ele não inclui uma GUI, mas você pode gerenciar totalmente o servidor local ou remotamente com o Windows PowerShell ou outras ferramentas. Para obter mais detalhes, consulte "Opções de instalação do Windows Server".
   - **[ ] Windows Server 2016 Standard evaluation (Desktop experience)**
     ##### **Descrição:** Essa opção é útil quando uma GUI é necessária, por exemplo, para fornecer compatibilidade com versões anteriores de um aplicativo que não pode ser executado em uma instalação Server Core. Todas as funções e recursos do servidor são suportados. Para obter mais detalhes, consulte "Opções de instalação do Windows Server".
   - **[ ] Windows Server 2016 Datacenter evaluation**
     ##### **Descrição:** Esta opção (recomendada) reduz o gerenciamento e a manutenção instalando apenas o que é necessário para executar a maioria das funções e aplicativos do servidor. Ele não inclui uma GUI, mas você pode gerenciar totalmente o servidor local ou remotamente com o Windows PowerShell ou outras ferramentas. Para obter mais detalhes, consulte "Opções de instalação do Windows Server".
   - **[x] Windows Server 2016 Datacenter evaluation (Desktop experience)**
     ##### **Descrição:** Esta opção é útil quando uma GUI é necessária, por exemplo, para fornecer compatibilidade com versões anteriores para um aplicativo que não pode ser executado em uma instalação Server Core. Todas as funções e recursos do servidor são suportados. Para obter mais detalhes, consulte "Opções de instalação do Windows Server".
     Clique no botão '_Next_'.

1. Leia os termos de licença e se estiver de acordo marque a opção:
   [x] _I accept the licence terms_  
   Clique no botão '_Next_'

   ##### \*(pode ser necessário ler o termo de licença até o fim para liberar essa opção )

1. Selecione o tipo de instyalação desejada?

   - [ ] **Upgrade**: Install Windows and keep files, settings, and applications
     ##### Os arquivos, configurações e aplicativos são movidos para o Windows com esta opção. Esta opção só está disponível quando uma versão suportada do Windows já está em execução no computador.
   - [x] **Custom**: Install Windows only (advanced)
     ##### Os arquivos, configurações e aplicativos não são movidos para o Windows com esta opção. Se você quiser fazer alterações em partições e unidades, inicie o computador usando o disco de instalação. É recomendado fazer backup de seus arquivos antes de continuar.

1. Selecione em qual partição deseja instalar o windows

   |     | Name                      | Total size | Free space | Type |
   | --- | ------------------------- | ---------- | ---------- | ---- |
   |     | Drive 0 Unallocated Space | 32GB       | 32GB       |      |
   |     |                           |            |            |      |

   - Clique no botão '_Next_'

1. Aguarde as etapas seguintes:

   Installing Windows  
   Status:

   - Copying Windows files
   - **Getting files ready for installation** (5%)
   - Installing features
   - Installing updates
   - Finishing up

   ##### \*O sistema irá reiniciar algumas vezes

1. Digite uma senha para a conta interna de administrador que você usará para acessar este computador.

   - crie uma **senha segura**
   - repita a **senha segura**

   Clique no botão '_Finish_'

1. Pressione **Ctrl+Alt+Delete** para acessar o sistema
1. Insira a **senha segura** criada anteriormente

### Configurando o Sistema

1. Renomeie o Computador
1. Ajuste a Data e a Hora do Sistema
1. Defina o Endereço IPv4
