Date: 2013-02-03 18:00
Title: Agregar un POI con JOSM
Category: Blog
Tags: blogging, howto, guía, OSM, JOSM

*Del blog weait.com: [Add a POI from JOSM](http://weait.com/content/add-poi-josm) (2013)*

![image-1](http://weait.com/sites/default/files/field/image/josm-site.png)

Existen varios editores con los que se puede contribuir con OpenStreetMap. Algunos dicen que JOSM es una gran herramienta. Otros lo describen como "opaco" o de "pocos amigos". La verdad es que JOSM es selectivo con sus amigos. Así que vamos a hacerle unos cuantos amigos a JOSM.

## Conociendo a JOSM

Java OpenStreetMap o JOSM está desarrollado en Java y por lo tanto debería correr en cualquier computador que tenga Java. Las [instrucciones de instalación](http://josm.openstreetmap.de/wiki/Es:InstallNotes) cubren MacOSX, *BSD y Windows. Hay otras opciones de instalación pero probablemente quieras sólo ejecutar la [versión de prueba de JOSM](http://josm.openstreetmap.de/josm-tested.jar). Una versión de JOSM que contiene las últimas funcionalidades y sus actualizaciones además de ser la preferida por los maperos audaces.

![image-2](http://dl.dropbox.com/u/1331087/images/osmco-image1.png)

Una vez instalado (o descargado) y ejecutado, JOSM mostrará un mensaje con las últimas noticias del proyecto. Además te dirá las actualizaciones de la versión de prueba de JOSM, como son frecuentes las actualizaciones deberías estar pendiente si sale una nueva versión.

## Seleccionar un área para Editar con JOSM

En la figura también se muestra el icono de *Descargar datos del servidor OSM* (Download from OpenStreetMap) (icono de flecha apuntando hacia abajo). Aquí es donde inician la mayor parte de las ediciones de OSM. Presione el icono *Descargar datos del servidor OSM*.

JOSM mostrará otra ventana con ciertas pestañas:

![image-3](http://dl.dropbox.com/u/1331087/images/osmco-image2.png)

Hay una gran cantidad de opciones en esta ventana. Por ahora nos concentraremos en los fundamental; descargar tu área de interés.

Haga clic en la pestaña "Mapa Deslizante" (Slippy Map) para desplegar el mapa.
Asegurate que la opción *Datos OpenStreetMap* (OpenStreetMap data) esté seleccionada y la opción *Datos GPS en bruto* (Raw GPS data) deseleccionada. La opción en parte inferior *Descargar como nueva capa* (Download as new layer) debería estar deseleccionada.

Maximice el área de interés (con la rueda del ratón). Se recomienda que esta área sea pequeña. Es mejor tener pocas cuadras alrededor de la ubicación de tu punto de interés (**POI**, Point Of Interest).

Para maximizar el área gire la rueda del ratón hacia adelante y para alejarse gire la rueda en sentido contrario.

Puede desplazarse por el mapa "agarrándolo" y moviendolo. Manteniendo presionado el botón derecho del ratón puede "agarrarlo". Esto depende mucho del software y del sistema operativo que estés usando. Explora, y luego será cuestión de acostumbrarse. **Mantenga presionado el botón derecho del ratón y mueva el mapa**.

Si necesitas moverte por una zona grande, considera primero alejarte del área, moverte y luego maximizarla de nuevo. Además el puntero del ratón te sirve como guía, lo descubrirás con la práctica.

Ahora que se ha acercado a la zona de interés, tendrá que seleccionar el área a descargar. Manteniendo presionado el botón izquierdo del ratón, arrastre el puntero para dibujar un cuadro en el mapa. Este es el cuadro límite que se descargará desde el servidor de OSM. Probablemente desee seleccionar unas pocas cuadras a ambos lados de su punto de interés para crear contexto. Dibuje el rectángulo de selección, y presione el botón *Descargar* (Download) situado en la parte inferior izquierda para bajar esta área desde el servidor de OSM para su edición.

![image-4](http://dl.dropbox.com/u/1331087/images/osmco-image3.png)

Cuando los datos se descargan del servidor, JOSM mostrará un área ligeramente mayor. La zona "sombreada con lineas oblicuas" que se muestra fuera del área que se ha descargado es para recordarle que no debe editar fuera del área que se descargó desde el servidor. Se muestran algunos elementos fuera del límite del cuadro porque estos hacen parte del cuadro delimitador, si se quiere editar algo que esté fuera del recuadro, se vuelve a hacer el proceso de descarga.

Ahora puede acercarse más a la zona en la que va a editar. En este caso, estoy acercándome a la esquina de *Fisher Mills Road y Scott*, porque ahí es donde está pizza Tito.

## Modo Selección

![image-5](http://dl.dropbox.com/u/1331087/images/osmco-image4.png)

La barra lateral izquierda muestra que el *modo selección* está activo. Se sabe que es el *modo de selección* porque está seleccionado el icono de la mano con un rectángulo punteado. Puedes elegir el *modo selección* presionando la tecla "s" o haciendo clic en el icono de la mano de la barra lateral izquierda. Se selecciona la calle con sentido oriente - occidente, la calle Fisher Mills, que cuando se selecciona se muestra como una línea roja con flechas. Cuando se selecciona un objeto en JOSM, las propiedades del objeto se muestran en el *panel propiedades* a la derecha del mapa. Puedes corroborar que estás buscando en el área correcta, al ver los nombres de las calles.

Además de seleccionar un solo objeto haciendo clic en él, se puede seleccionar un grupo de objetos manteniendo presionado el botón izquierdo y arrastrando un recuadro de selección. Pero no hagas eso ahora. Pulsa "Esc" para deseleccionar todo.

## Modo Adición

Para agregar un nodo, cambie al *modo adición* presionando la tecla "a" o haciendo clic en el icono "Dibujar nodos" (Draw nodes) de la barra lateral izquierda. EL *modo adición*, a veces conocido como el *modo dibujo*, se corrobora al ver que el puntero del ratón cambia a una cruz, o símbolo de suma. Cualquier punto añadido será agregado en el centro de la cruz.

## Agregar un Punto de Interés desde un Predefinido

Coloque el nodo (o punto) para "Pizza Tito", en la esquina nororiente de la calle "Fisher Mills" y la calle "Scott". Haga clic izquierdo una vez para colocar un nodo. Si mueve el ratón lejos del nodo, verá una línea que se extiende, como una banda elástica, hacia el puntero del ratón. El *modo adición* está diseñado para dibujar una línea de varios nodos. Pero eso es un tema para otro tutorial, por el momento dejamos de añadir nodos. Presiona "s" para volver al *modo selección*. El nuevo nodo aparecerá resaltado en rojo para indicar que está seleccionado.

Haga clic en un espacio vacío del mapa y verás que el nuevo nodo cambia a un cuadrado hueco amarillo. Selecciónelo de nuevo haciendo clic una vez en él mientras está en *modo selección*. No hemos asignado las propiedades de este nodo, así que el panel de propiedades aún está en blanco. Vamos a arreglar eso. Es hora de hacer de este nodo un "Pizza Tito".

## Menú de Predefinidos

![image-6](http://dl.dropbox.com/u/1331087/images/osmco-image5.png)

Mientras que el nuevo nodo esté seleccionado, en la barra de menú principal, seleccione *Predefinidos* >> *Instalaciones* >> *Comida + Bebidas* >> *Establecimiento de comida rápida* (Presets >> Facilities >> Food + Drinks >> Fast Food). Haga clic en *Establecimiento de comida rápida* para abrir la ventana de propiedades de la etiqueta predefinida.

![image-7](http://dl.dropbox.com/u/1331087/images/osmco-image6.png)

Ingrese los valores para *Nombre*: "Pizza Tito" y *Cocina*: pizza. No sé el horario de apertura, así que lo dejaré en blanco y a continuación presioné el botón *Aplicar Predeterminados* (Apply Preset) para guardar la información localmente.

Ahora podemos ver que el nodo ha cambiado a un icono de una hamburguesa y una bebida para representar la comida rápida. En el panel de propiedades (a la derecha) nos dice que este nodo tiene los datos: name=Pizza Tito, amenity=fast_food, cousine=pizza, así que todo va bien:

![image-8](http://dl.dropbox.com/u/1331087/images/osmco-image7.png)

## Subir datos a OpenStreetMap

Pulse el botón "Subir" (Upload) (icono de flecha apuntando hacia arriba) de la barra de iconos principal para subir el nuevo Punto de Interés. JOSM le presentará una ventana, en la que mostrará una lista de los cambios realizados, y le pedirá un comentario para el conjunto de dichos cambios. Agregar un comentario a los cambios realizados es útil para resumir lo que has hecho en la sesión de edición, que en este caso puede ser algo como "Agregado un POI de un restaurante en Cambridge Ontario".

Si antes no se han subido datos con JOSM, se le pedirá su nombre de usuario y contraseña de OpenStreetMap. Tu nombre de usuario OSM es la dirección de correo con la que te registraste, no tu nombre de usuario público. Agrege la información necesaria en el cuadro de diálogo de autenticación y pulse *Autenticar* (Authenticate) para subir los cambios.

Felicitaciones. Ha agregado un restaurante local en OpenStreetMap.

## Referencias

* Guía de JOSM en Español en el Wiki de OSM: [Guía general](http://josm.openstreetmap.de/wiki/Es:WikiStart), [Sección de ayuda/documentación](http://josm.openstreetmap.de/wiki/Es:Help)


*Traducción por Edwin Caldon*

