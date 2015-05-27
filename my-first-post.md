Date: 2012-04-23 18:30
Title: A Universal Greeting
Category: Blog
Tags: blogging, test, pelican

Este es un blog hospedado en Dropbox usando el servicio [Calepin](http://www.calepin.co/) y con edición en formato **Markdown** el mismo que usa Diaspora* y que me ha parecido genial. Si quieres usar este novedoso método de publicar y no quieres usar Pelican + Dropbox entonces puedes explorar [Pelican + Github](http://martinbrochhaus.com/2012/02/pelican.html). [Pelican](https://github.com/ametaireau/pelican) es un aplicación python para crear blogs estáticos y usando los formatos de texto Markdown (.md) y reEstructuredText (.rst).

Ésta es la configuración que seguí, aquí en Calepin:

![calepin config](http://dl.dropbox.com/u/1331087/images/Calepin_config.png "configuración Calepin")

* Antes de empezar lo primero que solicita el sitio es permiso para usar tu cuenta en Dropbox.

* El primer paso consiste en crear la cuenta y basta con ingresar el nombre que queramos para el sitio, ejemplo **edycop** para tener el sitio edycop.calepin.co 

* El segundo paso consiste en configurar la cuenta, para esto ingresa el *nombre del sitio*, tu cuenta en *disqus* para los comentarios de cada publicación que hagamos, y la cuenta en twitter para cualquier contacto. Si tienes un dominio propio y quieres redireccionarlo al sitio nombresitio.calepin.co entonces ingresalo en CNAME.

* El tercer paso, y también el único problema por ahora, es que cada vez que publiquemos a actualicemos un post debemos ir al sitio calepin.co y dar clic en el boton **Publish**. Segun su creador esto irá a cambiar en las próximas versiones.

Por ahora tengo el plugin de Dropbox para Nautilus en mi sistema GNU/Linux así que cuando quiero publicar voy al directorio que se crea por defecto (~/Dropbox/Apps/Calepin/) y allí creo los archivos .md (de Markdown) que van a ser mis publicaciones y aparecerán listadas en el sitio edycop.calepin.co. Desde luego llegados a este punto uno puede usar el editor de su preferencia. Más información de cómo escribir un post visitar la [guía rápida de Calepin](http://jokull.calepin.co/calepin-guide.html) .

### Update: (Jan 16, 2013)

Ahora Calepin usa la sintaxis [MultiMarkDown](https://github.com/fletcher/MultiMarkdown/blob/master/Documentation/MultiMarkdown%20User%27s%20Guide.md) la cual adiciona marcado para notas de pie de página, tablas, referencias cruzadas, atributos como alto y ancho para imágenes o borde, estilo de borde para enlaces, bibliografía al estilo Latex!, sintaxis para ecuaciones matemáticas! y glosarios.


