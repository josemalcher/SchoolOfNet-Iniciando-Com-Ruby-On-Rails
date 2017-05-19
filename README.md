# SchoolOfNet-Iniciando-Com-Ruby-On-Rails

Resumo do curso:

https://www.schoolofnet.com/curso-iniciando-com-ruby-rails/

---

## <a name="indice">Índice</a>

- [Introdução](#parte1)
- [Instalação](#parte2)
- [O que é ruby on rails](#parte3)
- [Arquitetura MVC](#parte4)
- [Criando projeto rails](#parte5)
- [Hello world](#parte6)
- [Rails console](#parte7)
- [ActiveRecord](#parte8)
- [Trabalhando com models](#parte9)
- [Migrations](#parte10)
- [Trabalhando com controllers](#parte11)
- [Um pouco sobre rotas](#parte12)
- [Validando model](#parte13)
- [Scaffold](#parte14)
- [Finalizando](#parte15)


---

## <a name="parte1">Introdução</a>


Referências Boas

[Ruby on Rails - coloque sua aplicação web nos trilhos](https://www.casadocodigo.com.br/products/livro-ruby-on-rails)

[Desenv. Ágil para Web com Ruby on Rails](https://www.caelum.com.br/apostila-ruby-on-rails/)

[Aprendendo Ruby e Rails, Livros e Guias](http://www.akitaonrails.com/2014/07/13/aprendendo-ruby-e-rails-livros-e-guias)

[Voltar ao Índice](#indice)

---

## <a name="parte2">Instalação</a>

[railsinstaller](http://www.railsinstaller.org/pt-BR)

[Configurando Ruby, Rails, MySQL e Git no Windows](https://nandovieira.com.br/configurando-ruby-rails-mysql-e-git-no-windows)

[RubyGems](https://rubygems.org/)


[Voltar ao Índice](#indice)

---

## <a name="parte3">O que é ruby on rails</a>

Ruby on Rails é um framework livre que promete aumentar velocidade e facilidade no desenvolvimento de sites orientados a banco de dados (database-driven web sites), uma vez que é possível criar aplicações com base em estruturas pré-definidas. Frequentemente referenciado como Rails ou RoR, o Ruby on Rails é um projeto de código aberto escrito na linguagem de programação Ruby. As aplicações criadas utilizando o framework Rails são desenvolvidas com base no padrão de arquitetura MVC (Model-View-Controller). [wikipédia - Ruby on Rails](https://pt.wikipedia.org/wiki/Ruby_on_Rails)

[Introdução ao Framework Ruby on Rails](http://www.devmedia.com.br/introducao-ao-framework-ruby-on-rails/31285)

Ruby on Rails é um framework que faz o desenvolvimento, implantação e manutenção de uma aplicação web mais fácil e esse utiliza uma linguagem orientada à objeto conhecida como Ruby. Para introduzi-lo é preciso que o desenvolvedor conheça algumas de suas filosofias. Essas são:

- DRY-Don't Repeat Yourself: Em português "Não repita você mesmo", significa que enquanto o desenvolvimento no Rails tem a mesma parte do código, ou o mesmo propósito em entidades diferentes, isso quer dizer que existe uma melhor maneira de escrever sua aplicação;
- Convention over Configuration: Em português "Convenção antes de Configuração", significa que invés de determinar a configuração, Rails possui convenções estruturais e nomeadas que implementam o often-cited principle of least surprese(POLS) ;
- Less Software: Em português "Menos Software", significa utilização de mais convenções, menos códigos, menos complexidades e, consequentemente, menores quantidades de bugs;

O desenvolvimento das aplicações em Rails são implementadas usando oMODEL-VIEW-CONTROLLER, mais conhecido como arquitetura MVC e trabalhado com as bibliotecas Active Record, Action View e Action Controller. Estes serão citados abaixo no artigo.

[Voltar ao Índice](#indice)

---

## <a name="parte4">Arquitetura MVC</a>

O Modelo MVC
Esse padrão de arquitetura utilizada divide a aplicação logicamente em três categorias: modelo, vista e controle (Model-View-Controller). Cada parte do padrão MVC é uma entidade capaz de ser construída e testada separadamente. O modelo representa os dados, a vista representa a interface do usuário e o controle comanda as ações, ou seja, o modelo(model) é a informação que a aplicação trabalha, a vista (view) é a representação e o controle (controller) é o diretor da interação entre eles.

O ciclo dessa estrutura começa quando o usuário interage com a interface (view) e chama um evento; o controller recebe o chamado da view e acessa o model, atualizando frequentemente a interface.

[O Modelo MVC](http://www.devmedia.com.br/introducao-ao-framework-ruby-on-rails/31285)

O primeiro é MVC, que significa Model View Controller. Explicando de forma bem simplista:

- Model: modelo dos dados, normalmente um banco de dados, mas é mais que só interface com BD. O recomendado é que toda regra de negócio fique nele. Por exemplo, numa loja, ao gravar um novo pedido, o modelo faz todo o cálculo de frete, checagem de estoque, processamento de pagamento etc.  
- View: como os dados serão vistos e como alguém pode interagir com esses dados, normalmente páginas HTML com forms.  
- Controller: é quem interpreta eventos que acontecem na View e manipula os dados que estão no Model, normalmente são ações como listar, procurar, alterar, inserir e deletar dados.

[MVC e Ruby on Rails, uma visão simplificada](http://blog.locaweb.com.br/artigos/tecnologia/mvc-e-ruby-on-rails-uma-visao-simplificada/)


<img src="https://betterexplained.com/wp-content/uploads/rails/mvc-rails.png" alt="MVC" />

[Intermediate Rails: Understanding Models, Views and Controllers](https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)


[Voltar ao Índice](#indice)

---

## <a name="parte5">Criando projeto rails</a>

```
$ rails new [nome-projeto]
```

Para utilizarmos o Rails, é necessário instalar a gem rails em nossa máquina através do comando gem install:

```
gem install rails
```

O comando acima, instalará a última versão estável do Rails. Caso queira, é possível também instalarmos uma versão específica passando-a conforme abaixo:

```
gem install rails -v=4.0.0
```

Após a instalação da gem rails em nossa máquina, ganhamos o comando que iremos utilizar para gerar os arquivos iniciais de nossa aplicação. Como a maioria dos comandos de terminal, podemos passar uma série de informações para que o projeto gerado seja customizado.

Para conhecer mais sobre as opções disponíveis, podemos imprimir a ajuda no console. Para isso basta executar o seguinte comando:

```
rails --help
```
Atualmente o Rails está na versão 4, que é a versão utilizada no curso. Caso queira saber a versão do Rails instalada na máquina, é só rodar o comando:

```
rails --version
```

O Rails já vem com inúmeros scripts prontos para tornar a vida do programador mais fácil criando tudo que for necessário para desempenhar uma determinada tarefa. Estes scripts são chamados de geradores e um destes é o gerador new, que proporciona a criação da estrutura base de uma aplicação Rails. Para usá-lo, é só digitar no terminal o seguinte comando:

```
rails new [caminho-da-app]
```

Caso a pasta apontada como caminho da aplicação não exista, ela será criada pelo gerador do Rails. Caso a pasta exista e contenha arquivos que possam conflitar com os gerados pelo Rails será necessário informar a ação adequada (sobrescrever, não sobrescrever) para cada um deles durante o processo de geração de arquivos.

O comando new suporta algumas opções a serem passadas no momento em que é chamado. Para visualizar todas as opções aceitas é só executar:

```
rails new -h
```

Dentre todas as opções, uma das mais úteis é a que prepara nossa aplicação para conexão com um banco de dados. Como o Rails é compatível com uma grande quantidade de bancos de dados podemos escolher aquele que temos mais familiaridade, ou um que já estiver instalado em nossa máquina. Por padrão o Rails usa o SQLite3 pois é bem simples, versátil e consegue se comportar bem em um ambiente de desenvolvimento, além de possibilitar que as informações sejam salvas em qualquer local do sistema de arquivos (por padrão dentro da aplicação) e está disponível para Windows, Mac e Linux.

Caso queira utilizar, por exemplo, o MySQL, basta passar a opção:

```
rails new meu_projeto -d mysql
```

[6.4 - Criando um novo projeto Rails](https://www.caelum.com.br/apostila-ruby-on-rails/ruby-on-rails/#6-4-criando-um-novo-projeto-rails)

Cada diretório tem uma função específica e bem clara na aplicação:

- app - A maioria dos arquivos específicos da nossa aplicação ficam aqui (inclusive todo o MVC, dividido em diretórios);
- bin - Executáveis do Rails e das gems instaladas;
- config - Configurações da aplicação;
- db - Migrações, esquema e outros arquivos relacionados ao banco de dados;
- doc - Documentação do sistema;
- lib - Bibliotecas auxiliares;
- log - Informações de log;
- public - Arquivos estáticos que serão servidos pela WEB;
- test - Testes da nossa aplicação;
- tmp - Arquivos temporários como cache e informações de sessões;
- vendor - Dependências e bibliotecas de terceiros.

[6.6 - Estrutura dos diretórios](https://www.caelum.com.br/apostila-ruby-on-rails/ruby-on-rails/#6-6-estrutura-dos-diretorios)


[Voltar ao Índice](#indice)

---

## <a name="parte6">Hello world</a>

```ruby
rails generate controller hello
```

Criar o index.html.erb

Adiiconar no Ccntrolador 

```ruby
class HelloController < ApplicationController
  def index
  end
end

```

e adicionar a rota da página

```ruby
Rails.application.routes.draw do

  get 'hello/index'

end

```

Start no Servidor 

```ruby
rails server

# ou rails s
```

Erro ao executar:
```
ExecJS::ProgramError in Hello#index
TypeError: O objeto não dá suporte para a propriedade ou método
<%= csrf_meta_tags %>

    <%= stylesheet_link_tag    'application', media: 'all', 'data-turbolinks-track': 'reload' %>
    <%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>
  </head>
```

Solução:

Remover as linhas de /assets de aplication.js e .css
```
//= require rails-ujs
//= require turbolinks
//= require_tree .
e
 *= require_tree .
 *= require_self
```

[TypeError: Object doesn't support this property or method](http://stackoverflow.com/questions/29838237/typeerror-object-doesnt-support-this-property-or-method)


[Voltar ao Índice](#indice)

---

## <a name="parte7"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte8"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte9"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte10"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte11"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte12"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte13"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte14"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte15"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte16"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte17"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte18"> </a>

[Voltar ao Índice](#indice)

---