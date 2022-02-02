# Crear sitio web/blog con Gatsby y Netlify

Instalar Gatsby

- **`npm install -g gatsby-cli`**

Gatsby es un framework, que funciona con react, y se alimenta de una API de contenido, bien sea API, Markdown, JSON, etc. Y todo lo trabaja usando GraphQL.

El repositorio vamos a tener en Github, y éste repositorio lo enlazamos con Netlify. Netlify nos va a proveer un sistema de autenticación, por la cual distintas personas podrán crear contenido en nuestro sitio web. De esta forma, este contenido se enviará al repositorio de Github, y éste se enviará al deploy de Netlify.

## Iniciamos el asistente de Gatsby. 

- `gatsby new gatsby-blog`

De esta forma podremos iniciar el asistente de Gatsby, y crear un nuevo proyecto con el nombre gatsby-blog.


## Plantillas de Gatsby

Otra forma que podemos usar es crear una plantilla de Gatsby, y luego crear un proyecto con esa plantilla. Para ello podremos buscarlas en la página de Gatsby. [Gatsby Starters](https://www.gatsbyjs.com/starters/) que nos llevará a la página de plantillas de Gatsby.

La plantilla que vamos a usar es el **`gatsby-starter-blog`**.

[Gatsby Starter Blog](https://www.gatsbyjs.com/starters/gatsbyjs/gatsby-starter-blog/)

- **`npx gatsby new website-gatsby https://github.com/gatsbyjs/gatsby-starter-blog`**

- **`npx gatsby develop`**


## Configuración de Gatsby

Los archivos de configuración de Gatsby son **`gatsby-config.js`** y **`gatsby-node.js`**.

Los archivos para generar paginas se encuentran en la carpeta **`src/pages`**.
A partir de ellas podemos generar páginas con Gatsby, y el automáticamente nos crea la ruta con el nombre de la página.

Para la creación de Post, podremos hacerlo en la carpeta **`src/posts`**, allí podremos crear el contenido de los posts en un archivo markdown, dentro de una capeta con el nombre del post.

La otra forma que podremos hacerlo es usando un CMS, en este caso netlify nos provee de Netlify CMS para crear contenido.

- [Netlify CMS](https://www.netlifycms.org/docs/start-with-a-template/)

Desde allí lo añadiremos a un sitio existente. [Add to your site](https://www.netlifycms.org/docs/add-to-your-site/)


## Configuración de Netlify

