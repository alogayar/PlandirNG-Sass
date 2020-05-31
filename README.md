# Theme Dipujaen Sass

Proyecto que desarrolla un tema css para los componentes de Prime, que usaremos en Angular.

## Tecnologia

Se ha utilizado SASS, aparte de las muchisimas ventajas, nos permite tener modulado y organizado nuestro código.
El echo de tener una buena estructuración en nuestros estilos nos hará la vida más fácil a la hora de realizar futuras modificaciones.

## Estructura

No existe un estándar de organización del proyecto, he optado por organizarlo de la siguiente forma : 

- assets/
    - sass/
        - dist/css/			
            - style.min.css
            - style.min.css.map
        - source/
            - abstracts/
                 - _functions.scss
				 - _mixins.css
                 - _variables.scss
            - base/
				 - _base.scss
                 - _fonts.scss
				 - _helpers.scss
            - components/
                 - _buttons.scss
				 - _forms.scss
				 - _table.scss
				 
            - layout/
                 - _footer.scss
                 - _header.scss
                 - _grid.scss             
            - pages/
                 - _home.scss            
            - vendors/
                 - bootstrap/grid.scss
                 - normalize.scss
                 
         
		 - prime-dipujaen-theme.scss
         - prime-dipujaen-theme.css
         - prime-dipujaen-theme.css.map
     - js/
     - img/



## Contenido de cada carpeta

Ahora veamos la finalidad de cada una de las carpetas:

La carpeta /#base contiene las tipografias de proyecto, reset y normalizaciones de elementos HTML para eliminar inconsistencias.
La carpeta /#layout contendrá la distribución de tu aplicación, incluso partes de la web en si misma.
En /#components guardaremos porciones del proyecto. Sería como si trataramos con widgets.
En la carpeta /#pages incluiremos estilos para cada página y de esta manera poder localizarlos más rápidamente (home.scss, login.scss, etc..)
/#abstracts es una carpeta muy importante y en la que incluyo helpers, mixins, funciones, variables y otras herramientas.
En /#vendor incluiremos archivos de librerías externas y que necesitar� nuestro proyecto para poder funcionar.

## Fichero principal

#prime-dipujaen-theme.scss

@charset "UTF-8";

// 1. Configuration and helpers
@import
  'abstracts/variables',
  'abstracts/functions',
  'abstracts/mixins';

// 2. Vendors
@import
  'vendors/normalize',
  'vendors/bootstrap/grid';

// 3. Base stuff
@import
  'base/base',
  'base/fonts',
  'base/helpers';
 
// 4. Layout-related sections 
@import
  'layout/header', 
  'layout/footer';
  
// 5. Components
@import 
  'components/button',  
  'components/table', 
  'components/forms';        