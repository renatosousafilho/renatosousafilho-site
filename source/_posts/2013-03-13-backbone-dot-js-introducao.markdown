---
layout: post
title: "Backbone.js - Introdução"
date: 2013-03-13 11:20
comments: true
categories: 
---

Neste post apresentarei um pouco sobre esta biblioteca Javascript que nos permite trazer o padrão MVC para o desenvolvimento com JavaScript. Lógico que não é a única biblioteca com essa proposta e dizer que ele é um dos mais importantes pode acabar sendo discordado para outros desenvolvedores, mas uma coisa é certa, dentre todos as bibliotecas ela é a mais simples e funcional, servindo também para um bom ponto de partida se você quiser estudar outras bibliotecas e frameworks similares como o Meteor, Batman.js, Sencha, entre outras.

Para começar a desenvolver usando o Backbone.js tudo que você precisa saber é um pouco de JSON e Javascript, e de jQuery, porém se você não for tão familiarizado, o estudo de Backbone.js pode matar dois coelhos com uma cajadada só, como foi meu caso. Então vamos conhecer o que podemos fazer com Backbone.js.

MVC ou não é MVC?

Bom, eu acredito que na prática nem tudo se encaixa 100% do que o nome sugere, o Backbone traz na sua utilização alguns conceitos de MVC, por mais que não seja igual ao MVC que estamos habituados, o Modelo, o Controlador e a Visão. Em termos prático, o C representaria o Collection, classe do Backbone que conhecermos melhor mais a frente. Enfim, é mais um detalhe de etimologia que não vai nos influir tanto, mas serve para já nos prepararmos que o desenvolvimento com Backbone.js não é exatamente igual a frameworks MVC como o Rails ou Django porém possua várias similaridades.

Como nem tudo são flores, existe uma peculiaridade do Backbone.js que não chega a ser exatamente um problema, justamente a sua natureza. Ele não é um framework, apenas uma biblioteca, o que quero dizer com isso é que não existe um padrão preestabelecido para organização do seu código. Você pode encontrar uma ou outra especificação, mas originalmente a proposta do Backbone é oferecer uma API para desenvolver o código mais modularizado com o uso. O que quero dizer com isso é que você tem a liberdade de escrever uma aplicação inteira em uma única página ou separar em vários scripts e páginas diferentes. A medida que você ganhar familiaridade com Backbone você pode acabar encontrando uma forma que lhe agrade mais. Mas não existe padrão para o Backbone.

Como eu crio uma aplicação com Backbone.js?

Para começar a criar uma aplicação com Backbone.js(http://backbonejs.org/), você precisa apenas do código da biblioteca  e do Underscore.js(http://underscorejs.org/),  uma dependência do Backbone.js. Tendo estes dois arquivos tudo que você precisa agora é de uma página html para começar sua aplicação.

<html>
<head>
	<title>Backbone Beginner</title>
	<script src="./backbone-min.js" type="text/javascript" charset="utf-8" ></script>
	<script src="./underscore-min.js" type="text/javascript" charset="utf-8" ></script>
</head>
<body>
	Let's learn about Backbone.js
</body>
</html>

A partir daí já podemos começar a escrever nossa aplicação. No nosso próximo post veremos um pouco  sobre modelos. Até lá.