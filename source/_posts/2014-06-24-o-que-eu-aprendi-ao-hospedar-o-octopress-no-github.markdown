---
layout: post
title: "O que eu aprendi ao hospedar o octopress no GitHub"
date: 2014-06-24 06:05:05 -0300
comments: true
categories: [Rails, Blog, Octopress, Github]
---
Eu tive algumas dificuldades de hospedar o meu blog no Github. Estava obtendo o seguinte erro:

'## Pushing generated _deploy website
To git@github.com:valdyrtorres/valdyrtorres.github.io.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:valdyrtorres/valdyrtorres.github.io.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Merge the remote changes (e.g. 'git pull')
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Após exaustivas buscas na Internet, no google, mesmo em meu site favorito que é o stackoverflow não
conseguia resolver. Ressalto que li atentamente a documentação do Git a respeito do non-fast-forward e bla-bla.

Finalmente encontrei a solução no seguinte site:

http://allenyee.me/blog/2013/08/21/what-i-learned-from-hosting-octopress-on-github/

Obrigado Allen!

Abaixo segue a transcrição da solução:

Vá para o diretório _deploy

cd octopress/_deploy

Como o branch master está nesse diretório (_deploy), execute:

   $ git pull origin master

Com ele você resolve os possíveis conflitos. Retorne para o diretório octopress:

   $ cd ..

Faça o deploy:

   $ rake deploy

Agora tudo funcionou.
