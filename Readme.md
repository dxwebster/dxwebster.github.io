<p align="center">
  <img src="./readme/Twitter.png"  width="550"/>
  <br><br>
  <div align="center">
  Layout do Twitter feito utilizando Flexbox e Sass
  
  💻 **Acesse o Preview [aqui](https://dxwebster.github.io/Twitter-Flexbox)** 
  </div>
</p>

## 📥 Executar esse projeto no seu computador

- Clonar Repositório: `git clone https://github.com/dxwebster/Twitter-Flexbox`
- Entrar na pasta: `cd Twitter-Flexbox`
- Instalar dependências: `yarn install`

## 🚀 Tecnologias utilizadas

- HTML3
- CSS5 (Flexbox)
- Sass
- NodeJS
- Live Server

# Live Server

Para escrever nossos códigos e ter um live reload, utilizaremos a extensão Live Server para VSCode.
Mais informações do Plugin: https://github.com/ritwickdey/live-server-web-extension

# Sass

Vamos rodar o sass para compilar nossos arquivos pelo Node. Nosso arquivo 'package.json' contém um script que vai fazer o sass observar as alterações dos arquivos e compilar automaticammente nosso .scss em .css. Para rodar o sass, basta executar `yarn start`

```json
// package.json
{
  "devDependencies": {
    "sass": "^1.26.10"
  },
  "scripts": {
    "start": "yarn sass --watch scss/style.scss css/style.css"
  }
}
```

# CSS Tips

## CSS Units

Unidades de medidas do CSS

Layout Fixo
`px` - Pixels

Layout Fluido
`%` - Porcentagem
`auto` - Automática
`vh` - Viewport Height
`vw` - Viewport Width

Textos fixos
`1px` = 0.75pt
`16px` = 12pt

Texto fluidos
`em` - multiplicado pelo pai 
`rem` - multiplicado pelo root

## CSS Media Queries 

No HTMl eu coloco a seguinte tag meta

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

No CSS eu uso da seguinte forma

```css
@media (max-width: 320px) {
  #form h3 {
    font-size: 2rem;
  }
}
```

### HTML Media Attrib.

Posso utilizar o atribuito `media` no link do meu HTML, ao importar um arquivo css, usando as propriedades da mesma forma que usaria na regra `@media` do css.

```html
<link 
    rel="stylesheet"
    href="responsive.css" 
    media="screen and (max-width: 768px)"
/>

<link rel="stylesheet" href="print.css" media="print">
```

### Imagens

Usamos a tag `<picture>` para que as imagens sejam responsivas.

```html
<picture class="image" alt="Imagem">
    <source media="(min-width: 768px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/maxresdefault.jpg">
    <source media="(min-width: 320px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/hqdefault.jpg">
    <source media="(min-width: 10px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/mqdefault.jpg">

    <img 
        src="https://i.ytimg.com/vi/GykTLqODQuU/hqdefault.jpg" 
        alt="Imagem" />
</picture>
```

Sempre que possível, usar SVG ao invés de JPG, PNG

## 📕 Licença

Todos os arquivos incluídos aqui, incluindo este _README_, estão sob [Licença MIT](./LICENSE).<br>
Criado com ❤ por [Adriana Lima](https://github.com/dxwebster)
