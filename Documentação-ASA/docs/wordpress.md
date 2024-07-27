`Wordpress`


    Criação de dois sites, um no wordpress e outro no mkdocs.


    Sendo docs.conf estático é www.conf Dinámico .


Primeiro teve que criar um container para os sites neles foi feito a Criação de dois diretórios eles são : docs.conf é www.conf . os Comandos usados:


Criar container:

[![Captura de ecrã de 2023-11-03 12-00-14](https://i.im.ge/2023/11/03/yS50Ap.Captura-de-ecra-de-2023-11-03-12-00-14.png)](https://im.ge/i/yS50Ap)


Criar um diretório docs.conf é www.conf


[![Captura de ecrã de 2023-11-03 12-08-25](https://i.im.ge/2023/11/03/yS5Ge4.Captura-de-ecra-de-2023-11-03-12-08-25.png)](https://im.ge/i/yS5Ge4)


Feito isso depois vai fazer a configuração do wordpress instalando as dependências:
Comando usado:

[![Captura de ecrã de 2023-11-03 12-12-06](https://i.im.ge/2023/11/03/yS9qEc.Captura-de-ecra-de-2023-11-03-12-12-06.png)](https://im.ge/i/yS9qEc)
[![Captura de ecrã de 2023-11-03 12-14-05](https://i.im.ge/2023/11/03/yS96d9.Captura-de-ecra-de-2023-11-03-12-14-05.png)](https://im.ge/i/yS96d9)




Depois disso entra no diretório /usr/local/bin

[![Captura de ecrã de 2023-11-03 12-16-32](https://i.im.ge/2023/11/03/yS9gdp.Captura-de-ecra-de-2023-11-03-12-16-32.png)](https://im.ge/i/yS9gdp)
Nesse comando ele vai criar o wp-cli.phar que a configuração inicial do wordpress. Vamos agora renomear o arquivo wp-cli.phar para wp é dando permissão de execução .


comando pra dar permissão : chmod +x wp
[![Captura de ecrã de 2023-11-03 12-19-27](https://i.im.ge/2023/11/03/ySjTTS.Captura-de-ecra-de-2023-11-03-12-19-27.png)](https://im.ge/i/ySjTTS)


Agora é Criado um usuário pro Container:


Comando usado: adduser (nome)


    su - (nome) Para entrar no usuário

    Volta pro Container é entrar no Diretório /var/www/


Remove o Arquivo html do Diretório


comando :
[![Captura de ecrã de 2023-11-04 00-42-04](https://i.im.ge/2023/11/04/yaT6lf.Captura-de-ecra-de-2023-11-04-00-42-04.png)](https://im.ge/i/yaT6lf)


Depois é criado o arquivo html no Super usuário root .


Comandos:


[![Captura de ecrã de 2023-11-04 12-00-54](https://i.im.ge/2023/11/04/yaBRKm.Captura-de-ecra-de-2023-11-04-12-00-54.png)](https://im.ge/i/yaBRKm)


No usuário comum e Preciso fazer o mesmo comando .


Nesse comando e Criado o html é o wordpress .
[![Captura de ecrã de 2023-11-04 12-05-36](https://i.im.ge/2023/11/04/yaBVc0.Captura-de-ecra-de-2023-11-04-12-05-36.png)](https://im.ge/i/yaBVc0)




Agora é criado o Banco de Dados no Mariadb para o login no wordpress.


Na linha de comando é usado o comando Mysql .


    Criação do nome do banco de Dados:

[![Captura de ecrã de 2023-11-04 12-12-26](https://i.im.ge/2023/11/04/yaGyNx.Captura-de-ecra-de-2023-11-04-12-12-26.png)](https://im.ge/i/yaGyNx)




Criação do usuário pro banco de dados.

        user = Seu usuário
        senha = Sua senha

        create user ‘user’@’localhost’ identified by ‘senha’;

Dando Privilegios necessarios pro usuario.


[![Captura de ecrã de 2023-11-04 13-04-57](https://i.im.ge/2023/11/04/y7MJ2p.Captura-de-ecra-de-2023-11-04-13-04-57.png)](https://im.ge/i/y7MJ2p)




    Mkdocs

    listar mkdocs disponiveis pra instalação:


[![Captura de ecrã de 2023-11-06 11-36-01](https://i.im.ge/2023/11/06/y5ozur.Captura-de-ecra-de-2023-11-06-11-36-01.png)](https://im.ge/i/y5ozur)


instalação do mkdocs :


[![Captura de ecrã de 2023-11-06 11-38-06](https://i.im.ge/2023/11/06/y5Xouy.Captura-de-ecra-de-2023-11-06-11-38-06.png)](https://im.ge/i/y5Xouy)


Depois de ter feito isso já pode ser usado o code-server no navegador com o ip do container é a porta 8080.


Dentro do code e Criado arquivo chamado asa-doc:


[![Captura de ecrã de 2023-11-06 11-44-28](https://i.im.ge/2023/11/06/y5X79Y.Captura-de-ecra-de-2023-11-06-11-44-28.png)](https://im.ge/i/y5X79Y)


Dentro do code-server e configurado o site pra a documentação .


no terminal de permissoes para o usuario na pasta docs


[![Captura de ecrã de 2023-11-06 11-49-18](https://i.im.ge/2023/11/06/y5XC4L.Captura-de-ecra-de-2023-11-06-11-49-18.png)](https://im.ge/i/y5XC4L)


Dentro do code-server e feito o comando terminal:


[![Captura de ecrã de 2023-11-06 11-45-46](https://i.im.ge/2023/11/06/y5XxqG.Captura-de-ecra-de-2023-11-06-11-45-46.png)](https://im.ge/i/y5XxqG)


`Code Server`