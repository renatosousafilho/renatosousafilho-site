---
layout: post
title: "Nodejs - Criando um servidor HTTP "
date: 2013-02-07 11:32
comments: true
categories: 
---

<p>O passo inicial para criar uma aplicação com nodejs é utilizando o módulo de http. Este módulo possui funcões para que possamos lidar com requisições em uma determinada porta do servidor, para isso vamos conhecer o básico de sua API.
Para fazer uso do módulo de HTTP, precisamos antes carregarmos em um objeto, através do uso do método require. Como vemos abaixo:
<pre><code>var http = require('http');	
</code></pre>

<p>Agora é onde começa nossa implementação. Por padrão o http requer uma funcão que receba como parametros dois obejtos: <strong>request</strong> e <strong>response</strong>, dessa forma temos que escrever algo deste tipo:</p>
<pre><code>function handleRequest(request,response){
	response.writeHead(200);
	response.write("Hello World");
	response.end();
}
</code></pre>

<p>Note que utilizamos o objeto response para definir as características da resposta do nosso servidor às requisções. Na primeira linha, é definido o Header do pacote de reposta, com o status 200, o que significa que a requisição está ok(podemos taḿbém usar os status como 501 para erro interno do servidor, ou 404 para uma requisição com falha). Em seguida, escrevemos o corpo da resposta com o método write e por fim, finalizamos a resposta do cliente. Esta função será usada como um <i>callback</i> para o método <i>createServer</i> do objeto http que nos retornará o nosso servidor web.</p>
<pre><code>var server = http.createServer(handleRequest);</code></pre>

<p>Por fim devemos fazer com que este nosso servidor criado seja associado a uma porta da nossa máquina, utilizando o método <i>listen()</i> do objeto referente ao servidor que foi criado.</p>
<pre><code>server.listen(8080);</code></pre>

<p><i>Observação: certifique-se de que a porta utilizada no parâmetro já não está sendo utilizada por outro serviço da sua máquina como um servidor apache ou algum outro tipo de Serviço</i> </p>

<p>Pronto, desta forma temos nosso arquivo server.js, como segue abaixo:</p>
<pre><code>var http = require('http');
function handleRequest(request,response){
	response.writeHead(200);
	response.write("Hello World");
	response.end();
}
var server = http.createServer(handleRequest);	
server.listen(8080);
</code></pre>

<p>Para executarmos nosso servidor, basta usar o comando:</p>
<pre><code>node server.js</code></pre>
	
<p>E acessar a url http://localhost:8080 e lá estará nosso primeiro exemplo de servidor.
</p>
 
<p>Como o javascript possui uma síntaxe bem felixível podemos simplificar o código acima para esta forma.</p>
<pre>
var http = require('http');
http.createServer(function(request,response){
	response.writeHead(200);
	response.write("Hello World");
	response.end();
}).listen(8080);
</pre>

<p>O módulo de HTTP do Nodejs possui uma extensa API que abrange várias funcionalidades do famoso protocolo de transferência de hipertexto, para mais informações confira a documentaçaõ oficial. (<a href="http://nodejs.org/api/http.html">http://nodejs.org/api/http.html</a>)</p>