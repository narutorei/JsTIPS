title: Entendendo o Resolve do AngularJS
tags:
  - AngularJS
  - Resolve
  - JavaScript
categories:
  - AngularJS
date: 2014-10-28 08:12:00
---
Tive um problema algum tempo com o DataTables e o AngularJS por causa da randerização dos dados da tabela, estudando um pouco cheguei a melhor solução pra trabalhar com dados que você necessariamente precisa deles PRONTOS assim que se inicia a randerização dos dados.
Esse cara é o Resolve! 
###### masoq? ele resolve ? como assim?

É simples! vejamos nosso módulo abaixo :

{% gist 7a496e113d0bcad781e1 exampleListResolve.js %}

#####Loco ein? tendi nada...
Calma que eu explico! No nosso $stateProvider, adicionamos o resolve, que é um objeto que irá te retornar um valor. Toda a mágica acontece nele! O AngularJS não permite que a aplicação termine de rodar e execute o controller, até que o resolve esteja concluído!

A principal diferença é, quando você recupera a promise DENTRO do resolve, o Angular trata ela como síncrona! ( ou seja, ele vai esperar que ela termine para terminar o trabalho dele! )
E como você recupera os dados retornados do Resolve? Você injeta como dependência no controller, como fizemos na linha 17!
Simples né? :D

Gostou do post? Ficou com alguma duvida? Quer dar uma dica? Comente! :)