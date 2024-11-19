<h1 align="center">
  <br>
  <a href="https://github.com/ninpl/hugo-type-moon-theme"><img src="https://github.com/ninpl/hugo-type-moon-theme/blob/master/images/logo.png?raw=true" alt="LogoRepo" width="100"></a>
  <br>
  Hugo Type Moon Tema
  <br>
</h1>

<h4 align="center">Tema para <a href="https://gohugo.io/" target="_blank">hugo</a>, ligero y con diferentes características.</h4>

<p align="center">
  <a href="https://gohugo.io/">
    <img src="https://img.shields.io/badge/hugo-v0.50-brightgreen"
         alt="Hugo">
  </a>
  <a href="https://pages.github.com/">
    <img src="https://img.shields.io/badge/Static-%20Web-blue">
  </a>
</p>

<p align="center">
  <a href="#informacion">Informacion</a> •
  <a href="#uso">Uso</a> •
  <a href="#descargar">Descargar</a> •
  <a href="https://github.com/ninpl/hugo-type-moon-theme">English</a> •
  <a href="#colaboradores">Colaboradores</a> •
  <a href="#licencia">Licencia</a>
</p>

<p align="center"><img src="https://github.com/ninpl/hugo-type-moon-theme/blob/master/images/fondo.png?raw=true" width=600 alt="Imagen del ejemplo"></p>

<p align="center"><em>Imagen de la portada general del tema. More themes in <a href="https://themes.gohugo.io/">hugo.themes</a>.</em></p>

## Informacion

<img src="https://github.com/ninpl/hugo-type-moon-theme/blob/master/images/info.png?raw=true" align="right"
     alt="Info" width="200" height="320">
     
