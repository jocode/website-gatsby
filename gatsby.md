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

Vamos a netlify y creamos las carpetas necesarias en el proyecto para que funcione como CMS gestionado por Netlify CMS.

En la carpeta **public** creamos un carpeta llamada **`admin`** con 2 archivos:
- **`index.html`**
- **`config.yml`**

En el archivo `index.html` colocamos el contenido para iniciar sesión en Netlify. Y en el archivo `config.yml` colocamos la configuración de nuestro sitio web, para indicarle que carpetas se deben gestionar, para guardar los post y para guardar las imágenes, crear categorías, etc.


### Habilitar el inicio de sesion en Netlify

Para gestionar el inicio de sesión para colocar las entradas de post, ingresamos a Netlify y primero que todo vinculamos el repositorio de Github con nuestro sitio web. De esta forma ya luego dentro de las configuraciones del sitio **Site Settings** podremos acceder a Netlify CMS.

Para ello, accedemos a **Identity** y damos clic en **Enable Identity**, y luego cambiar las preferencias de registro, para que solo unos usuarios puedan ser editores del blog.

En la parte de servicios, debemos habilitar también **Git Gateway**, para que podamos subir los archivos a nuestro repositorio de Github. Para que el contenido que se publica en NetlifyCMS se envíe a Github y se renderice luego en Netlify.

Y finalmente podremos habilitar proveedores externos para permitir que los usuarios se registren e inicien sesión con proveedores de OAuth externos, como Google.


## Acceder al panel para el CMS

Para al administrador, debemos ingresar a la URL del sitio web y en la url, colocamos **`/admin`**, de esta forma ya podremos acceder al panel de administración.

