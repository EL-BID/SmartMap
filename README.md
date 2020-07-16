*Esta herramienta digital está publicada en la página web de la iniciativa [Código para el Desarrollo](http://code.iadb.org/es/repositorio/22/smartmap)*

## SMARTMAP
[![Analytics](https://gabeacon.irvinlim.com/UA-4677001-16/SmartMap/readme?useReferer)](https://github.com/EL-BID/SmartMap)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=EL-BID_SmartMap&metric=alert_status)](https://sonarcloud.io/dashboard?id=EL-BID_SmartMap)

### Descripción
---
SmartMap es una herramienta para visualizar, analizar y superponer datos geográficos. Los usuarios pueden elegir entre docenas de indicadores sociales, económicos y ambientales, extraídos de fuentes públicas de información, para crear mapas personalizados y detallados.

La información disponible en SmartMap se basa en los datos oficiales publicados por los organismos nacionales e internacionales a los que se hace referencia. La política adoptada para definir los límites administrativos no refleja ninguna posición oficial del Grupo del BID y del FOMIN.

Los resultados del análisis deben considerarse meramente indicativos y de cualquier forma no se deben utilizar referencias en situaciones críticas o de emergencias. El equipo de NEXSO SmartMap agradece cualquier comentario, observación o sugerencia con respecto a la información contenida en esta aplicación y sus funcionalidades.

### Arquitectura de aplicaciones
---
Smartmap es una aplicación modular del tipo MVC basadaa en Backbonejs y JQuery en el cliente y ESRI ArcGis del lado del servidor.

Cliente

- /js - aplicación principal
- /ja/component - Modulos de la aplicación
- /ja/component/smartmap-ui - Contenedor principal de la interfaz


Servidor

La aplicación consume servicio remoto de datos geográficos en un servidor público del BID. Para configurar el servicio, consulte /js/config/config.js

Advertencia:

> El servicio actual está temporalmente sin conexión.

Recuerda:

> Smartmap está diseñado para incorporarse en otras aplicaciones. Por lo tanto, se puede reutilizar por separado los módulos instanciados en smartmap-ui.

### Vamos más allá, hacer que sea de código abierto social
---
El software es una herramienta fundamental para el diseño e implementación de proyectos y programas. Esta herramienta se abre bajo el programa de [Código para el Desarrollo](code.iadb.org) del BID, que busca consolidar su compromiso con el uso y promoción del conocimiento abierto, así como acelerar el diálogo sobre cómo la tecnología puede impulsar el desarrollo de América Latina y el Caribe.

### Requisitos de desarrollo
---

- NodeJS
- grunt-cli (Se necesita instalar globalmente see: https://github.com/gruntjs/grunt-cli#grunt-cli-)
- Sass CSS Importer ( $ gem install --pre sass-css-importer )
- Compass ($ gem install compass)
- Browser-Sync

### Cómo instalar 
---

Navega hasta `cd js/components/smartmap-ui`:

- `npm install`
- `grunt init --force` (instala las depencias de Bower, se requiere parar el proceso para continuar, utiliza Ctrl +c. Se ejecuta el comando forzado por un bug que se debe resolver.)
- `grunt build`

Navega al directorio raiz de tu aplicación

- `npm install`
- `grunt init --force` (instala las depencias de Bower)
- `grunt build`

Abre una nueva terminal y ejecuta Browser Sync para cargar un servidor HTTP

- `browser-sync start --server --files "css/*.css"`

Voila !! Todo esta listo y corriendo.

Recuerda:

> Cada vez que necesite reconstruir completamente el proyecto ejecuta `grunt build` en el directorio smartmap-ui y una vez completado ejecuta `grunt build` en la raíz de la aplicación.

### Desarrollo
---

Durante la fase de desarrollo, se recomeinda ejecutar el observaodr de grunt para vigilar el directorio smartmap-ui y el raíz.
- `grunt watch` en el directorio raíz
- `grunt watch --force` en el directorio smartmap-ui (para evitar errores del tipo linting durante el desarrollo)
- en lugar de usar --force, también puede agregar `debug ': true` al archivo `smartmap-ui / .jshintrc`

La aplicación se debe ejecutar en el directorio raíz.

### Cómo contribuir
---

Consulte el archivo de contribución (contribution) en este repositorio.

### Mejoras Identificadas
---

Identificamos varios puntos para mejorar Smartmap.

1. Cambiar el motor del mapa.
2. Corregir los errores de codigo.
3. Implementar el funcionalidades de Social Media
4. Implementar guardar mi mapa.
5. Actualizar bibliotecas y referencias.
6. Mejorar la documentación en el código.
7. Mejorar el rendimiento del código.

### Más información
---
## Análisis de calidad
De acuerdo al sistema de evaluación de software definido en la guía de ciclo de vida de desarrollo de software, el análisis de esta herramienta ha generado la siguiente evaluación:

* Blocker issues: 74 (> 0) **Low** 
* Duplicated lines: 1.3% (< 15%) **Hard**
* Critical issues: 41 (> 20) **Standard**
* Technical debt: 72d (> 60d) **Low**
* Test coverage: 0% (< 10%) **Low**

Más información en [este link.](https://el-bid.github.io/software-life-cycle-guide/delivery/evaluation-matrix/)

### Licencia
---

Licencia MIT

### Autores
BID

- Jairo Anaya @jairoanaya

ESRI

- Josh Petterson @jpeterson

- Allison Sizer @Alison Sizer

Flipside

- Olaf Verman

- Ricardo Saavedra


Sinapsis Innovation

- Cristian Agudelo @ crstn210

### Otros enlaces

Http://server.arcgis.com/en/

Http://www.nexso.org/smartmap
