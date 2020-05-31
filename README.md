# Theme Dipujaen Sass

Proyecto que desarrolla un tema css para los componentes de Prime, que usaremos en Angular.

## Tecnologia

Se ha utilizado SASS, aparte de las muchisimas ventajas, nos permite tener modulado y organizado nuestro c�digo.
El echo de tener una buena estructuraci�n en nuestros estilos nos har� la vida m�s f�cil a la hora de realizar futuras modificaciones.

## Estructura

No existe un est�ndar de organizaci�n del proyecto, he optado por organizarlo de la siguiente forma : 

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

La carpeta base contiene las tipograf�as de proyecto, reset y normalizaciones de elementos HTML para eliminar inconsistencias.
La carpeta layout contendr� la distribuci�n de tu aplicaci�n, incluso partes de la web en si misma.
En components guardaremos porciones del proyecto. Ser�a como si trataramos con widgets.
En la carpeta pages incluiremos estilos para cada p�gina y de esta manera poder localizarlos m�s r�pidamente (home.scss, contact.scss, etc �)
En themes en el caso que necesitaramos crear un theme para una parte de nuestro proyecto (extranet, admin, etc �)
abstracts es una carpeta muy importante y en la que incluyo helpers, mixins, funciones, variables y otras herramientas.
En vendor incluiremos archivos de librer�as externas y que necesitar� nuestro proyecto para poder funcionar (La grillas o reboot de bootstrap podr�an ser un ejemplo).

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

