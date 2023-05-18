# Anotações Importantes

- Iniciando o projeto ``npm init -y``
- Aqui foi instalado o nodemon ``npm install nodemon@2.0.15``
- Adicionado o seguinte Script no arquivo package.json ``"dev": "nodemon server.js"``
- Para rodar o projeto: ``nodemon server.js``
- Para auxiliar nas rotas: ``npm install express``

Você pode usar o <a href="https://expressjs.com/pt-br/starter/generator.html">Express Application Generator</a> para criar um “esqueleto” para aplicações Express. 
A instalação é realizada via NPM (Node Package Manager ou seja, o Gerenciador de Pacotes do Node). Pode-se usar o parâmetro -g para instalar o pacote globalmente, ou seja, você pode acessá-lo de qualquer lugar do computador:

````js
npm install express-generator -g
````

Depois da instalação, vá até o local/pasta onde você deseja desenvolver o projeto e escreva a seguinte linha de comando abaixo, indicando express <nome do projeto a ser criado>:

````js
express olamundo
````
No terminal, já terá a orientação para navegar até a pasta criada e instalar os pacotes com npm install.

````js
change directory:
    > cd olamundo
install dependencies:
    > npm install
````
Vamos fazer esses dois passos e depois iremos usar o comando ``npm start`` para iniciar a aplicação. Observe que ao digitar o endereço http://localhost:3000 no navegador, ele já vai exibir uma mensagem.

Essa implementação pode ser vista nos arquivos index.js e users.js dentro da pasta routes.
## Detalhando alguns atributos

- Name: é onde você define o nome pelo qual seu módulo será chamado;

- Version: cada vez que uma atualização do módulo é lançada é atribuído um conjunto de 3 números. os módulos trabalham com três níveis de versionamento seguindo um padrão chamado SemVer (Semantic Versioning), ou seja, versionamento semântico, onde 3 números separados por ponto correspondem, respectivamente, aos atributos Major, Minor e Patch. 

- Patch está relacionado a uma alteração que não quebra uma funcionalidade anterior e nem adiciona novas. Geralmente é usado para liberar alguma correção de bug. Minor é quando adicionamos uma nova funcionalidade, sem quebrar funcionalidades anteriores. Major é quando pode ocorrer uma quebra de compatibilidade. Por isso, é importante indicar a versão de forma adequada. Você pode ler mais sobre versionamento semântico <a href="https://semver.org/lang/pt-BR/">aqui</a>

- Description: define o que será este módulo. Ideal que seja uma descrição curta e clara sobre o objetivo principal;

- Main: define o ponto de entrada da aplicação;

- Scripts: essa sessão tem alguns scripts pré-definidos, mas você também pode definir os seus personalizados. Nesse <a href="https://docs.npmjs.com/cli/v8/using-npm/scripts">link</a> é possível ter acesso a algumas informações sobre os mesmos;

- Keywords: é um array de palavras-chave sobre o projeto;

- Author: são dados de autoria, pode conter nome, e-mail e site;

- License: é a licença escolhida para o projeto;

- Dependencies: define a lista de pacotes necessários para executar seu projeto num ambiente de produção; 

- DevDependencies: define a lista de pacotes necessários para executar o projeto num ambiente de desenvolvimento e testes. 

Existem outras configurações que podem existir nesse arquivo, como repositório do git, homepage, peerDependencies, entre outras que podem ser visualizadas na <a href="https://docs.npmjs.com/cli/v8/configuring-npm/package-json">documentação oficial</a> do NPM.

## O que é Npm?

 NPM é acrônimo de Node Package Manager ou Gerenciadores de Pacotes do Node.

## Mas o que são exatamente estes gerenciadores?

Gerenciadores de pacotes são repositórios de código aberto nos quais devs disponibilizam soluções para o uso da comunidade. Estas soluções nada mais são do que programas que outras pessoas desenvolveram e que utilizamos para ganhar tempo no desenvolvimento de nosso próprio código, e vão desde libs (bibliotecas pequenas e específicas) até frameworks com vários recursos prontos. E um pacote (ou módulo) - aqui podemos pensar em um pacote mesmo - que é como chamamos o conjunto do código que determinada lib ou framework utiliza para executar.

Algumas dessas bibliotecas são desenvolvidas por times para resolver algum problema específico que tiveram que enfrentar. Depois, elas são disponibilizadas para que outras pessoas com o mesmo contratempo aproveitem e também utilizem. Outras bibliotecas são disponibilizadas por empresas de software, que utilizam as plataformas dos gerenciadores, para a distribuição de suas soluções de código. E sendo de código aberto, isso significa que você também pode criar e publicar a sua lib para outras pessoas baixarem e instalarem em seus projetos.

## Instalação local vs global

Estes pacotes de código podem ser instalados localmente, estando disponíveis somente para o projeto no qual foi instalado através da pasta node_modules, e globalmente, sendo instalados em um diretório geral do NPM e ficando disponíveis para todos os projetos em seu computador, sem a necessidade de instalar separadamente em cada projeto.

Na maior parte das vezes, você vai utilizar a opção local, com os comandos npm install <nome do pacote> ou yarn add <nome do pacote>, pois fica mais fácil fazer o gerenciamento de versão das libs que utilizamos e muitas vezes, um pacote que instalamos “puxa” um ou vários outros pacotes auxiliares que ele precisa para funcionar. O ideal é não poluir o diretório global com libs que poderão ser utilizadas em somente um projeto.

Algumas libs e frameworks mais complexas vão solicitar que a instalação seja feita globalmente para funcionar. Sempre vale a pena consultar a documentação de cada uma! Para fazer uma instalação global de pacotes, utilizamos os comandos npm install -g <nome do pacote> ou yarn add global <nome do pacote>.

## Alguns Comandos

``install`` *Instala um novo módulo*
``list`` *Lista os módulos instalados*
``test`` *Executa o script de teste especificado no package.json*
``--global`` *Usado como um sinalizador para instalar um pacote globalmente (não só na pasta do projeto)*
``--save`` *Salva o módulo ao instalar*
``--save-exact`` *Salva o módulo ao instalar, porém na versão exata mencionada*
``--save-dev`` *Salva o módulo ao instalar, porém como uma dependência de desenvolvimento*
``npm help <nome do comando>`` *Para saber mais*

