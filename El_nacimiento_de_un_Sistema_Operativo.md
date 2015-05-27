Date: 2012-08-30 18:00
Title: El nacimiento de un Sistema Operativo
Category: Blog
Tags: blogging, linux, linus, sistema operativo

## Parte I

*Del libro Just for Fun de Linus Torvalds y David Diamond (2001)*

Algunas personas recuerdan el pasado según los autos que han conducido o los trabajos conseguidos o los lugares en los que han vivido o los amores que han tenido. Mis años están marcados por los computadores.

Tuve sólo tres computadores mientras crecí. Entre ellos estaba el mencionado Commodore  VIC-20, el cual heredé de mi abuelo [1]. Fue uno de los primeros computadores para "el hogar", los antecesores del actual PC (Computador Personal). El Commodore 64 vino a ser como el hermano mayor del VIC-20, luego fue un computador Amiga, que tenía un grupo importante de seguidores en Europa. Estos computadores nunca fueron realmente populares como el PC o incluso el Apple II, que ya era común en la época que yo jugaba con el VIC.

En esos días previos a la proliferación de los PCs, la mayor parte de la programación de los computadores "caseros" se hizo en lenguaje ensamblador (No puedo creer que haya empezado la oración con "En esos días …"). Los computadores tenían su propio sistema operativo desarrollado por aficionados, el equivalente de lo que fue el DOS para el PC. Dependiendo del computador, era ya sea un formato rudimentario o uno ligeramente mejorado. Igual que el DOS, el sistema operativo tenía un cargador de programa y un entorno básico de programación. En aquel entonces no existían estándares y una serie de empresas querían controlar el mercado. Commodore fue una de las más reconocidas en esto.

Cuando había conseguido casi tanto como pude, salí del VIC-20, empecé a ahorrar para un modelo de nueva generación. Este fue un gran reto en mi vida. Como ya he mencionado, había perdido la noción de que mi familia vivía en lo particular, el tiempo, entre otras cosas, pero el camino a mi segundo computador es algo difícil de olvidar.

Obtuve un poco de dinero de Navidad y cumpleaños, guardados celosamente (debido a que nací un 28 de Diciembre, las dos ocasiones se funden en una). También gané algo de dinero en el verano trabajando en el grupo de limpieza en los parques de Helsinki [2]. Muchos de los parques de Helsinki no son paisajísticos ni bien mantenidos, son más bien como áreas recreativas o verdes que son bosque de maleza. Lo que teníamos que hacer era cortar el exceso de arbustos o recoger ramas secas --fue un trabajo interesante. Siempre he encontrado placentero el aire libre. También tuve una ruta para repartir periódicos, además, en un momento dado --no eran periódicos, era correo basura. En realidad, no estaba muy interesado en trabajos de verano, me acabo de dar cuenta de eso. Pero los hice por esos días. En general, probablemente obtuve más dinero de las becas escolares.

En Finlandia, es común que la gente haga donaciones a las escuelas, incluso a las escuelas primarias públicas. Así, a partir de cuarto grado, el dinero es distribuido a los estudiantes de acuerdo a lo que la persona haya establecido en qué invertirse el fondo. Recuerdo que una de las donaciones en mi escuela fue para el niño más simpático de la clase. Esto fue en sexto grado y realmente votamos en clase para quién debería ganarse el dinero. Debo decir, que no fui yo quien ganó. El botín ascendió a sólo unos 200 marcos Finlandeses [3], que tal vez eran unos cuarenta dolares, en ese momento, pero me pareció una gran cantidad de dinero para dar a un alumno de sexto grado sólo por ser popular.

Muy a menudo el dinero se destinaba a la mejor persona en un tema o deporte en particular. Y muchos los premios eran por la escuela específica o financiados por el gobierno. En algunos casos, los fondos disminuían con el tiempo. Recuerdo una vez en que el fondo fue de alrededor de un penique [4]. Cuando esa era la situación, la escuela debió compartir gastos para hacerla un poco más amena, pero aún así era pequeña la suma de dinero; y más que otra cosa, esto fue una manera de mantener la tradición de dar dinero cada año. Finlandia toma en serio sus tradiciones académicas, lo que es una gran cosa.

También yo recibiría estas becas cada año por ser el chico de las matemáticas. En la secundaría los premios eran más jugosos. Los más grandes eran del orden de $500. Así que ahí es donde vino la mayor cantidad de dinero para mi segundo computador; mi pensión semanal no habría alcanzado para un computador. También pedí prestado algo de dinero a mi padre.

