# Sumário

- [Instalando o ELK](#1-instalando-o-elk)
  - [a. Configuração da maquina virtual](#a-configuração-da-máquina-virtual)
  - [b. Instalação do Elastic Search](#b-instalação-do-elasticsearch)
  - [c. Instalação do Kibana](#c-instalação-do-kibana)
  - [d. Instalação do LogStash](#d-instalação-do-logstash)
- [Iniciando um Script](#e-para-iniciar-um-script)
 
# 1. Instalando o ELK

[[github.com/StehMaria/]](https://github.com/StehMaria/Instala-o-ELK-Stack/blob/main/README.md): Como Instalar Elasticsearch, Logstash e Kibana no Ubuntu

O **ELK Stack** é uma ferramenta gratuita da **Elastic** com softwares para pesquisar, analisar e visualizar logs ajudando no monitoramento de equipamentos.

- Elasticsearch – Busca e analise, com ferramentas e filtros.

- Logstash – Processador de dados com pipelines que recebe transforma e envia dados simultâneos.

- Kibana – Visualizar dados do Elasticsearch através de gráficos e dashboards.

- Beats – Agentes que envia dados coletados para o Logstash ou Elasticsearch.

## a. Configuração da máquina virtual

Para utilizar o ELK Stack, vamos configurar uma **máquina virtual** com as seguintes configurações:

- ISO: Ubuntu Server (v. 22.04) - disponível em: [[ubuntu.com/download/]](https://ubuntu.com/download/server)
- RAM: 6GB
- 2 CPU
- Sistema: 64bits
- HD: VHD
- Video 64MB

![](./img/VM_conf01.png)
![](./img/VM_conf02.png)
![](./img/VM_conf03.png)
![](./img/VM_conf04.png)
![](./img/VM_conf05.png)
![](./img/VM_conf06.png)
![](./img/VM_conf07.png)

caso seja necessário utilize o tutorial a seguir:  
[[tecnoblog.net/]](https://tecnoblog.net/responde/como-criar-uma-maquina-virtual-virtualbox/): Como criar uma máquina virtual com o VirtualBox [20 passos]

## a. Instalando SO:

- Language: English
- Update: Continue Without updating
- Keyboard:

- [cancel update and reboot]

- reinicie se necessário
  Ocorreram alguns travamentos durante a instalação do SO resolvidos apenas reiniciando a VM.

* Pressione enter
  Após o reinício foi necessário pressionar enter para ser solicitado username e password

* Quando solicitado digite username e password configurado

## b. Instalação do Elasticsearch

[<h6>[voltar]</h6>](#sumário)

[[www.digitalocean.com/]](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-18-04-pt): Como Instalar e Configurar o Elasticsearch no Ubuntu 18.04
Para fazer a instalação do Elasticsearch no Ubuntu Server:

1. Importe a **chave GPG pública** do Elasticsearch para o APT, executando o comando a seguir:

```BASH
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
```

OU

```BASH
curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
```

2. Atualize os pacotes e instale o transport-https:

Este transporte do APT permite o uso de repositórios acedidos via HTTP Secure protocol (HTTPS), também chamado de HTTP sobre TLS. Está disponível por predefinição desde o apt 1.5 e estava disponível antes no pacote [apt-transport-https](https://manpages.ubuntu.com/manpages/focal/pt/man1/apt-transport-https.1.html). Note que um transporte nunca é chamado directamente por um utilizador mas usado pelas ferramentas do APT com base na configuração do utilizador.

HTTP é por si próprio um protocolo de transporte não encriptado (comprove apt-transport- http(1)), o qual, sendo indicado pelo S acrescentado, fica embrulhado numa camada encriptada conhecida por Transport Layer Security (TLS) para disponibilizar encriptação fim-para-fim. Um atacante com habilidades suficientes pode mesmo assim observar os colegas de comunicação e uma análise mais profunda à comunicação encriptada pode mesmo assim revelar detalhes importantes. Uma visão geral sobre métodos de transporte disponíveis alternativos é dada em sources.list(5).

```BASH
sudo apt-get install apt-transport-https
```

3. Adicione a lista de origens da Elastic ao diretório sources.list.d, onde o APT irá procurar por novas origens:

Os componentes do Elasticsearch não estão disponíveis nos repositórios de pacotes padrão do Ubuntu. No entanto, eles podem ser instalados com a APT após adicionar a lista de origem do pacotes do Elastic.

Todos os pacotes são assinados com a chave de assinatura do Elasticsearch para proteger seu sistema de **spoofing de pacotes**. Os pacotes autenticados usando a chave serão considerados confiáveis pelo seu gerenciador de pacotes. Neste passo, você importará a chave GPG pública do Elasticsearch e adicionará a lista de origem de pacotes do Elastic para instalar o Elasticsearch.

Para começar utilize o cURL, a ferramenta de linha de comando para transferir dados com URLs, para importar a chave GPG pública do Elasticsearch para o APT. Observe que estamos usando os argumentos -fsSL para silenciar todo o progresso e possíveis erros (exceto para uma falha de servidor) e permitir que o cURL faça uma solicitação em um novo local se for redirecionado. Faça o pipe da saída do comando cURL no programa apt-key, que adiciona a chave pública GPG para o APT.

```BASH
echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
```

- Como remover itens da lista?
  Caso seja necessário remover itens dessa lista utilize o comando a seguir

```BASH
sudo nano /etc/apt/sources.list.d/elastic-7.x.list
```
[[vivaolinux.com.br/artigo/]](https://www.vivaolinux.com.br/artigo/Introducao-ao-Linux-O-editor-de-texto-Nano): Introdução ao Linux: O editor de texto Nano  

![nano sourceList](./img/elk/ELK_NanoSourcesList.png)
É recomendado que se comente o item, adicionando # no inicio da linha, e não apaga-lo caso seja necessário reverter é só descomentar, ou seja, remover a # do inicio da linha.

4. Atualize a lista de pacotes do APT:

[[www.cyberciti.biz/]](https://www.cyberciti.biz/faq/what-does-sudo-apt-get-update-command-do-on-ubuntu-debian/): O que o comando sudo apt-get update faz no Ubuntu/Debian?

O comando `sudo apt-get update` é usado para baixar informações do pacote de todas as fontes **configuradas**.

As fontes geralmente são definidas no arquivo `/etc/apt/sources.list` e outros arquivos no diretório `/etc/apt/sources.list.d`.

Portanto, quando você executa o comando update, ele baixa as informações dos pacotes da Internet.

É uma boa prática, sempre que possível, efetuar essa verificação dos pacotes e suas dependências utilizando o comando:

```BASH
sudo apt update
```

```BASH
sudo apt upgrade
```

5. Instale o Elasticsearch:

<font color="yellow">Caso tenha outra versão do elasticsearch já instalada basta executar o comando a seguir para remover: </font>  

```BASH
sudo apt remove elasticsearch
```

Para instalar execute o comando:  
```BASH
sudo apt install elasticsearch
```

6. Faça algumas alterações no arquivo abaixo, descomentando as seguintes linhas:

```BASH
sudo nano /etc/elasticsearch/elasticsearch.yml
```

  node.name: node-1
  network.host: 0.0.0.0
  discovery.seed_hosts: ["127.0.0.1"] 
  cluster.initial_master_nodes: ["node-1"]


7. Carregue o Elaticsearch no servidor:

```BASH
sudo /bin/systemctl daemon-reload
```

```BASH
sudo /bin/systemctl enable elasticsearch.service
```

```BASH
sudo /bin/systemctl start elasticsearch.service
```

```BASH
sudo systemctl enable elasticsearch.service
```

```BASH
sudo systemctl status elasticsearch
```

```BASH
curl -X GET "http:localhost:9200"
```

## C. Instalação do Kibana:

1. Atualize os pacotes:

```BASH
sudo apt update
```

2. Instale o kibana

```BASH
sudo apt install kibana
```

3. Realize as alterações no arquivo kibana.yml:

```BASH
nano /etc/kibana/kibana.yml
```

- server.port: 5601

- server.host: "0.0.0.0"

- elasticsearch.hosts["http://127.0.0.1:9200"]

4. Inicie o serviço no servidor:

```BASH
sudo /bin/systemctl daemon-reload
```

```BASH
sudo /bin/systemctl start kibana.service
```

```BASH
sudo systemctl enable kibana.service
```

```BASH
sudo systemctl status kibana
```

## d. Instalação do Logstash

1. Instale o Logstash:

```BASH
sudo apt install logstash
```

2. Entre na pasta e inicie o serviço:

```BASH
cd /etc/logstash/
```

```BASH
sudo /bin/systemctl start logstash
```

```BASH
sudo systemctl enable logstash
```

```BASH
sudo systemctl status logstash
```

## e. Para iniciar um script

```BASH
cd /usr/share/logstash
```

```BASH
sudo /bin/logstash -f /etc/logstash/nome_do_arquivo.conf
```

# [![Home][homeimage]][homelink] [![Top][topimage]](#)

[topimage]: https://img.shields.io/badge/-Voltar_ao_topo-grey
[homeimage]: https://img.shields.io/badge/-Home-blue
[homelink]: ./../../../README.md#