Un tema ~~Jekyll~~ Hugo de código abierto. Ideal para blogs y fácil de personalizar. Este tema es una adaptación del tema [Type](https://github.com/rohanchandra/type-theme) original creado por [Rohan Chandra](https://github.com/rohanchandra). Las características notables de este tema de Hugo son la integración de un sistema de comentarios impulsado por Disqus, Google Analytics y soporte de localización (l10n).

* **Google Analytics** - Sistema que se conecta fácilmente con Google Analytics para **registrar los datos de su sitio web en una métrica**. Siguiendo todo el flujo de tráfico que se genera.

* **Localización** - Toda la información de type-moon-theme está en un archivo, si no desea un sitio web en inglés, puede **cambiar al idioma** que desee fácilmente. Editando el archivo que contiene todas las cadenas relacionadas con el tema.

* **Retratos** - Puede personalizar las diferentes **entradas de artículos con los retratos** que desee. Simplemente cargándolos desde la raíz de los archivos de imagen. Modificando levemente la visión en cada una de las entradas.

* **Icono Descriptivo** - Iconos en la parte superior del título, que definen el contenido de la publicación para el lector. Por ejemplo, si hay un código dentro de una entrada, puede advertir usando esta opción. También hay opciones para **documentos, música, archivos**, entre otros.

* **Comentarios** - Comentarios a través de Disqus. Es un **servicio global de alojamiento de comentarios de blogs** para sitios web y comunidades en línea que utilizan una plataforma de red.

## Uso

Supongo que tienes instalado Git. Dentro de la carpeta de su web Hugo, ejecute

		$ hugo new site blog
    $ cd blog
		$ git init
    $ git submodule add https://github.com/ninpl/hugo-type-moon-theme.git themes/hugo-type-moon-theme
		$ echo 'theme = "hugo-type-moon-theme"' >> config.toml
		$ hugo server

Debería ver una carpeta llamada `hugo-type-moon-theme` dentro del directorio` themes` que creamos hace unos momentos.

* **exampleSite** - Copie la **carpeta de data** que está en exampleSite y péguela en la raíz del blog (./). Copie el archivo **config.toml** que está en exampleSite y péguelo en la raíz del blog.

> Para convertir la carpeta exampleSite en un sitio de demostración independiente, la propiedad themesDir se ha establecido en ../... De esta manera, puede obtener una vista previa de este tema ejecutando el servidor hugo dentro de la carpeta exampleSite.
> Debido a la ruta personalizada de themesDir, Hugo no podrá encontrar temas si copió config.toml en el directorio raíz de un sitio web regular de Hugo. Asegúrese de comentar la propiedad themesDir si usa el tema en producción.

 * **El archivo de configuración** - Ahora, echemos un vistazo a **config.toml**. Siéntete libre de jugar con **la configuración**.

---

| Parameter | Description |
| :-------: | :----------:|
| `baseurl = "https://replace-this-with-your-domain.com/"` | Cambiar por su dominio. |
| `languageCode = "es-es"` | Idioma de la web |
| `title = "Type moon theme"` | Título de la web |
| `theme = "hugo-type-moon-theme"` | Tema que contiene la web |
| `disqusShortname = "spf13"` | El sistema de comentarios opcional funciona con Disqus. Ingrese su nombre corto para habilitar la sección de comentarios debajo de sus publicaciones. Con el parámetro de frontmatter **disableComments** puede deshabilitar la sección de comentarios para cada página individualmente. |
| `googleAnalytics = ""` | Lo mismo se aplica a la activación de Google Analytics. Habilítelo ingresando el código de seguimiento de su sitio web. |
| `paginate = 10` | Publicación que tendrá cada página. |
| `themesDir = "../.."` | Descomente para levantar un sitio temporal de la carpeta de exampleSite, coméntelo para producción. |
| `author = "Your name"` | Autor de la web. |
| `description = "Add a description of your website"` | Descripción de la web. |
| `keywords = "keyA,keyB,keyC..."` | Claves para encontrar la web. |
| `avatar = "img/avatar.png"` | Avatar de su usuario, aparece en cada publicación. |
| `gravatar = "your@email.com"` | En caso de que tengas tu avatar en gravatar, puedes acceder a él a través de tu correo electrónico. |
| `headerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.<br><br>Remove all header text in **config.toml** to disable this feature."` | Texto de encabezado que aparece delante del fondo. |
| `headerImage = ""` | Imagen del encabezado que aparece en la página de inicio. |
| `copyright = "Released under the MIT license<br>Powered by [Hugo](//gohugo.io/) with the [Type Moon Theme](//github.com/moonantonio/hugo-type-moon-theme)"` | Copyright que está escrito al final de la web. |
| `title = "Type moon theme"` | Establecer título para la plantilla opengraph de Hugo |
| `mainSections = []` | Defina qué tipos de contenido se mostrarán en la página de inicio. |

---

* **El archivo de arquetipos** - Cada vez que cree **una nueva publicación**, obtendrá varias opciones para completar.

---

| Parameter | Description |
| :-------: | :----------:|
| `featureimage = "img/bg.png"` | Defina una miniatura ingresando la ruta relativa a la imagen en el parámetro de la publicación, de esta manera puede almacenarlas al lado del archivo de contenido o en la carpeta `static`. |
| `portraitimage = "img/portrait/portrait0000.png"` | Defina un retrato ingresando la ruta relativa a la imagen en el parámetro de la publicación, de esta manera puede almacenarlos al lado del archivo de contenido o en la carpeta `static`. |
| `title = "{{ replace .TranslationBaseName "-" " " | title }}"` | El título de la publicación. |
| `date = {{ .Date }}` | La fecha de entrada. |
| `draft = true` | Determina si la entrada está en modo borrador y, por lo tanto, no se procesará. |
| `tags = ["type"]` | Etiquetas separadas por comas. |
| `categories = ["type"]` | Categorías separadas por comas. |
| `menu = "nav"` | Puede definir las entradas del menú como desee enlazando una publicación o cualquier otro sitio. Primero, permítanos vincular una publicación que ha escrito. Podemos hacer esto en el frontmatter del archivo de contenido de la publicación configurando `menu` en` nav`. Eso es. |
| `type = "fa fa-file"` | Tipo de información encontrada dentro de la entrada. |
| `disableComments = "true"` | Desactivar comentarios. |

---

Para ver su sitio en acción, ejecute el servidor local integrado de Hugo.

    $ hugo server

Ahora entra [`localhost:1313`](http://localhost:1313) en la barra de direcciones de su navegador.

---

 <img src="https://github.com/ninpl/hugo-type-moon-theme/blob/master/images/info.png?raw=true" align="left"
     alt="Info" width="190" height="290">

## Descargar

Usted puede [descargar](https://github.com/ninpl/hugo-type-moon-theme/releases) la última versión instalable de **Hugo Type Moon Theme**.

## Colaboradores

1. ¡Bifurcalo!
2. Crea tu rama de características: `git checkout -b my-new-feature`
3. Confirme sus cambios: `git commit -am 'Add some feature'`
4. Empuje la rama: `git push origin my-new-feature`
5. Envíe una pull request: D

El proyecto ahora es mantenido por [N9+](https://github.com/ninpl), creado por [Rohan Chandra](https://github.com/rohanchandra), porteado por [digitalcraftsman](https://github.com/digitalcraftsman) y arreglado por [Andy Grunwald](https://github.com/andygrunwald) con ayuda de los colaboradores ([list](https://github.com/ninpl/hugo-type-moon-theme/graphs/contributors)).

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->

| [<img src="https://avatars3.githubusercontent.com/u/7427480?s=460&u=6c19110c744836fd6265dd1b4781e6ddd22dd20a&v=4" width="100px;"/><br /><sub><b>N9+</b></sub>](https://ninpl.com/)<br /> | [<img src="https://avatars2.githubusercontent.com/u/816965?s=460&u=cfac03d73d63c2f1f61e0ed4f88a8bfb88f24274&v=4" width="100px;"/><br /><sub><b>Rohan Chandra</b></sub>](https://github.com/rohanchandra)<br /> | [<img src="https://avatars0.githubusercontent.com/u/7010165?s=460&v=4" width="100px;"/><br /><sub><b>digitalcraftsman</b></sub>](https://github.com/digitalcraftsman)<br /> | [<img src="https://avatars1.githubusercontent.com/u/320064?s=460&u=9a53426eee768d13406cabcead926211cd3343a0&v=4" width="100px;"/><br /><sub><b>Andy Grunwald</b></sub>](https://github.com/andygrunwald)<br /> |  | | |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: |

<!-- ALL-CONTRIBUTORS-LIST:END -->


## Licencia
[MIT](https://github.com/ninpl/hugo-type-moon-theme/blob/master/LICENSE.md)

---

> [ninpl.com/](https://ninpl.com/) &nbsp;&middot;&nbsp;
> GitHub [@ninpl](https://github.com/ninpl)
