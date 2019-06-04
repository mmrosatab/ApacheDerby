# ApacheDerby

Este repositório se destina ao estudo do Apache Derby, gerenciador de banco de dados Java. O repositório contém instruções básicas para a instalação e utilização do Apache Derby no Eclipse, bem como uma pequena aplicação que faz acesso a um banco da dados.

Download Derby Versão 10.14.2.0
https://db.apache.org/derby/releases/release-10.14.2.0.cgi

# Instalando e configurando Apache Derby para uso externo (Apache Derby DB no Eclipse)

1 - Baixe a pasta compactada do apache derby e a descompacte (aqui foi usada a versão 10.14.2.0).

2 - Crie um projeto java.

3 - Crie uma pasta dentro do projeto java e copie para esta página o arquivo Derby.jar que está contido na pasta lib dentro da pasta de download do Apache Derby que você baixou.

4 - Para adicionar uma nova definicação de driver vá em: Window->Preferences->Data Management->Connectivity->DriverDefinitions. Clique em add, em Database escolha Derby Embedded JDBC Driver (versão 10.2) .  Em Jar List clique me Add Jar e selecione o caminho onde o Derby.jar esta em seu projeto java. Em Properties defina o nome do bando de dados e a senha.

5 - Altere a persctiva para banco de dados indo em Window->Persperctive->Open Perspective->Other->Database Development.

6 - Vá em Database Conections, clique com botão direito do mouse, selecione new, selecione um local/pasta para armazenar o banco, coloque o nome e a senha que você definiu no item 4. Deixe a box de save password ativada, clique em next e depois em 
finish e aguarde a configuração. Ao finalizar o banco de dados já estará conectado.

7 - Retorne para perspectiva Java.

8 - Crie outra pasta dentro do projeto java para armazenar um script sql.

9 - Crie um arquivo do tipo sql dentro desta pasta de script criada clicando com o botão direito sobre a pasta, indo em: new -> other -> SQL Development -> SQL File -> next, defina o nome do arquivo com extensao sql (ex: sc.sql), em database server type selecione: Derby_10x, escolha o nome da conexão e o nome do banco de dados que vc definiu nas etapas anteriores e clique em finish.

10 - Retorne a perspectiva Database Development, digite os comandos sql no arquivo de script criado (sc.sql), clique com botão direito do mouse sobre a área do arquivo de script sql aberto e selecione a opção execute all. Sua query será executada.

![derbyscreenshot](https://user-images.githubusercontent.com/9852787/55071764-4242b680-5068-11e9-9e22-b8c52821618d.png)


# Utilizando o Apache Derby através da aplicação Java

** (Vá na perspectiva Database Development e desconecte o banco da dados antes de executar a aplicação caso contrário resultará em erro)

Antes de criar as classes java para o acesso ao bando de dados, sete o classapath.

1 - clique com botão direito do mouse em cima da pasta projeto no eclipse e selecione "properties" 

2 - Vá em: resources->java build path-> libraries.

3 - Clique em "classpath".

4 - Clique em "add jar's".

5 - Selecione o caminho ate o derby.jar em seu projeto.

6 - Clique em "apply e close".

7 - Crie as classes e seja feliz.

![screenshot1](https://user-images.githubusercontent.com/9852787/55071332-21c62c80-5067-11e9-8c5a-9a2711c17dc5.png)
![screenshot2](https://user-images.githubusercontent.com/9852787/55071338-24c11d00-5067-11e9-9ceb-05e57b0deb90.png)
