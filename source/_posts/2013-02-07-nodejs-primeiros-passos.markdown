---
layout: post
title: "Nodejs - Primeiros passos"
date: 2013-02-07 11:30
comments: true
categories: 
---
<p>
	O Nodejs foi uma das coisas mais bacanas a respeito de desenvolvimento para Web que conheci ultimamente. Trata-se de uma plataforma que permite desenvolver aplicações do lado do servidor usando apenas Javascript. O Nodejs foi construido com a engine de javascript do Google, V8, sendo este o que permite a escrita de Javascript para server-side. Fico devendo um outro post falando melhor sobre o v8, mas por enquanto vamos ao que interessa.
</p>
<h3>Instalando o Nodejs</h3>
<p>
	Para instalar o nodejs em um ambiente linux baixe o <a href="http://nodejs.org/dist/v0.8.19/node-v0.8.19.tar.gz">arquivo compactado(.tar.gz)</a>, extraia os arquivos e faça os seguintes passos:
</p>
<pre><code>
	cd /<i>your_directory</i>/node-x.x.x
	sudo ./configure --prefix=/usr/local/node
	sudo make 
	sudo make install
</code></pre>

<p>Ao concluir os comandos acima, o nodejs já está devidamente instalado com os outros demais recursos que eles oferecem, dentre os principais o npm(Node Package Manager), o qual será definido melhor nos próximos posts.</p>

<h3>Hello World no Nodejs</h3>
<p>
	Para ter um primeiro contato, com o nodejs podemos utilizar o seu console. Um pequeno ambiente que pode rodar no terminal de shell do seu SO e que podemos testar alguns comandos básicos do nodejs. Abra seu terminal e faça os passos abaixo.
</p>
<pre><code>
	node
	> console.log("Hello World")
	Hello World
	undefined
</code></pre>
<p>
	Nos próximos posts falaremos como começar a criar uma aplicação server-side utilizando o nodejs. Até lá...
</p>