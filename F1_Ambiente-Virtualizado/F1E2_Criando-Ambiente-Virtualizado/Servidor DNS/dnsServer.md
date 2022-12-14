## O passo a passo completo da configuração do Servidor DNS utilizando o Ubuntu Server é encontrado em: 
* Bóson Treinamentos: Instalação e configurações gerais de rede no Ubuntu - 01 - https://www.youtube.com/watch?v=0SSSfyy7bO4

* Bóson Treinamentos: Servidor DNS - Criação das Zonas e Testes com clientes - Linux Ubuntu -02 - https://www.youtube.com/watch?v=xZcf7TaxKHU


## Tutorial referente aos principais conceitos da configuração do Servidor DNS no Ubuntu 16.04

Para fazer a configuração do servidor DNS afim de realizar a tradução dos nomes dos hosts da rede interna, foi utilizada a distribuição Ubuntu Server 16.04 e o servidor para o protocolo DNS chamado de Bind na versão 9. 

A instalação do servidor DNS Bind9 é extremamente simples, basta digitar o seguinte comando:

```bash
apt install bind9
```

### Configurar IP estático para o Ubuntu DNS Server
Para realizar essa configuração tem de editar o arquivo "interfaces", que está localizado em "/etc/network/interfaces. Configurando o ip estático, máscara, rede, endereço de broadcast e gateway.

Após a configuração da interface, devemos editar o arquivo "/etc/hosts". Colocando o endereço IP do Servidor DNS (172.22.22.200) e o domínio (sx-dns.jedi.com). Em seguida foram criadas duas zonas, uma de pesquisa direta e outra de reversa.

### Criação dos arquivos de Zona de pesquisa direta e Reversa

Na sequência foram criados os arquivos para a zona direta e reversa e então foram feitas as edições nos mesmos afim de preenchê-los com o nome do domínio criado assim como o preenchimento de todos os hosts da rede interna e seus respectivos nomes para que o servidor DNS consiga fazer a tradução dos seus nomes no endereço IP referente a cada um desses hosts. 

### Configurações dos Hosts da Rede

Após toda a configuração do servidor DNS, foram feitas configurações nos hosts da rede para que apontem para o Ubuntu Server quando necessitarem da tradução dos nomes, colocando como nameserver o endereço IP do Ubuntu (172.22.22.200) e como search o nome do domínio (jedi.com). 
