# Treinamento Front-end Semantico

Projeto de treino para praticar HTML semantico, SCSS modular, metodologia BEM e uso do Parcel como bundler.

## Objetivo

Este projeto foi criado para estudar a estrutura de uma pagina web com boas praticas de front-end:

- uso correto de tags semanticas como `header`, `nav`, `main`, `section`, `article`, `aside` e `footer`;
- organizacao de classes seguindo a metodologia BEM;
- separacao dos estilos em arquivos SCSS por responsabilidade;
- responsividade para diferentes tamanhos de tela;
- compilacao automatica de SCSS com Parcel.

## Tecnologias utilizadas

- HTML5
- SCSS
- BEM
- Parcel
- Node.js
- npm

## Como instalar

Instale as dependencias do projeto:

```bash
npm install
```

## Como rodar o projeto

Inicie o servidor de desenvolvimento:

```bash
npm start
```

Tambem e possivel usar:

```bash
npm run dev
```

Depois, acesse no navegador:

```text
http://localhost:1234
```

## Como gerar o build

Para gerar a versao final otimizada:

```bash
npm run build
```

Os arquivos finais serao criados na pasta `dist/`.

## Estrutura do projeto

```text
.
+-- index.html
+-- package.json
+-- package-lock.json
+-- README.md
+-- src
    +-- image
    |   +-- logo.png
    +-- scss
        +-- main.scss
        +-- abstracts
        |   +-- _mixins.scss
        |   +-- _variables.scss
        +-- base
        |   +-- _base.scss
        |   +-- _reset.scss
        +-- components
        |   +-- _button.scss
        |   +-- _content.scss
        |   +-- _hero.scss
        |   +-- _lesson.scss
        |   +-- _sidebar.scss
        +-- layout
            +-- _footer.scss
            +-- _header.scss
            +-- _main.scss
            +-- _navigation.scss
            +-- _responsive.scss
```

## Organizacao do SCSS

O arquivo `src/scss/main.scss` e o ponto de entrada dos estilos. Ele importa os modulos de base, layout, componentes e responsividade.

```scss
@use "./base/reset";
@use "./base/base";

@use "./layout/header";
@use "./layout/navigation";
@use "./layout/main";
@use "./layout/footer";

@use "./components/hero";
@use "./components/button";
@use "./components/content";
@use "./components/lesson";
@use "./components/sidebar";

@use "./layout/responsive";
```

## Scripts disponiveis

| Comando | Funcao |
| --- | --- |
| `npm start` | Inicia o projeto com Parcel |
| `npm run dev` | Inicia o ambiente de desenvolvimento |
| `npm run build` | Gera a versao final do projeto |

## Observacao

Com Parcel, o arquivo SCSS pode ser chamado diretamente no `index.html`:

```html
<link rel="stylesheet" href="./src/scss/main.scss" />
```

O Parcel compila o SCSS para CSS automaticamente durante o desenvolvimento e no build.
