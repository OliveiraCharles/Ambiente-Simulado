# Configuração - Máquinas (Hyper V - Servidor)


1) certificar-se de estar na mesma LAN que o servidor ter um ip fixo pertencente a rede /24
2) abrir o VSCode como administrador
3) abrir no VSCode o aquivo C:\Windows\System32\drivers\etc\hosts
4) na ultima linha escrever "192.168.1.100       LENOVO" e salvar
5) procurar por "Gerenciador de Credenciais" na barra de pesquisar do windows
6) clicar em "adicionar uma credencial do windows"
7) colocar o nome como "LENOVO" o usuario como "Administrator" e a senha como "Lenovo@2022##"
8) abrir o powershell como administrador
9) dar os seguintes comandos:
	Get-NetConnectionProfile
	Get-NetConnectionProfile | Set-NetConnectionProfile -NetworkCategory Private
	Get-NetConnectionProfile
	Enable-PSRemoting
	Get-Item WSMan:\localhost\Client\TrustedHosts
	Set-Item WSMan:\localhost\Client\TrustedHosts -Value "LENOVO,192.168.1.100"
	S
	Get-Item WSMan:\localhost\Client\TrustedHosts
10) se o hyperV estiver aberto feche e abra-o de novo
11) conecte no servidor cujo nome é "LENOVO" e pronto!


EXPLICAÇÃO:
	No passo 1 vc esta ficando com ipv4 compativel com a rede onde a LAN do servidor esta
	
	No passo 2, 3 e 4 você está dizendo para o computador qual IP ele precisa entender quando você escrever "LENOVO" é tipo um DNS proprio só dentro da maquina, se estiver sem 		previlegio de administrador nao conseguira editar o arquivo.

	No passo 5, 6 e 7 você esta cadastrando a credencial com a qual irá efetuar login no servidor.
	
	No passo 8 e 9 você efetua alguns comandos. Primeiro verifica o tipo de conexão de rede. Depois seta a conexão como "privada" e verifica de novo se alterou. Com o "enable" você ativa vários serviços relacionados a acesso remoto no windows. Depois busca na tabela de hosts confiaveis quem está la, então adiciona o servidor como confiavel, aceita, e por fim verifica de novo se realmente foi adicionado.

	Os passos 10 e 11 são os de finalização.


	Só seguir tudo que é sucesso!
