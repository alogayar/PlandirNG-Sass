# Theme Dipujaen Sass

Proyecto que desarrolla un tema css para los componentes de Prime, que usaremos en Angular.

## Tecnologia

Se ha utilizado SASS, aparte de las muchisimas ventajas, nos permite tener modulado y organizado nuestro código.
El echo de tener una buena estructuración en nuestros estilos nos hará la vida más fácil a la hora de realizar futuras modificaciones.

## Estructura

No existe un estándar de organización del proyecto, he optado por organizarlo de la siguiente forma : 

|- assets/
|    |- css/| 
|        |- dist/ 
|            |- style.min.css
|            |- style.min.css.map
|        |- source/
|            |- abstracts/
|            |     |- media-queries.scss
|            |     |- variables.scss
|            |- base/
|            |     |- _fonts.scss
|            |- components/
|            |     |- _headings.scss
|            |- layout/
|            |     |- _footer.scss
|            |     |- _header.scss
|            |     |- _nav.scss
|            |     |- _content.scss
|            |- pages/
|            |     |- _home.scss
|            |- themes/
|            |- vendor/
|            |     |- bootstrap/
|            |     |- _grid.scss
|            |     |- _greboot.scss
|         |- style.scss
|         |- style.css
|         |- style.css.map
|     |- js/
|     |- img/



## Contenido de cada carpeta

Ahora veamos la finalidad de cada una de las carpetas:

La carpeta base contiene las tipografías de proyecto, reset y normalizaciones de elementos HTML para eliminar inconsistencias.
La carpeta layout contendrá la distribución de tu aplicación, incluso partes de la web en si misma.
En components guardaremos porciones del proyecto. Sería como si trataramos con widgets.
En la carpeta pages incluiremos estilos para cada página y de esta manera poder localizarlos más rápidamente (home.scss, contact.scss, etc …)
En themes en el caso que necesitaramos crear un theme para una parte de nuestro proyecto (extranet, admin, etc …)
abstracts es una carpeta muy importante y en la que incluyo helpers, mixins, funciones, variables y otras herramientas.
En vendor incluiremos archivos de librerías externas y que necesitará nuestro proyecto para poder funcionar (La grillas o reboot de bootstrap podrían ser un ejemplo).

## Fichero principal

@charset 'utf-8';
// Configuration and helpers
@import 'abstracts/variables';
@import 'abstracts/media-queries';
// vendors @import 'vendor/bootstrap/reboot';
@import 'vendor/bootstrap/grid';
// Base stuff
@import 'base/fonts';
// Components
@import 'components/headings';
// layout//
@import 'layout/nav';
@import 'layout/header'; 
@import 'layout/content';
@import 'layout/footer';
// pages
@import 'pages/home';

