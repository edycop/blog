Date: 2013-07-29 18:00
Title: El Kernel Linux
Category: Blog
Tags: howto, guía, linux, kernel

## El Kernel Linux: Introducción

*Primeta parte del blog en linux.org: [The Linux kernel: Introduction](http://www.linux.org/posts/10427/) por Devyn C. Johnson*

En 1991, un estudiante finlandés llamado Linus Benedict Torvalds desarrolló el núcleo (kernel) del ahora popular sistema operativo. Él liberó la versión 0.01 de Linux en septiembre de 1991, y en febrero de 1992, licenció el kernel bajo la licencia GPL. La Licencia Pública General de GNU (GPL) da el permiso a las personas para usar, apropiar, modificar y distribuir el código fuente de forma legal y gratuita. Esto permite que el kernel sea muy popular, ya que cualquiera puede descargarlo de forma gratuita. Hoy en día que cualquiera puede crear su propio kernel, puede ser útil saber cómo conseguir, editar, configurar, compilar e instalar el kernel Linux.

Un kernel es el corazón de un sistema operativo. El sistema operativo está compuesto por todos los programas que administran el hardware y permite a los usuarios ejecutar las aplicaciones en un computador. El kernel controla el hardware y las aplicaciones. Las aplicaciones no se comunican directamente con el hardware, sino que hacen llamados al kernel. En resumen, el software se ejecuta sobre el kernel y el kernel controla el hardware. Sin un kernel, un computador es un objeto inútil.

Hay muchas razones por las que un usuario desee hacer su propio kernel. Muchos usuarios pueden querer desarrollar un kernel que sólo contenga el código necesario para ejecutar en su equipo. Por ejemplo, mi kernel tiene controladores (drivers) para los dispositivos FireWire, pero mi equipo no tiene estos puertos. Cuando el sistema arranca, se desperdicia tiempo y espacio de memoria RAM en controladores para dispositivos que mi equipo no tiene. Si quería agilizar mi kernel, podría desarrollar mi propio kernel que no tenga controladores para FireWire. Así como por la otra razón, un usuario puede tener un dispositivo con una pieza especial de hardware, pero el kernel con el que viene la última versión de Ubuntu le falta el controlador necesario. Este usuario podría descargar la última versión del kernel (que está un par de versiones por delante del kernel de Ubuntu) y desarrolla su propio kernel que tiene el controlador necesario. Estas son dos de las razones más comunes por las que los usuarios quieran desarrollar su propio kernel Linux.

Antes de descargar un kernel, debemos mencionar algunas definiciones y datos importantes. El kernel Linux es un kernel monolítico. Esto significa que todo el sistema operativo está en un espacio de la memoria RAM reservado para el núcleo. Es decir, el núcleo o kernel se carga en la memoria RAM. El espacio utilizado por el kernel es reservado por el kernel. Sólo el kernel puede usar el espacio reservado para él. El núcleo se apropia del espacio en la RAM hasta que el sistema se apaga. En contraste al espacio del kernel, está el espacio de usuario. El espacio de usuario es el espacio en la memoria RAM ocupado por los programas del propio usuario. Las aplicaciones como navegadores web, vídeo juegos, procesadores de texto, reproductores multimedia, el fondo de pantalla, temas, etc., todos ellos están en el espacio de usuario de la RAM. Cuando una aplicación se cierra, cualquier programa puede utilizar el nuevo espacio libre. Con el espacio del kernel, una vez que se toma el espacio de la RAM, nadie más puede tomar dicho espacio.

El kernel Linux también es un kernel de multitarea preferente. Esto significa que el kernel detendrá algunas tareas con tal de asegurar que cada aplicación tenga la oportunidad de utilizar la CPU. Por ejemplo, si una aplicación se está ejecutando pero está a la espera de algunos datos, el kernel pondrá dicha aplicación en espera y permitirá que otro programa utilice los recursos recién liberados de la CPU hasta que lleguen los datos. De lo contrario, el sistema estaría desperdiciando recursos para las tareas que están a la espera de datos u otro programa a ejecutar. El kernel forzará a los programas a esperar por la CPU o dejar de usarla. Las aplicaciones no pueden continuar o usar la CPU sin el consentimiento del kernel.

El kernel Linux hace que los dispositivos aparezcan como archivos en el directorio */dev*. Los puertos USB, por ejemplo, se encuentran en */dev/bus/usb*. Las particiones del disco duro se ven en */dev/disk/by-label*. Es por esta característica que muchas personas dicen "En Linux, todo es un archivo". Aunque si un usuario desea acceder a los datos en su memoria USB, por ejemplo, no puede acceder a los datos usando estos archivos.

El kernel Linux es portable. La portabilidad es una de las mejores características que hace popular a Linux. La portabilidad es la capacidad del kernel para trabajar en una amplia variedad de procesadores y sistemas. Entre algunos de los procesadores que soporta el kernel están Alpha, AMD, ARM, C6X, Intel x86, Microblaze, MIPS, PowerPC, SPARC, UltraSPARC, entre otros. Esta no es una lista completa.

En el directorio de arranque (*/boot*), los usuarios verán un archivo "vmlinux" o "vmlinuz". Ambos son núcleos Linux compilados. El que termina con una "z" está comprimido. El "vm" es por ***memoria virtual***. En los sistemas con procesadores SPARC, lo que verán los usuarios será un archivo zImage. Un número reducido de usuarios puede encontrar un archivo bzImage; el kernel Linux comprimido. No importa cual de ellos tenga el usuario, todos son archivos de arranque que no deben cambiarse a menos que el usuario sepa lo que está haciendo. De lo contrario, puede hacer que su sistema no arranque --el sistema no encenderá [^1].

[^1]: Para leer una explicación de la jerarquía del sistema de archivos en español puedes revisar [archeando.wordpress.com](http://archeando.wordpress.com/2013/08/04/jerarquia-del-sistema-de-ficheros-en-arch/)

El código fuente son las instrucciones de un programa. Con el código fuente, los programadores pueden realizar cambios en el kernel y ver cómo funciona el kernel.

### Descargar el kernel

Ahora que entendemos más sobre el kernel o núcleo, es el momento de descargar el código fuente. Ir a [kernel.org](http://kernel.org) y hacer clic en el botón grande para descargarlo. Una vez finalizada la descarga, descomprimir el archivo descargado.

Para este artículo, estoy usando el código fuente del kernel Linux 3.9.4. Todas las instrucciones en esta serie de artículos son las mismas (o casi las mismas) para todas las versiones del kernel.

En mi próximo artículo, hablaremos de cómo está organizado el código fuente.


## El Kernel Linux: El Código Fuente

*Segunda parte del blog en linux.org: [The Linux Kernel: The Source Code](http://www.linux.org/threads/the-linux-kernel-the-source-code.4204/) por Devyn C. Johnson*

Después de descargar y descomprimir el código fuente del kernel, los usuarios verán muchos directorios y archivos. Puede llegar a ser un verdadero reto tratar de encontrar un archivo en particular. Afortunadamente, el código fuente se ordena de una manera específica. Esto permite a los desarrolladores encontrar cualquier archivo o parte del núcleo.

La raíz del código fuente del kernel contiene los directorios que aparecen a continuación.

> arch

> block

> crypto

> Documentation

> drivers

> firmware

> fs

> include

> init

> ipc

> kernel

> lib

> mm

> net

> samples

> scripts

> security

> sound

> tools

> usr

> virt

Además hay algunos archivos que se encuentran en la raíz del código fuente. Se listan en la tabla a continuación.

| Archivo  | Descripción |
| :------------: | ----------- |
| **COPYING** | Información sobre licencias y derechos. El kernel Linux está licenciado bajo la licencia GPLv2. Esta licencia otorga a cualquier persona el derecho de usar, modificar, distribuir y compartir de forma gratuita tanto el código fuente como el código compilado. Sin embargo, nadie puede vender el código fuente. |
| **CREDITS** | Lista de contribuyentes. |
| **Kbuild** | Este es un script que establece algunas configuraciones para compilar el kernel. Por ejemplo, este script configura la variable ARCH donde ARCH es el tipo de procesador que un desarrollador quiere que el núcleo soporte. |
| **Kconfig** | Este script se utiliza cuando el desarrollador configura el kernel; este tema se discutirá luego en un otro artículo.|
| **MAINTAINERS** | Esta es la lista de los mantenedores actuales, sus correos, página web, y el archivo o la parte del kernel en la que se especializan en desarrollar y mantener. Esto es útil para cuando un desarrollador encuentra un error en el kernel y desea reportar el problema al mantenedor que puede manejar el problema. |
| **Makefile** | Este script es el archivo principal que se utiliza para compilar el kernel. Este archivo pasa parámetros al compilador, así como la lista de archivos a compilar y cualquier otra información necesaria. |
| **README** | Este archivo de texto contiene información para los desarrolladores que quieren saber cómo compilar el kernel.|
| **REPORTING-BUGS** | Este documento de texto contiene información sobre los reportes de errores. |

El código fuente del kernel estará en archivos con extensión ".c" o ".h". La extensión ".c" indica que el kernel está escrito en C, uno de los muchos lenguajes de programación. Los archivos ".h" son archivos de cabecera, y también están escritos en C. Los archivos de cabecera contienen código que se usan en otros archivos ".c". Esto ahorra tiempo a los programadores, ya que pueden utilizar dicho código en lugar de escribir nuevo código. De lo contrario, código que realiza la misma acción se repetiría en muchos o todos los archivos ".c". Además, eso consume y desperdicia espacio en disco duro.

Todos los archivos de los directorios listados anteriormente están bien organizados. Los nombres de las directorios ayudan a los desarrolladores a por lo menos tener una buena idea sobre su contenido. A continuación se proporcionan un árbol de directorios y sus descripciones.

**arch** - Este directorio contiene un ***Kconfig*** que proporciona algunas configuraciones para compilar el código fuente que está en este directorio. Cada arquitectura de procesador soportada está en el directorio correspondiente. Por lo tanto, el código fuente de procesadores Alpha está en el directorio alpha. Tenga en cuenta que a medida que pasa el tiempo, se soportarán nuevos procesadores, o algunos pueden ser retirados. Para el kernel Linux v3.9.4, estos son los directorios en arch:

> alpha

> arc

> arm

> arm64

> avr32

> blackfin

> c6x

> cris

> frv

> h8300

> hexagon

> ia64

> m32r

> m68k

> metag

> microblaze

> mips

> mn10300

> openrisc

> parisc

> powerpc

> s390

> score

> sh

> sparc

> tile

> um

> unicore32

> x86

> xtensa

**block** - Este directorio contiene código para los controladores de dispositivo en bloque. Los dispositivos en bloque son dispositivos que reciben y envían datos en bloque. Los datos en bloque son trozos grandes de datos en lugar de un flujo continuo de ellos.

**crypto** - Este directorio contiene el código fuente de muchos algoritmos de cifrado. Por ejemplo, "sha1_generic.c" es el archivo que contiene el código para el algoritmo de cifrado SHA1.

**documentation** - Este directorio contiene los documentos en texto plano (sin formato) que proporcionan información sobre el kernel y muchos de los archivos. Si un desarrollador necesita información, puede ser de gran utilidad empezar a buscarla aquí.

**drivers** - Este directorio contiene el código de los controladores. Un controlador es un programa que gestiona un dispositivo hardware. Por ejemplo, para que un computador entienda el teclado y lo haga usable, es necesario un controlador de teclado. Existen muchos directorios aquí. Cada directorio es nombrado de acuerdo al dispositivo o el tipo de hardware. Por ejemplo, el directorio *bluetooth* contiene el código para los controladores *bluetooth*. Otros controladores cómunes son *scsi*, *usb* y *FireWire*. Algunos controladores pueden ser más difíciles de encontrar. Por ejemplo, los controladores del *joystick* no están en un directorio *joystick*. En su lugar de eso, se encuentran en *./drivers/input/joystick*. Los controladores del teclado y ratón también se encuentran en el directorio *input*. El directorio *Macintosh* contiene código para el hardware fabricado por Apple. El directorio *xen* contiene el código para el hipervisor Xen. Un hipervisor es software o hardware que permite a los usuarios ejecutar múltiples sistemas operativos en un solo equipo. Esto significa que el código *xen* permitiría a los usuarios tener dos o más sistemas Linux ejecutándose al mismo tiempo en un computador. Además los usuarios pueden correr Windows, Solaris, FreeBSD, o algún otro sistema operativo sobre el sistema Linux. Hay muchas otros directorios en *drivers*, pero son muy numerosos para mencionarlos en este artículo, pero lo haremos en un posterior artículo.

**firmware** - El directorio *firmware* contiene código que permite al computador leer y entender las señales de los dispositivos. Por ejemplo, una cámara web maneja su propio hardware, pero el computador debe entender las señales digitales que está enviando la cámara web. Entonces, el sistema Linux usará el firmware *vicam* para entender a la cámara. De lo contrario, sin el firmware, el sistema Linux no sabrá cómo procesar la información que la cámara web le envía. Además, el firmware ayuda al sistema Linux a enviar mensajes al dispositivo. El sistema Linux podría entonces decirle reenfocar o girar.

**fs** - Este es el directorio del sistema de archivos (File System). Todo lo que el código necesita para comprender y utilizar los sistemas de archivos está aquí. Dentro de este directorio, el código de cada sistema de archivos está en su propio directorio. Por ejemplo, el código del sistema de archivos ext4 está en la carpeta *ext4*. Dentro del directorio *fs*, los desarrolladores podrán ver algunos archivos sin directorios. Estos archivos manejan todos los sistemas de archivos. Por ejemplo, *mount.h* contendrá el código para el montaje de los sistemas de archivos. Un sistema de archivos es una forma estructurada de almacenar y gestionar archivos y directorios en un dispositivo de almacenamiento. Cada sistema de archivos tiene sus propias ventajas y desventajas. Estas se deben a la programación del sistema de archivos. Por ejemplo, el sistema de archivos NTFS soporta compresión transparente (cuando está habilitado, los archivos se comprimen automáticamente sin que el usuario lo note). La mayoría de los sistemas de archivos no tienen esta característica, y sólo podrían tener esta capacidad si se programa en los archivos del directorio *fs*.

**include** - El directorio *include* contiene diversos archivos de cabecera que utiliza el kernel. El nombre del directorio viene de la sentencia "include" de C que se utiliza para importar un encabezado en código C en el proceso de compilación.

**init** - El directorio *init* tiene el código que se ocupa de la puesta en marcha del kernel (INITiation). El archivo *main.c* es el centro del kernel. Este es el archivo principal del código fuente que enlaza todos los demás archivos.

**ipc** - IPC es la abreviación de Comunicación Entre Procesos (Inter-Process Communication). Este directorio tiene el código que se encarga de la capa de comunicación entre el kernel y los procesos. El kernel controla el hardware y los programas sólo pueden solicitar al kernel realizar una tarea. Supongamos que un usuario tiene un programa que abre la bandeja de DVD. El programa no abre la bandeja directamente. Sino que el programa informa al kernel que la bandeja se debe abrir. Entonces, el kernel abre la bandeja mediante el envío de una señal al hardware. Este código también gestiona las señales de terminación. Por ejemplo, cuando un administrador de sistemas abre un gestor de proceso para cerrar un programa que se ha bloqueado, la señal para cerrar el programa es lo que se llama una señal de terminación. El kernel recibe la señal y entonces el kernel (dependiendo del tipo de la señal de terminación) pedirá al programa parar o el kernel simplemente sacará el proceso de la memoria y la CPU. Las tuberías o pipes utilizados en la línea de comandos también emplean la IPC. Las tuberias le dicen al kernel que coloque los datos de salida en una página física de la memoria. El programa o comando siguiente que recibe los datos se le da un puntero a la página de dicha memoria.

**kernel** - El código de este directorio controla el propio kernel. Por ejemplo, si un depurador necesita rastrear un problema, el kernel usaría el programa que se originó a partir de los archivos fuente de este directorio para informar al depurador de todas las acciones que realiza el kernel. Además aquí hay código para mantener la noción de tiempo. En el directorio *kernel* está un directorio denominado "*power*". Parte del código de este directorio provee las funcionalidades para reiniciar, apagar y suspender el computador.

**lib** - El directorio *library* tiene el código para las librerías del kernel, que es un conjunto de archivos que el kernel necesitará referenciar en algún momento.

**mm** - El directorio de Administración de Memoria (*Memory Management*) contiene el código para la gestión de la memoria. La memoria no está organizada aleatoriamente en la RAM. Sino que el kernel coloca cuidadosamente los datos en la RAM. El kernel no sobrescribe ninguna memoria que se está utilizando o que contenga datos importantes.

**net** - El directorio *network* contiene el código para los protocolos de red. Esto incluye el código para IPv6 y Appletalk, así como los protocolos para Ethernet, wifi, bluetooth, etc. Además, el código de manejo de puentes de red y resolución de nombres DNS se encuentran en el directorio *net*.

**samples** - Este directorio contiene código fuente de ejemplo y módulos que se están empezando a desarrollar. Se desea que se desarrollen nuevos módulos con características útiles; pero ningún programador ha anunciado que vaya a trabajar en el proyecto. Pues bien, esos módulos van aquí. Esto le da a los nuevos programadores del kernel la oportunidad de ayudar al pasar por este directorio y elegir un módulo en que les gustaría ayudar a desarrollar.

**sripts** - Este directorio contiene los *scripts* necesarios para compilar el kernel. Lo mejor es no cambiar nada en este directorio. De lo contrario, es posible que no pueda configurar o compilar el kernel.

**security** - Este directorio tiene el código para la seguridad del kernel. Es importante proteger el kernel de los virus informáticos y hackers. De lo contrario, el sistema Linux puede ser dañado. La seguridad del kernel se discutirá en un posterior artículo.

**sound** - Este directorio tiene el código de los controladores de sonido para las tarjetas de sonido/audio.

**tools** - Este directorio contiene herramientas que interactúan con el kernel.

**usr** - ¿Recuerda el archivo *vmlinuz* y archivos similares mencionados en el artículo anterior? El código en este directorio crea esos archivos después de compilar el kernel.

**virt** - Este directorio contiene el código para *virtualización* el cual permite a los usuarios ejecutar múltiples sistemas operativos al mismo tiempo. Esto es diferente de *Xen* (mencionado anteriormente). Con *virtualización*, el sistema operativo invitado está actuando como cualquier otra aplicación dentro del sistema operativo Linux (sistema anfitrión o host/servidor). Con un hypervisor como Xen, los dos sistemas operativos están gestionando el hardware juntos y al mismo tiempo. En la *virtualización*, el sistema operativo invitado se ejecuta en la parte superior del kernel Linux, mientras que en un hipervisor, no hay sistema operativo invitado y todos los sistemas operativos no dependen uno del otro.

Tip: Nunca mueva un archivo en el código fuente del kernel a menos que sepa lo que está haciendo. De lo contrario, la compilación fallará debido a un archivo "no encontrado" (*missing file*).

La estructura de direcorios del kernel Linux se ha mantenido relativamente constante. Los desarrolladores del kernel han hecho algunas modificaciones, pero en general, esta configuración es la misma en todas las versiones del kernel. El esquema del directorio de controladores (*drivers*) sigue siendo la misma. En el siguiente artículo hablaremos sobre los controladores del kernel. 


## El kernel de Linux: Controladores

*Tercera parte del blog en linux.org: [The Linux kernel: Drivers](http://www.linux.org/article/view/-the-linux-kernel-drivers) por Devyn C. Johnson*

Los controladores son pequeños programas que permiten al kernel para comunicar y manejar el hardware o los protocolos (reglas y normas). Sin un conductor, el kernel no sabe cómo comunicarse con los protocolos de hardware o el mango (el kernel realmente entrega las órdenes a la BIOS y el BIOS los pasa en el hardware). El código fuente del kernel de Linux contiene muchos controladores (en forma de código fuente) en la carpeta drivers. Se explicará cada carpeta dentro de la carpeta drivers. Al configurar y compilar el kernel, que ayuda a entender los drivers. De lo contrario, un usuario puede agregar controladores al kernel que no necesitan o dejar de lado importantes factores. El código fuente del controlador por lo general incluye una línea comentado que establece el propósito del controlador. Por ejemplo, el código fuente del controlador tc tiene una sola línea comentó que dice el conductor de autobuses TurboChannel. Debido a la documentación, los usuarios deben ser capaces de ver las primeras líneas comentadas de los futuros conductores aprendan su propósito.






*Traducción libre por Edwin Caldon, CC: by-nc-sa*

