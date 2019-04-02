## Tutorial de instalação das ferramentas para o backend de PS1

### Instalar Node

Estou utilizando a versão 11

Para SO baseado em debian instalador [aqui](https://github.com/nodesource/distributions)

outras versões de SO [aqui](https://nodejs.org/en/download/package-manager)
ps: Caso for usar em Windows, recomendo fortemente o chocolatey, já usei e funciona bem

depois de instalar verificar a versão:
`node -v`
saída será algo como `v11.12.0`

### instalar Yarn

para Linux instruções no site oficial [aqui](https://yarnpkg.com/pt-BR/docs/install#debian-stable)

Para Windows instruções com o chocolatey [aqui](https://chocolatey.org/packages/yarn)

o meu está na versão 1.13
`yarn -v 1.13.0`

### instalar o git

instruções melhores no site oficial [linux](https://git-scm.com/download/linux) [windows](https://git-scm.com/download/win)

### instalar VsCode

Como editor de texto, eu sugiro usarmos o Visual Studio Code, além de simples e leve, poderemos configurar o eslint e prettier, juntos esses dois trabalham com a sintaxe do código e algumas outras configurações, como por exemplo: definir o charset padrão (windows usa um diferente se não me engano), tipo de endline, padrão de tabs, aspas simples ou duplas. etc.. Quando salvamos o código, os plugins fazem toda as alterações para deixar no padrão, assim a gente evita problemas com compatibilidade windows x linux e o código fica padronizado. O prettier também diz quando estámos usando uma sintaxe errada facilitando encontrar alguns erros.

enfim caso tenha interesse link [aqui](https://code.visualstudio.com/)

#### Básico sobre ES6

Para melhor acompanhamento e uso do adonisjs sugiro que vocês se inscrevam no curso de ES6 da rocketseat [aqui](https://rocketseat.com.br/starter) é grátis.

## Client Rest

Para podermos testar as rotas da aplicação, precisaremos enviar requisições para nossa API, com o navegador isso não é possível, para isso usaremos o [Insomnia](https://insomnia.rest/download/)

## Adonis

Como no nosso projeto utilizaremos o Adonisjs como framework, precisamos instala-lo de forma global para podermos usar os comandos no terminal.

```
npm i -g @adonisjs/cli
```

Obs: Talvez precise permissão.
