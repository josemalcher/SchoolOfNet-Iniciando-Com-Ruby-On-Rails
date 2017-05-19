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

## <a name="parte5"> </a>

[Voltar ao Índice](#indice)

---

## <a name="parte6"> </a>

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