Era 1986 o 1987. Tendría dieciséis o diecisiete. Mis años de baloncesto estaban quedando atrás. Invertí una cantidad excesiva de tiempo investigando el campo antes de decidir qué computador comprar. Los PCs no eran muy buenos en ese tiempo, así que cuando fantaseaba con mi nuevo computador sabía que no iba a ser un PC.

Opté por un Sinclair QL, que muchos de ustedes probablemente son muy jóvenes para recordar. Aquí la historia. La Sinclair fue una de las primeras máquinas de 32-bits en el mercado de uso doméstico. Sir Clive Sinclair, el fundador de la compañía, fue el Steve Wozniak de Gran Bretaña. Él desarrolló estos “componentes” informáticos que fueron vendidos en Los Estados Unidos como computadores Timex. Es decir, la misma compañía que hacia los relojes Timex importaba la materia prima del computador Sinclair y lo vendía aquí con el nombre de Timex. Los primeros fueron vendidos como “componentes” antes de que él empezara la venta de computadores ya ensamblados.

![Sinclair QL](http://dl.dropbox.com/u/1331087/images/sinclair-ql-large.jpg “Sinclair QL”)

![Microdrive](http://dl.dropbox.com/u/1331087/images/214px-Microdrive_cart.png “Microdrive”)

El Sinclair tenía un sistema operativo denominado Q-DOS. Yo lo sabía con toda seguridad en ese momento. Fue especialmente escrito para ese computador en particular. Tenía un sistema base realmente avanzado para la época, y unos gráficos bastante buenos. Una de las cosas que me fascinaba del sistema operativo era la multitarea: podías ejecutar varios programas a la vez. Sin embargo, el sistema base no era multitarea, así que no podías ejecutar más que un programa base a la vez. Pero si escribías tus propios programas en lenguaje ensamblador, usted podía hacer que el sistema operativo los planificará [5] y les asignara su intervalo de ejecución, de esa manera podía ejecutar muchos programas al mismo tiempo.

El computador incorporaba el chip 68008 de 8-megahertz, que fue la segunda y más barata versión del chip 68000 de Motorola. Internamente, la primera generación de chips 68000 fueron de 32-bits, pero externamente tenían una interfaz de 16-bits para cualquier cosa fuera de la CPU [6] --como una memoria u otro componente hardware. Debido a que sólo podía cargar a la vez 16 bits de la memoria, las operaciones de 16 bits, muchas veces, eran más rápidas que las operaciones de 32-bits. La arquitectura fue muy popular y aún hoy existe en muchos dispositivos embebidos o en autos. No es el mismo chip, pero está basado en la misma arquitectura.

El chip 68008, la versión que tenía mi computador, usaba 8 bits, no 16 bits, para su interfaz con el mundo exterior a la CPU. Pero a pesar de que interactuaba externamente a 8 bits a la vez, internamente era de 32 bits. Eso hizo que fuera, de cierta manera, más agradable en la programación.

Tenía 128 kilobytes de memoria --no megabytes-- que era una cantidad enorme para una máquina casera de la época. Mi antigua VIC-20 sólo tenía 3½ kilobytes de memoria. Y puesto que era una máquina de 32-bits se podía acceder a toda la memoria sin ningún problema, lo que era algo inaudito en aquel entonces. Esa fue la principal razón por la que quise comprar dicho computador. La tecnología era interesante y adoraba la CPU.

Yo tenía la esperanza de hacerme con el descuento del computador al comprarlo en una tienda donde un amigo conocía a los propietarios; pero hubiera tomado mucho tiempo en llegar así que caminé decidido a Akademiska Bokhandeln, la librería más grande de Helsinki, donde había una sección de informática. Se los compré directamente del mostrador.

El computador costó cerca de $2.000. No solía ser la norma que el nivel de costo más bajo de los computadores era siempre de $2.000. Sólo hace un par de años esto ha cambiado. Ahora puedes comprarte un PC nuevo por $500. Es como los autos. Nadie fabrica autos por menos de $10.000. En algún momento, dejó de valer la pena. Desde luego, las compañías pueden fabricar un auto que se venda en $7.000, pero los fabricantes parten del hecho que las personas quienes se pueden permitir pagar $7.000 por un auto, son más felices comprando uno por $10.000 que tiene cosas extras, como el aire acondicionado, ya que hace parte del equipamiento estándar. Si comparamos el nivel de costos bajos de los autos de éste año con el nivel de los autos de hace quince años, cuestan casi lo mismo. De hecho, ajustando por la inflación deben costar un poco menos. Pero son mucho mejor.

Así es como solía ser con los computadores. Cuando los computadores no eran algo que todo mundo comprara, no había un umbral de dolor al pagar $2.000. Si el computador de menor costo es mucho más caro, no es posible para una compañía vender muchos equipos. Pero eran los suficientemente caros para los fabricantes que no tenia sentido para una compañía hacerlos más baratos. La gente siempre paga los $200 adicionales o más por una máquina mejor.

En los últimos dos años ya son menos costosos de fabricar. Incluso las máquinas de gama baja se han puesto a buen precio. Las compañías han perdido mucha de las personas que pagarían los $200 extras por una máquina un poco mejor. Dado que las compañías no pudieron vender los complementos por sí solos, tuvieron que incluirlos en el precio.

Lo admito: en ese entonces 1987, uno de los puntos de venta del QL fue aquel que se veía genial.

El computador era totalmente negro mate, con un teclado negro. Era rígido en su forma. No era una máquina con bordes redondeados ni mucho menos elegante. Parecía ser algo extremo. El teclado era como de una pulgada de grosor, ya que hacia parte de la misma unidad que el equipo. Esa era la forma como venían diseñados la mayoría de computadores caseros. Al lado derecho del teclado, en la que tendría un teclado numérico, tenías dos ranuras para el revolucionario micro-lector Sinclair, que era este interminable carrete de cinta que se usó sólo en la máquina Sinclair. Funcionaba y fue organizada como una unidad de disco. Debido a que era una cinta larga, sólo podías darle vueltas hasta que acertabas en lo que querías. Y al final resultó ser una mala idea, ya que no era tan fiable como una unidad de disco.

Así que invertí cerca de $2.000 en el Sinclair QL. El máximo uso que le di fue desarrollar proyectos de programación uno tras otro. Siempre estaba buscando algo interesante que hacer. Tuve un compilador y un interprete para el lenguaje Forth [7], sólo para probar. Forth fue un lenguaje extraño que ya nadie más usa. Era divertido, y ampliamente usado en el mercado de lenguajes de programación de los 80s para diferentes cosas, pero nunca llegó a ser popular, por lo difícil para personas no técnicas. En realidad era poco útil.

Yo mismo escribía mis herramientas de programación. Una de las primeras cosas que compré para la máquina fue una tarjeta de expansión para una EEPROM [8]. Es una memoria en la que escribes datos tu mismo usando módulos especiales, y permanecen allí cuando apagas el computador. De esa manera, podría tener disponibles fácilmente las herramientas en el momento que quisiera, sin tener que cargarlas en la RAM [9] y usar la preciada RAM para los programas.

Lo que me llevó a interesarme en los sistemas operativos: compré una unidad de disquete de tal manera que no tendría que usar los micro-lectores, pero el controlador que venía con la unidad de disquete era pésimo, así que terminé escribiendo uno propio. En el proceso de escribirlo encontré algunos errores en el sistema operativo --o al menos discrepancias entre lo que la documentación decía que debería hacer el sistema operativo y lo que estaba haciendo en ese momento. Los encontré porque algo que había escrito no funcionaba bien.

Mi código siempre es, ummm, perfecto. Así que sabía que tenía que ser algo más, me decidí, y desensamblé el sistema operativo.

Usted podría comprar libros que publican listados parciales del sistema operativo. Eso ayuda. También necesita un desensamblador, una herramienta que toma el lenguaje máquina y lo transforma en lenguaje ensamblador. Eso es importante porque cuando sólo tienes una versión en lenguaje máquina, es difícil seguir las instrucciones. Te encuentras con que una instrucción saltará a una dirección numérica, lo que hace que sea muy difícil de leer. Un buen desensamblador te colocará nombres en lugar de números y también te permitirá determinar algunos nombres. Además puede ser usado para ayudarte a identificar secuencias de instrucciones en particular. Tuve mi propio desensamblador que podía usar parar crear listados razonablemente buenos. Cuando algo no funcionaba, podía ir y decirle que listará un lugar en particular, y así podía ver todo lo que estaba por hacer el sistema operativo. Algunas veces usé el desensamblador no porque algo estuviera defectuoso sino porque estaba tratando de entender lo que se suponía que hacia.

Una de las cosas que odié del QL fue que tenía un sistema operativo de sólo lectura. No podías cambiar cosas. Se tenían unos “ganchos” [10] --lugares donde puedes insertar tu propio código para controlar ciertas funciones-- pero sólo en ciertos lugares. Es muchísimo mejor poder remplazar completamente tu sistema operativo. Hacer un sistema operativo en ROM [11] es una mala idea.

A pesar de que había dicho que Finlandia estaba en el top tecnológico, el Sinclair QL no estaba haciendo grandes incursiones en el séptimo país más grandes de Europa. Debido a que el mercado era tan pequeño, cada vez que querías comprar actualizaciones para ésta máquina de vanguardia e iconoclasta, tenias que pedirlas a Inglaterra, vía giro postal. Esto involucraba recorrer los catálogos hasta que encontraras a alguien quien venda lo que sea que estés buscando. Luego tenías que reunir los cheques certificados y esperar semanas por la entrega (esto cuando no existía Amazon.com ni las tarjetas de crédito). Eso fue lo que tuve que hacer cuando quise expandir mi RAM de 128-kilobytes a 640-kilobytes. Fue el mismo cuento cuando compré un nuevo ensamblador, para traducir el lenguaje ensamblador en lenguaje máquina (unos y ceros) [12], y un editor, que básicamente es un procesador de texto pero para programar.

Tanto el ensamblador como el editor funcionaban bien, pero estaban en los micro-lectores y no podían ser ejecutados desde la EEPROM. Por eso escribí mi propio ensamblador y editor y los usé para todas mis implementaciones. Ambos fueron escritos en lenguaje ensamblador, lo que es increíblemente estúpido para los avances actuales. Es complicado y lleva tiempo --Creería que toma cientos de veces más tiempo resolver un problema en lenguaje ensamblador que en lenguaje C, por ejemplo, el cual estaba disponible por la época.

Adicioné unos pocos comandos al interprete básico que venía con la máquina así que cuando quería editar algo sólo ejecutaba mi editor automáticamente y me llevaba instantáneamente allí. Mi editor era más rápido que aquel que venia con la máquina. Particularmente estaba orgulloso de cuan rápido podía escribir caracteres en la pantalla. Normalmente, con una máquina como esa, tomaría mucho tiempo llenar la pantalla con caracteres para que vieras moverse el texto. Y estaba contento con el hecho que con mi editor, escribías texto tan rápido que cuando te movías rápidamente hacia abajo dejabas una estela. Eso fue importante para mi. Las mejoras hechas a la máquina la dejaban mucho más ágil, y sabía que había hecho un montón de trabajo para hacerla funcionar de esa manera.

En éste momento, supe que no había mucha gente quienes estuvieran interesadas en los computadores de la forma que yo lo hacía. Existía un club de informática en mi colegio, pero no pasé mucho tiempo allí. Básicamente era un sitio para chicos que querían conocer sobre computadores. 250 estudiantes de toda la escuela conformaban el club, y no creo que alguien más haya estado usando uno desde los 10 años.

Una de las cosas que me gustaba mucho hacer en mi Sinclair QL era hacer clones de juegos. Escribí clones de los juegos del VIC-20 que me habían gustado y algunas veces incluí mejoras. Pero la mayoría no eran tan buenas: una mejor máquina, no un mejor concepto.

Probablemente mi juego favorito fue “Asteroids”, pero nunca pude hacer un buen clon de él. La razón es que, en la época, todos los juegos arcade de “Asteroids” [13] fueron hechos con gráficos vectoriales reales. En lugar de tener un gráfico basado en pequeños puntos --píxeles-- eran gráficos que se hacían con la ayuda de un tubo de rayos catódicos (CRT – cathode-ray tube), electrones disparados a través de un tubo detrás del CRT y desviados por imanes. De esa manera se obtienen gráficos de alta resolución, pero no podías reproducirlo fácilmente. Podías hacer un clon, pero no se parecería al “Asteroids” original si lo escribías en un computador que no tenía la capacidad gráfica necesaria.

Recuero hacer un clon de Pac Man en lenguaje ensamblador. El primer paso es tener en mente cuál es el aspecto esperado de los personajes de Pac Man. Luego tratas de dibujarlos aprovechando una cuadricula de dieciséis por dieciséis, a color. Y si eres artista, puedes hacer un buen trabajo. Pero si eres el Sr. No-Artista como yo, finalizará con aspecto del primo enfermo de Pac Man.

Esta bien, no era un clon muy bueno. Pero estuve muy orgulloso de ello. Se podía jugarlo, y lo envíe a una de las revistas que publicaban código informático. Había vendido otros programas a revistas y pensé que esto sería algo normal.

No.

Uno de los problemas fue que el programa había sido escrito en lenguaje ensamblador. Eso significaba que si cometías un descuido, un pequeño error copiándolo de la revista, el código no funcionaría.

También escribí algunos juegos propios. Pero requería cierta destreza mental para crearlos. Debido a que los juegos requieren un gran rendimiento, realmente tienes que acercarte al hardware del computador. Yo podía hacer eso, pero no tenía la mentalidad de planear un juego completo. Lo que hace a un gran juego no es qué tan rápido sea o qué tan buenos son los gráficos. Tiene algo más que te anima a jugarlo --algo que te mantiene inmerso en él. Es como las películas. Los efectos especiales son una cosa pero también necesita un buen argumento. Y mis juegos nunca tenían un argumento. Un juego debe tener un movimiento progresivo, una idea. Muchas veces, ésta progresión es sólo que el juego sea más rápido. Eso es lo que hace Pac Man. A veces cambia el laberinto o los monstruos mejoran al seguirte.

Lo que me interesaba de Pac Man era afrontar el problema de hacer que los gráficos no parpadearan. Es un problema muy común en los videojuegos más viejos, ya que sin hardware especial tus personajes sólo parpadean. La forma como mueves tus personajes en la pantalla es quitar una copia vieja y dibujar la nueva copia. Si ocurre que tienes una mala temporización, las personas pueden ver cuando no hay copia, es decir, parpadea. Esto se supera de muchas maneras. Puedes dibujar primero el nuevo personaje y luego quitar el viejo, pero debes tener cuidado de no quitar la parte del viejo personaje que coincide con el nuevo. En lugar de ver el irritante parpadeo, ahora obtienes un buen efecto --a veces ves la sombra del viejo personaje en la pantalla. Ya no es parpadeo, pero crea el efecto de dejar una estela (motion blur [14]). El problema con ésta solución es que es muy costosa en memoria y tiempo.

Hay una razón por la que los videojuegos están siempre a la vanguardia, y es que muchas veces son los primeros tipos de programas que crean los programadores. Particularmente tiene que ver con el hecho que algunos de los programadores más listos del mundo son chicos de quince años jugando en sus computadores (Es lo que pensé hace dieciséis años, y creo que aún es verdad). Pero hay otra razón por la que los juegos son pioneros: los Juegos piden hardware.

Si observas los computadores de hoy, son suficientemente rápidos para cualquier cosa. Pero el terreno donde pruebas los limites del hardware son acciones de videojuegos, como algunos de 3-D que ahora son tan populares. Fundamentalmente, los videojuegos son una de las pocas cosas en computación donde puedes decir si las cosas no están sucediendo en tiempo real. En procesadores de texto, no te importa el retraso de un segundo aquí o un segundo allí. Pero en un videojuego, empieza a ser notable cerca de la décima de segundo. Los videojuegos solían ser bastantes simples. Hoy día, la programación es una parte pequeña de cualquier videojuego. Hay música, hay argumento. Si lo comparas con hacer una película, el componente de la programación es sólo el trabajo de cámara.

Tuve la Sinclair QL durante tres años. Me acompaño desde el colegio a la Universidad de Helsinki y al Ejercito Finlandés [15]. Estuvo bien, pero estábamos listos para partir caminos. Más o menos en el último año descubrí su limitación. La 68008 fue una buena CPU, pero estaba leyendo acerca de la siguiente generación 68020, y aprendiendo sobre ciertas características como la administración y paginación de memoria. Estos nuevos computadores podían hacer cosas que son muy significativas cuando estas trabajando a bajo nivel.

Lo que me incomodaba de la Sinclair QL era que mientras el sistema operativo era capaz de realizar multitarea, aún podías hacer fallar el sistema en cualquier momento ya que no había protección de memoria. Una tarea que decidí hacer mal, pudo bloquear el equipo.

El Sinclair QL fue la última incursión de Sir Clive Sinclair en el diseño y fabricación de computadores. Una de la razones: no fue comercialmente exitoso. Tuvo una tecnología interesante, pero la compañía tenía problemas de producción y problemas de aseguramiento de la calidad y la inevitable mala prensa. Además, el mercado empezó a ser más competitivo.

La decada de los 80s fueron los años donde podías empezar a imaginar que, sí, tal vez algún día podrías tener tu propio computador, aunque sólo fuera para ejecutar un procesador de texto. Y todas las señales apuntan al PC. Sí, el original PC de IBM ha iniciado la inundación de los estantes y se ha convertido en éxito a pesar de numerosas limitaciones técnicas. Estas criaturas de color beige que estaban por todas partes tenían el sello de aprobación de IBM, después de todo, eso tenía un gran significado. Otro de los atractivos: los periféricos eran estandarizados y fáciles de conseguir.

Estuve leyendo sobre todas estas CPUs que podían hacer lo que yo quería. Era claro que el 68020, que parecía interesante, no iba más. Podía haber considerado comprar una CPU de actualización para la QL. En aquellos días eso significaba básicamente la reconstrucción de la máquina. De todas maneras, el sistema operativo no sabía de administración de memoria, así que yo habría tenido que escribir mi propia versión. Así fue como pensé: Hhhmmm. Hacer eso será un gran paso. Y va a ser costoso conseguir una nueva CPU.

Y luego estaba todavía el dolor de cabeza cada vez mayor de construir cosas para el equipo. No era como si hubiera un catálogo de Sears para el Sinclair QL y sólo era coger el teléfono y pedir más memoria. La rutina de giro-postal-de-Inglaterra estaba haciéndose aburrida (No me importaba que no hubiera ningún software empaquetado porque era capaz de escribirlo todo yo mismo).

Hubo un efecto secundario positivo de todo esto. Cuando estaba pensando en deshacerme de la máquina, decido vender mis periféricos --la unidad de disco duro real que había comprado porque no podía aguantar un segundo más el micro-lector, y mi RAM de expansión. Pero no había gente haciendo cola en las calles en busca de esas cosas, así que tenías que hacer publicidad en una revista de informática y orar. Y así fue como conocí a mi buen amigo Jouku Vierumaki [16], que resultó ser probablemente la otra persona en toda Finlandia que era dueño de un Sinclair QL. Él contestó mi anuncio y cogió el tren desde Lahti y compró algunos de mis periféricos. Luego me indujo a jugar billar.


----

[1] Leo Waldemar Törnqvist , abuelo materno y profesor de estadística en la Universidad de Helsinki

[2] Helsinki, Finlandia

[3] [Marco Finlandés](http://es.wikipedia.org/wiki/Marco_finland%C3%A9s)  = Finnmarks =  Finnish Mark = Markka: unidad monetaria de Finlandia que existió hasta el año 2002.

[4] penique = un centavo: Un marco finlandés se dividía en 100 peniques

[5] [http://es.wikipedia.org/wiki/Planificador](http://es.wikipedia.org/wiki/Planificador)

[6] CPU = Central Processing Unit = Unidad de Procesamiento Central

[7] [http://es.wikipedia.org/wiki/Forth](http://es.wikipedia.org/wiki/Forth)

[8] EEPROM = Electrically Erasable and Programmable Read Only Memory = Memoria de Solo Lectura Programable y Borrable Eléctricamente

[9] RAM = Random Access Memory = Memoria de Acceso Aleatorio

[10] [Hooking](http://en.wikipedia.org/wiki/Hooking) (enganchar) cubre una serie de técnicas usadas para modificar o mejorar el comportamiento de un sistema operativo, aplicaciones u otros componentes de software a través da las interceptaciones de llamados de funciones, mensajes o eventos pasados entre componentes de software. El código que manipula tales llamados de funciones, mensajes o los eventos interceptados se denomina "hook" (gancho).

[11] ROM = Read Only Memory = Memoria de Solo Lectura

[12] Ensamblador (assembler) hace referencia al programa que se encarga de traducir el lenguaje ensamblador (assembly language). El ensamblador es lo que hoy se conoce como compilador.

[13] [Arcade](http://es.wikipedia.org/wiki/Arcade) es el término genérico de las máquinas recreativas de videojuegos disponibles en lugares públicos de diversión.

[14] [Motion blur](http://es.wikipedia.org/wiki/Motion_blur) o desenfoque de movimiento es el desenfoque o borrosidad que se produce en la imagen por el movimiento a gran velocidad de los objetos.

[15] En secciones anteriores del libro, Linus cuenta su paso por el servicio militar obligatorio de Finlandia, después de estar un año en la Universidad.

[16] Jouku “Avuton” Vierumaki, en un aparte del libro menciona como Linus le muestra lo que estaba desarrollando: “Estaba impresionado cuando Linus se acerca y presiona una combinación de teclas e inmediatamente aparece una terminal independiente y donde puede acceder un usuario diferente, en ese momento me di cuenta que él había creado algo genial”

*Traducción libre por Edwin Caldon*
