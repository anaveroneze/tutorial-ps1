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

Para podermos testar as rotas da aplicação, precisaremos enviar requisições para nossa API, para isso usaremos o [Insomnia](https://insomnia.rest/download/)

## Adonis

Como no nosso projeto utilizaremos o Adonisjs como framework, precisamos instalá-lo de forma global para que tenhamos acesso aos comandos pelo terminal.

```
npm i -g @adonisjs/cli
```

Obs: Talvez precise permissão.

## Configurações do Visual Studio Code

### EditorConfig

Instalaremos primeiro o EditorConfig para isso basta irmos nas extensões do vscode apertando `ctrl + shift + x` e buscar por Editor Config deve ser o primeiro, com a cara de um ratinho.

```
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

### ESLint e Prettier

Mesma coisa, ir nas extensões e buscar por ESLint e por Prettier, instalar e reiniciar o Vscode

**Daqui pra baixo ignora, coloquei toda minha config aqui, mas ter vários cacarecos e algumas coisas só precisam ser feitas uma vez no projeto todo, então deixa pra fazermos juntos**

abrir as configurações do editor com o atalho `ctrl + ,` no canto superior direito vai ter {}, clicar sobre pra abrir as configurações no modo JSON

```
{
  "editor.fontSize": 16,
  "editor.lineHeight": 24,
  "editor.fontFamily": "'Fira code', 'monospace', monospace, 'Droid Sans Fallback'",
  "editor.fontLigatures": true,
  "workbench.iconTheme": "material-icon-theme",
  "editor.formatOnSave": true,
  "editor.rulers": [80, 120],
  "editor.tabSize": 2,
  "editor.renderLineHighlight": "gutter",
  "terminal.integrated.fontSize": 14,
  "emmet.syntaxProfiles": {
    "javascript": "jsx"
  },
  "emmet.includeLanguages": {
    "javascript": "javascripreact"
  },
  "javascript.updateImportsOnFileMove.enabled": "never",
  "breadcrumbs.enabled": true,
  "editor.parameterHints.enabled": false,
  "prettier.eslintIntegration": true,
  "window.zoomLevel": 0,
  "files.associations": {
    "*.html": "html"
  },
  "editor.suggestSelection": "first",
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue"
}
```

Eu uso a font fira code com font ligatures pra ficar mais bonito visualmente, caso tenha interesse mais instruções no [git](https://github.com/tonsky/FiraCode/wiki)

Depois do projeto iniciado
instalar o ESLint no projeto
``npm install -D eslint```
npx eslint --init
selecionar check , find and enforce code style
use a popular style guide
standart
JSON

.eslintRC.json
automaticamente criado

```
{
  "extends: "standard",
  "globals": {
    "use": true
  }
}
```
