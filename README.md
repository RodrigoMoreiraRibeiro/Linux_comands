# Linux_comands

xargs kill -9 = mata os processos, sendo puxado somente o ID com o awk anteriormente

ps -ef | grep <service> | grep -v 'grep' | awk '{print $columnumber}' | xargs kill -9 = comando completo para mata todos processos do servico

tar -czvf  <nome do arquivo>.tar.gz <caminho para compactar>
c = criar
z = compactar
v = verbose
f = arquivo
x = extrair

tar -czvf  <nome do arquivo>.tar.gz -C <caminho para extrair>

zip -r(indicar se for diretorio) <nome do arquivo> <localparasalvar>

useradd no ubuntu nao cria o diretorio /home

curl -o /dev/null -s -w "%{http_code}\n" "https://ws.stf.jus.br/servico-intercomunicacao-2.2.2/intercomunicacao?wsdl"

cp -r * /var/www/html/ = copiar tudo do local atual, incluindo diretorios


wget -q -P /tmp/webservice https://www.tooplate.com/zip-templates/2136_kool_form_pack.zip = wget nao interativo

cat <<EOT 

texto
de
multiplas
linhas
com UTF-8 e $

EOT

mysql -u user -psenha -e "Query SQL"

tracert <url> = verifica as rotas da url

netstat -antp = verifica as portas na maquina

nmap <ipmaquina> = verifca também quais portas estão abertar e tras o endereço mac

dig <url> = verifica se o DNS esta funcionando ou nao 

route -n = mostrara os gateways

arp = volta todos endereços mac atrelado a maquina

mtr [url] = verifica a rota em tempo real 

telnet <ip porta> = verifica se a porta esta aberta no devido IP

ss -tunlp = verificacao de rede 

:se nu = dentro do VIM mostra o numero de linhas escritas

Se for passado somente $1, $2 no script, a variavel pode ser usada na hora de rodar o script como um arg
por exemplo: wget $1   ./script.sh http://www.lorem.com

echo $? = verifica se o ultimo comando foi bem sucedido ou nao
127 = erro no comando
1 = erro no arg
0 = normal

read -p 'Username: ' USR = tipo um input
read -sp 'Password: ' pass = um input mas com -s para nao mostrar oq esta sendo digitado


:undo = desfaz todas alteracoes

scp <arquivo> user@0.0.0.0:/tmp/

yum/apt search <pacote>
