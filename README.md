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
- [Trabalhando com Views](#parte13)
- [Validando o Model](#parte14)
- [Scaffold](#parte15)
- [Finalizando](#parte16)


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

## <a name="parte7">Rails console</a>

Criando um novo controller uma função: 

```ruby
rails generate controller my index
```

Gerar Moldel e os campos

```ruby
rails generate model person name:string age:integer 
```

Migrate
```ruby
rake db:migrate
#versão 5.0
rails db:migrate

# Vai executar o procedimento de /db/migrate/

class CreatePeople < ActiveRecord::Migration[5.1]
  def change
    create_table :people do |t|
      t.string :name
      t.integer :age

      t.timestamps
    end
  end
end

```

DB condole
```ruby
rails console
sqlite> (comendos sql)
```

```ruby
irb(main):001:0> Person.first
  Person Load (0.0ms)  SELECT  "people".* FROM "people" ORDER BY "people"."id" ASC LIMIT ?  [["LIMIT", 1]]
=> nil
```

Adicionando um registro

```ruby
irb(main):002:0> Person.create :name => "Jose MAlcher", :age =>32
   (0.0ms)  begin transaction
  SQL (2.5ms)  INSERT INTO "people" ("name", "age", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["name", "Jose MAlcher"], ["age", 32], ["created_
at", "2017-05-19 20:40:10.940235"], ["updated_at", "2017-05-19 20:40:10.940235"]]
   (11.0ms)  commit transaction
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):003:0> Person.first
  Person Load (0.0ms)  SELECT  "people".* FROM "people" ORDER BY "people"."id" ASC LIMIT ?  [["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):004:0>

```

```ruby
rb(main):008:0> Person.find(1)
  Person Load (1.0ms)  SELECT  "people".* FROM "people" WHERE "people"."id" = ? LIMIT ?  [["id", 1], ["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):009:0>

```

Para sair: "exit"

Para desfazer ou apagar um controller

```ruby
> rails destroy controller my
 remove  app/controllers/my_controller.rb
      invoke  erb
      remove    app/views/my
      invoke  test_unit
      remove    test/controllers/my_controller_test.rb
      invoke  helper
      remove    app/helpers/my_helper.rb
      invoke    test_unit
      invoke  assets
      invoke    coffee
      remove      app/assets/javascripts/my.coffee
      invoke    scss
      remove      app/assets/stylesheets/my.scss

#ou o model
>rails destroy model person
 invoke  active_record
      remove    db/migrate/20170519203503_create_people.rb
      remove    app/models/person.rb
      invoke    test_unit
      remove      test/models/person_test.rb
      remove      test/fixtures/people.yml


```



[Voltar ao Índice](#indice)

---

## <a name="parte8">ActiveRecord</a>

É um framework que implementa o acesso ao banco de dados de forma transparente ao usuário, funcionando como um Wrapper para seu modelo. Utilizando o conceito de Conventions over Configuration, o ActiveRecord adiciona aos seus modelos as funções necessárias para acessar o banco.

ActiveRecord::Base é a classe que você deve estender para associar seu modelo com a tabela no Banco de Dados.

[Active Record](https://www.caelum.com.br/apostila-ruby-on-rails/active-record/#7-1-motivacao)



[Voltar ao Índice](#indice)

---

## <a name="parte9">Trabalhando com models</a>

Com a model criada.

```ruby
# Gerando o model:
rails generate model person name:string age:integer

# > rails db:migrate

# > rails console
# ----------------
Person.first
 Person Load (0.5ms)  SELECT  "people".* FROM "people" ORDER BY "people"."id" ASC LIMIT ?  [["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
# ----------------
Person.find(1)
  Person Load (0.5ms)  SELECT  "people".* FROM "people" WHERE "people"."id" = ? LIMIT ?  [["id", 1], ["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
# ----------------
Person.take
  Person Load (0.0ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):004:0> Person.take(2)
  Person Load (1.0ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 2]]
=> [#<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">]
# ----------------
Person.create(:name =>"Maria joaquina", :age => 22)
   (0.0ms)  begin transaction
  SQL (2.0ms)  INSERT INTO "people" ("name", "age", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["name", "Maria joaquina"], ["age", 22], ["create
d_at", "2017-05-21 15:57:16.372722"], ["updated_at", "2017-05-21 15:57:16.372722"]]
   (9.7ms)  commit transaction
=> #<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">
irb(main):006:0> Person.take(2)
  Person Load (0.5ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 2]]
=> [#<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">, #<Person id: 2, name: "Maria
joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]
# ----------------
Person.last
  Person Load (0.0ms)  SELECT  "people".* FROM "people" ORDER BY "people"."id" DESC LIMIT ?  [["LIMIT", 1]]
=> #<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">

# ----------------
Person.order(:name)
  Person Load (0.5ms)  SELECT  "people".* FROM "people" ORDER BY "people"."name" ASC LIMIT ?  [["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">, #<Pe
rson id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]>

# ----------------
Person.order(name: :desc)
  Person Load (0.5ms)  SELECT  "people".* FROM "people" ORDER BY "people"."name" DESC LIMIT ?  [["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">, #<
Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">]>

# ----------------
Person.order(name: :asc)
  Person Load (0.5ms)  SELECT  "people".* FROM "people" ORDER BY "people"."name" ASC LIMIT ?  [["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">, #<Pe
rson id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]>

# ----------------
Person.select("name")
  Person Load (0.5ms)  SELECT  "people"."name" FROM "people" LIMIT ?  [["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: nil, name: "Jose MAlcher">, #<Person id: nil, name: "Maria joaquina">]>

# ----------------
Person.find_by name: "Jose MAlcher"
  Person Load (0.5ms)  SELECT  "people".* FROM "people" WHERE "people"."name" = ? LIMIT ?  [["name", "Jose MAlcher"], ["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">

# ----------------
erson.where(name: "Maria joaquina")
  Person Load (1.0ms)  SELECT  "people".* FROM "people" WHERE "people"."name" = ? LIMIT ?  [["name", "Maria joaquina"], ["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]>

# ----------------
Person.where(name: "Maria joaquina").take
  Person Load (1.0ms)  SELECT  "people".* FROM "people" WHERE "people"."name" = ? LIMIT ?  [["name", "Maria joaquina"], ["LIMIT", 1]]
=> #<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">

# ----------------
Person.limit(2)
  Person Load (0.0ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 2]]
=> #<ActiveRecord::Relation [#<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">, #<Pe
rson id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]>
# ----------------
person = Person.first
  Person Load (1.0ms)  SELECT  "people".* FROM "people" ORDER BY "people"."id" ASC LIMIT ?  [["LIMIT", 1]]
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):020:0> person.destroy
   (0.0ms)  begin transaction
  SQL (1.0ms)  DELETE FROM "people" WHERE "people"."id" = ?  [["id", 1]]
   (11.0ms)  commit transaction
=> #<Person id: 1, name: "Jose MAlcher", age: 32, created_at: "2017-05-19 20:40:10", updated_at: "2017-05-19 20:40:10">
irb(main):021:0> Person.take(5)
  Person Load (0.0ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 5]]
=> [#<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]

# ----------------
Person.all
  Person Load (0.5ms)  SELECT  "people".* FROM "people" LIMIT ?  [["LIMIT", 11]]
=> #<ActiveRecord::Relation [#<Person id: 2, name: "Maria joaquina", age: 22, created_at: "2017-05-21 15:57:16", updated_at: "2017-05-21 15:57:16">]>


```

[7.9 - Manipulando nossos modelos pelo console](https://www.caelum.com.br/apostila-ruby-on-rails/active-record/#7-9-manipulando-nossos-modelos-pelo-console)

[Voltar ao Índice](#indice)

---

## <a name="parte10">Migrations</a>

Migrations ajudam a gerenciar a evolução de um esquema utilizado por diversos bancos de dados. Foi a solução encontrada para o problema de como adicionar uma coluna no banco de dados local e propagar essa mudança para os demais desenvolvedores de um projeto e para o servidor de produção.

Com as migrations, podemos descrever essas transformações em classes que podem ser controladas por sistemas de controle de versão (por exemplo, git) e executá-las em diversos bancos de dados.

Sempre que executarmos a tarefa Generator -> model, o Rails se encarrega de criar uma migration inicial, localizado em db/migrate.

ActiveRecord::Migration é a classe que você deve estender ao criar uma migration.

Quando geramos nosso modelo na seção anterior, Rails gerou para nós uma migration (db/migrate/<timestamp>_create_restaurantes.rb). Vamos agora editar nossa migration com as informações que queremos no banco de dados.

```ruby
class CreatePeople < ActiveRecord::Migration[5.1]
  def change
    create_table :people do |t|
      t.string :name
      t.integer :age

      t.timestamps
    end
  end
end

```
Criando uma novo model
```ruby
rails generate model client
      invoke  active_record
      create    db/migrate/20170521171443_create_clients.rb
      create    app/models/client.rb
      invoke    test_unit
      create      test/models/client_test.rb
      create      test/fixtures/clients.yml

```

```ruby
class CreateClients < ActiveRecord::Migration[5.1]
  def change
    create_table :clients do |t|

      t.timestamps
    end
  end
end
```
Criando migration

```ruby
rails generate migration test
      invoke  active_record
      create    db/migrate/20170521171649_test.rb
# ----------------
class Test < ActiveRecord::Migration[5.1]
  def change
  end
end
```
Adicionando
```ruby
class Test < ActiveRecord::Migration[5.1]
  def change
    add_column :test, :name, :string
    add_index :test, :name
    remove_column :test, :name, :string
  end
end
```

[7.7 - Migrations](https://www.caelum.com.br/apostila-ruby-on-rails/active-record/#7-7-migrations)


[Voltar ao Índice](#indice)

---

## <a name="parte11">Trabalhando com controllers</a>

O "V" de MVC representa a parte de view (visualização) da nossa aplicação, sendo ela quem tem contato com o usuário, recebe as entradas e mostra qualquer tipo de saída.

Há diversas maneiras de controlar as views, sendo a mais comum delas feita através dos arquivos HTML.ERB, ou eRuby (Embedded Ruby), páginas HTML que podem receber trechos de código em Ruby.

Controllers são classes que recebem uma ação de uma View e executam algum tipo de lógica ligada a um ou mais modelos. Em Rails esses controllers estendem a classe ApplicationController.

As urls do servidor são mapeadas da seguinte maneira: /controller/action/id. Onde "controller" representa uma classe controladora e "action" representa um método do mesmo. "id" é um parâmetro qualquer (opcional).

[Controllers e Views](https://www.caelum.com.br/apostila-ruby-on-rails/controllers-e-views/)

Criando novo

```
> rails generate controller person
      create  app/controllers/person_controller.rb
      invoke  erb
      create    app/views/person
      invoke  test_unit
      create    test/controllers/person_controller_test.rb
      invoke  helper
      create    app/helpers/person_helper.rb
      invoke    test_unit
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/person.coffee
      invoke    scss
      create      app/assets/stylesheets/person.scss
# GERANDO O MODEL
> rails generate model person name:
  string, age:integer
        invoke  active_record
        create    db/migrate/20170522234432_create_people.rb
        create    app/models/person.rb
        invoke    test_unit
        create      test/models/person_test.rb
        create      test/fixtures/people.yml

```
```ruby
class CreatePeople < ActiveRecord::Migration[5.1]
  def change
    create_table :people do |t|
      t.string, :name
      t.integer :age

      t.timestamps
    end
  end
end
```

Adicionando funções

```ruby
class PersonController < ApplicationController
  def index
    @people = Person.all
    respond_to do |f|
      f.html
    end

    def show
      @person = Person.find(params[:id])

      respond_to do |f|
        f.html
      end
    end
  end

  def new
    @person = Person.new

    respond_to do |f|
      f.html
    end
  end

  def create
    @person = Person.create(person_params)
    respond_to do |f|
      f.html{redirect_to action: 'index'}
    end
  end

  def destroy
    @person = Person.find(params[:id])
    @person.destroy

    respond_to do |f|
      f.html {redirect_to action: 'index'}
    end

  end

  private def person_params
            params.require(:person).permit(:person)
  end

end

```



[Voltar ao Índice](#indice)

---

## <a name="parte12">Um pouco sobre rotas</a>

Ajuste para objeter retorno (json):
```ruby
  # GET /person
  def index
    @people = Person.all
    respond_to do |f|
      f.html
      f.json{render :json => @people}
    end
  end
```

```ruby
Rails.application.routes.draw do

  # get 'hello/index'
  root :to => 'hello#index'

  get '/person' => 'person#index'

# Outra forma
  resources :person
  resources :hello

end


```

As operações disponíveis para cada um dos recursos são:

- GET: retorna uma representação do recurso
- POST: criação de um novo recurso
- PUT: altera o recurso
- DELETE: remove o recurso

Os quatro verbos do protocolo HTTP são comumente associados às operações de CRUD em sistemas Restful. Há uma grande discussão dos motivos pelos quais usamos POST para criação (INSERT) e PUT para alteração (UPDATE). A razão principal é que o protocolo HTTP especifica que a operação PUT deve ser idempotente, já POST não.


[Rotas](https://www.caelum.com.br/apostila-ruby-on-rails/rotas/)

[Voltar ao Índice](#indice)

---

## <a name="parte13">Trabalhando com Views</a>

Material da aula:

index.html.erb
```html
<h1>Listing People</h1>

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <thbody>
    <% @people.each do |p| %>
      <tr>
        <td> <%= p.name %> </td>
        <td> <%= p.age %> </td>
      </tr>
    <% end %>
  </thbody>
</table>
```

new.html.erb
```html
<h1>New Person</h1>

  <%= render 'form' %>

```
+_form.html.erb
````ruby
<%= form_for @person, :url => {:action => "create"} do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>

  <%= f.label :age %>
  <%= f.text_field :age %>

  <br>

  <%= f.submit %>

<br>
    <%= link_to("Back to list", :controller => "person", :action => "index") %>


<% end %>

````

person_controller.rb
```ruby
class PersonController < ApplicationController

  # GET /person
  def index
    @people = Person.all
    respond_to do |f|
      f.html
      f.json{render :json => @people}
    end
  end


  # GET /person/1
  def show
    @person = Person.find(params[:id])

    respond_to do |f|
      f.html
    end
  end


  # GET /person/new
  def new
    @person = Person.new

    respond_to do |f|
      f.html
    end
  end

  # POST /person
  def create
    @person = Person.create(person_params)
    respond_to do |f|
      f.html {redirect_to action: 'index'}
    end
  end

  # DELETE /person/1
  def destroy
    @person = Person.find(params[:id])
    @person.destroy

    respond_to do |f|
      f.html {redirect_to action: 'index'}
    end

  end

  private def person_params
    params.require(:person).permit(:name, :age)
  end

end

```

routes.rb
```ruby
Rails.application.routes.draw do

  # get 'hello/index'
  root :to => 'hello#index'

  get '/person' => 'person#index'
  get '/person/new' => 'person#new'
  post 'person' => 'person#create'


  # Outra forma
  # resources :person
  # resources :hello

end

```
Material extra aula:

ERB

ERB é uma implementação de eRuby que já acompanha a linguagem Ruby. Seu funcionamento é similar ao dos arquivos JSP/ASP: arquivos html com injeções de código. A ideia é que o HTML serve como um template, e outros elementos são dinamicamente inseridos em tempo de renderização.

sintaxe básica

Para uma página aceitar código Ruby, ela deve estar entre "<%" e "%>". Há uma variação deste operador, o "<%=", que não só executa códigos Ruby, mas também imprime o resultado na página HTML.
Logo, o seguinte código ERB:
```html
<html>
  <body>
    <p>Meu nome é: <%= "João" %></p>
    <p>Não vai imprimir nada ao lado: <% "Não será impresso" %></p>
  </body>
</html>
```

Irá resultar em:
```html
<html>
  <body>
    <p>Meu nome é: João</p>
    <p>Não vai imprimir nada ao lado: </p>
  </body>
</html>
```
if, else e blocos

O operador "<%" é muito útil quando precisamos que um pedaço de HTML seja adicionado com uma condição. Por exemplo:
```html
<body>
  <% if nomes.empty? %>
    <div class="popup">
      Nenhum nome
    </div>
  <% else %>
    <div class="listagem">
      <%= nomes %>
    </div>
  <% end %>
</body>
```

Caso a variável nomes seja igual à [], o resultado será:

```html
<body>
    <div class="popup">
      Nenhum nome
    </div>
</body>
```

Por outro lado, se nomes for igual à ["João", "Maria"] o resultado será:

```html
<body>
    <div class="listagem">
      ["João", "Maria"]
    </div>
</body>
```

Podemos ainda iterar pelos nomes imprimindo-os em uma lista, basta mudar o ERB para:

```html
<body>
  <% if nomes.empty? %>
    <div class="popup">
      Nenhum nome
    </div>
  <% else %>
    <ul class="listagem">
      <% nomes.each do |nome| %>
        <li><%= nome %></li>
      <% end %>
    </ul>
  <% end %>
</body>
```

Para nomes igual à ["João", "Maria"] o resultado seria:

```html
<body>
    <ul class="listagem">
        <li><%= João %></li>
        <li><%= Maria %></li>
    </ul>
</body>
```

Do controller para view

É importante notar que todos os atributos de instância (@variavel) de um controlador estão disponíveis em sua view. Além disso, ela deve ter o mesmo nome da action, e estar na pasta com o nome do controlador o que significa que a view da nossa action index do controlador restaurantes_controller.rb deve estar em: app/views/restaurantes/index.html.erb.

[9.4 - Trabalhando com a View: O ERB](https://www.caelum.com.br/apostila-ruby-on-rails/controllers-e-views/#9-4-trabalhando-com-a-view-o-erb)

[Voltar ao Índice](#indice)

---

## <a name="parte14">Validando model</a>

models/person.rb
```ruby
class Person < ApplicationRecord
  validates :name, presence: true, format: {with: /\A[a-zA-Z]+\z/, message: "Accept only letters"}
end

```
Logs
```
Started POST "/person" for 127.0.0.1 at 2017-05-23 05:09:54 -0300
Processing by PersonController#create as HTML
  Parameters: {"utf8"=>"✓", "authenticity_token"=>"KRyJxObZ0U9nmS1kywhmWV8WCLyhyrDXegdqWUgGTaYTtxvvNr/xfb
hiwuHCSCoOmxDY62XDDPLY7IjfLlFE1Q==", "person"=>{"name"=>"jose2", "age"=>""}, "commit"=>"Create Person"}
   (1.0ms)  begin transaction
   (1.0ms)  rollback transaction
Redirected to http://localhost:3000/person
Completed 302 Found in 40ms (ActiveRecord: 2.0ms)

```

7.14 - Validações
Ao inserir um registro no banco de dados é bem comum a entrada de dados inválidos.

Existem alguns campos de preenchimento obrigatório, outros que só aceitem números, que não podem conter dados já existentes, tamanho máximo e mínimo etc.

Para ter certeza que um campo foi preenchido antes de salvar no banco de dados, é necessário pensar em três coisas: "como validar a entrada?", "qual o campo a ser validado?" e "o que acontece ao tentar salvar uma entrada inválida?".

Para validar esses registros, podemos implementar o método validate em qualquer ActiveRecord, porém o Rails disponibiliza alguns comandos prontos para as validações mais comuns. São eles:

- validates_presence_of: verifica se um campo está preenchido;
- validates_size_of: verifica o comprimento do texto do campo;
- validates_uniqueness_of: verifica se não existe outro registro no banco de dados que tenha a mesma informação num determinado campo;
- validates_numericality_of: verifica se o preenchimento do campo é numérico;
- validates_associated: verifica se o relacionamento foi feito corretamente;
- etc...

Todos estes métodos disponibilizam uma opção (:message) para personalizar a mensagem de erro que será exibida caso a regra não seja cumprida. Caso essa opção não seja utilizada, será exibida uma mensagem padrão.

[7.14 - Validações](https://www.caelum.com.br/apostila-ruby-on-rails/active-record/#7-14-validacoes)


[Voltar ao Índice](#indice)

---

## <a name="parte15">Scaffold</a>

[10.1 - Um pouco mais sobre o Scaffold](https://www.caelum.com.br/apostila-ruby-on-rails/completando-o-sistema/#10-1-um-pouco-mais-sobre-o-scaffold)

Vimos que quando usamos o gerador scaffold o Rails cria os arquivos necessários em todas as camadas. Controller, Model, Views e até mesmo arquivos de testes e a Migration. Para concluir nossos projeto precisamos criar apenas Controller + Views pois tanto o modelo quanto as migrations já estão prontos. Para isso vamos usar o mesmo gerador scaffold mas vamos passar os parâmetros: --migration=false para ele ignorar a criação da migration e o parâmetro -s que é a abreviação para --skip que faz com que o rails "pule" os arquivos já existentes.

```ruby
> rails generate scaffold book title
:string isbn:string page:integer
      invoke  active_record
      create    db/migrate/20170523081642_create_books.rb
      create    app/models/book.rb
      invoke    test_unit
      create      test/models/book_test.rb
      create      test/fixtures/books.yml
      invoke  resource_route
       route    resources :books
      invoke  scaffold_controller
      create    app/controllers/books_controller.rb
      invoke    erb
      create      app/views/books
      create      app/views/books/index.html.erb
      create      app/views/books/edit.html.erb
      create      app/views/books/show.html.erb
      create      app/views/books/new.html.erb
      create      app/views/books/_form.html.erb
      invoke    test_unit
      create      test/controllers/books_controller_test.rb
      invoke    helper
      create      app/helpers/books_helper.rb
      invoke      test_unit
      invoke    jbuilder
      create      app/views/books/index.json.jbuilder
      create      app/views/books/show.json.jbuilder
      create      app/views/books/_book.json.jbuilder
      invoke  test_unit
      create    test/system/books_test.rb
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/books.coffee
      invoke    scss
      create      app/assets/stylesheets/books.scss
      invoke  scss
      create    app/assets/stylesheets/scaffolds.scss

```
Migrate
```
rails db:migrate
```

[Voltar ao Índice](#indice)

---

## <a name="parte16">Finalizando</a>

Melhor Referencia: 

[Desenv. Ágil para Web com Ruby on Rails](https://www.caelum.com.br/apostila-ruby-on-rails/)

[Voltar ao Índice](#indice)

---

