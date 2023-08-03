# docker-nginx-api-cpf

Criada uma instância na AWS com Amazon Linux.

1 -  Atualizando o sistema e instalando o Docker.

1.1 Feito o update no sistema..
$sudo yum update -y
1.2 Instalado Docker na instância.
$sudo yum install docker -y
1.3 Start no serviço Docker.
$sudo service docker start

2 - Baixando imagem docker do nginx.

$docker pull nginx

 3 - Criar pasta app e criar arquivo index.html com site do api cep  (https://viacep.com.br/exemplo/jquery/)
 
$mkdir app 

4 - Criando container  

$ docker container run -d -p 80:80 --name cpf -v /home/ec2-user/app:/usr/share/nginx/html/ nginx
