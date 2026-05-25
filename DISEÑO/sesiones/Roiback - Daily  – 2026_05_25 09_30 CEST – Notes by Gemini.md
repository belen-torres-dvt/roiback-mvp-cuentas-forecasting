may 25, 2026

## Roiback \- Daily  \- Transcripción

### 00:00:00

**Belen Torres:** A ver, este. Vale, vale. Eh, bueno, esto lo tenéis también el documento este de preguntas que hay en vuestro Sharepen. Vale, hay algunas preguntas que si no se pueden responder no pasa nada,

**Otelo Pons:** Hm.

**Ana Martín:** Mhm.

**Belen Torres:** lo intentamos analizar de otra forma o incluso lo ponemos en ya se definirá más adelante, así que no pasa nada. Vale, la primera sería eh tema de volumetría de datos, ¿vale? Esto sé que la tabla, bueno, esta es la tabla de eh las tabla de dimensiones, que sería la de account y la de property que sé si son. Me imagino que esa volumetría de datos no va a variar mucho de aquí a pocos años, pero imagino que la de Google Analytics,

**Otelo Pons:** Mhm.

**Belen Torres:** por ejemplo, sí que va a haber bastantes cambios con eso. Entonces, eh creo que ahora mismo probablemente no sepas contestarme a esa pregunta. Igualmente creo que seguimos teniendo permiso al de al de Analytics. Puedo hacer ahí un análisis para saber qué volumetría y luego

**Otelo Pons:** Correcto.

**Belen Torres:** el de bookings. Ese sí que no tenemos permiso. No sé si eso de alguna forma me lo me lo pueden mirar o incluso con alguna query para

### 00:01:13

**Otelo Pons:** Bueno,

**Belen Torres:** que Sí.

**Otelo Pons:** basta basta con hacer una query de las reservas quean cada año y ya está.

**Belen Torres:** una query.

**Otelo Pons:** y y

**Belen Torres:** Vale,

**Otelo Pons:** desacrejimiento.

**Belen Torres:** sí, lo hago yo. Digo, era por si lo tenían más a mano, si sabías, pero bueno, me encargo yo ha algún aqui o lo que sea y ya saco yo la

**Otelo Pons:** O sea,

**Belen Torres:** volimetría.

**Otelo Pons:** sé que se hacen unos 8 9000 movimientos cada día porque me lo miro cada

**Belen Torres:** Eso de bookings.

**Otelo Pons:** día. Sí.

**Belen Torres:** Wow,

**Otelo Pons:** O sea,

**Belen Torres:** qué pasada.

**Otelo Pons:** no que sean 8000 reservas cada día,

**Belen Torres:** Sí, con los movimientos.

**Otelo Pons:** se hacen entre 8 y 9000 movimientos de reservas cada día.

**Belen Torres:** Sí, sí. O ya sea de cancelación o de modificación de la reserva o de eh nuevo nueva reserva de

**Otelo Pons:** Correcto.

**Belen Torres:** algo. Vale, ahora nuestro proceso, el que se va a implementar, ¿cuándo os interesaría que se vaya actualizando? ¿Os interesaría que, por ejemplo, empecemos una vez al día cada 24 horas?

### 00:02:05

**Belen Torres:** O sea, hay que tener en cuenta también cuándo se actualiza vuestros procesos. Entonces, si por ejemplo la tabla de bookings eh está actualizada, o sea, bueno, no sé, no sé cómo cómo es esa actualización que tenéis vosotros ahora

**Otelo Pons:** Depende.

**Belen Torres:** mismo,

**Otelo Pons:** Nosotros trabajamos con actualizaciones diarias más que nada para que

**Belen Torres:** ¿vale?

**Otelo Pons:** esté todo más o menos sincronizado. Es decir, todo lo que viene en Analytics nos lo manda Google y nos lo manda con un par de días de decalaje, o sea, ni siquiera es ni siquiera es diario. Los bookings los cogemos cada los cogemos cada hora, pero todos los procesos solo los lanzamos una vez al día. Por eso,

**Belen Torres:** Vale.

**Otelo Pons:** para que tenga esté más o menos sincronizado con el gesto

**Belen Torres:** Y y ¿a qué hora lo hacéis vosotros?

**Otelo Pons:** de

**Belen Torres:** lo hacéis por la noche o algo, más que nada para hacerlo rollo justo después, ¿sabes? O sea, que esté sincronizado todos los procesos.

**Otelo Pons:** te lo tendría que mirar. O sea, al final, o sea, al final por la mañana primera hora es cuando,

**Belen Torres:** Vale,

**Otelo Pons:** o sea, a las 8:30 o sí ya está todo.

### 00:03:20

**Belen Torres:** a las 8:30 lo tenéis todo, ¿vale?

**Otelo Pons:** Sí. Lo a las 8:30 lo damos todo por actualizado hasta día de vale

**Belen Torres:** Vale.

**Otelo Pons:** lo que no quita que se hagan más actualizaciones durante el día.

**Daniel ACOSTA:** Otelo, ¿te puedo preguntar por qué es tan tarde?

**Otelo Pons:** Vale,

**Daniel ACOSTA:** Porque normalmente los procesos nocturnos se hacen mucho antes, en plan a las 4 o 5 de la mañana.

**Otelo Pons:** por el tema de horarios, porque a las 4 o 5 de la mañana y nap y tal no no han terminado. Bueno, no, ahí sí que no. Exacto. No han terminado el día en Latan,

**Ana Martín:** en lata

**Otelo Pons:** perdona.

**Daniel ACOSTA:** Claro.

**Belen Torres:** Vale,

**Ana Martín:** y se pueden hacer varios procesos o no vale la pena

**Belen Torres:** vale.

**Ana Martín:** no pasearlo.

**Belen Torres:** En varias ejecuciones te refiere.

**Otelo Pons:** Sí, pero como está como Sí,

**Belen Torres:** Sí.

**Otelo Pons:** o sea, podríamos hacerlo ahora para esto. ¿Correcto? Por eso,

**Ana Martín:** No, claro,

**Otelo Pons:** o sea,

**Ana Martín:** yo digo ahora plantearlo ahora sí por los temas de los horarios de cada región.

**Otelo Pons:** las reservas las las cogemos cada hora,

### 00:04:30

**Ana Martín:** Yeah.

**Otelo Pons:** pero como hasta ahora todo iba por click y tal y en click sí que solo lo cargamos una vez al día, por el tema es de que si no se para todo y tal, pues pues lo hacíamos así, pero ya te digo, las reservas las tenemos cada uno y podríamos incluso incrementar

**Daniel ACOSTA:** Claro, a ver, cortar cortarte todo el mundo no te va a cortar porque ahora mismo son las 12:30 en California, que es GMT \-8, creo que bueno GMT \-7, hay un GMT \-8, o sea,

**Juan Ezquerro:** A

**Daniel ACOSTA:** que a las 8:30 de la mañana son las 11 y pico,

**Juan Ezquerro:** ver.

**Daniel ACOSTA:** si llega una cancelación a esa hora te la comes. O sea, que cortarte todo el mundo en una sola hora es muy complicado.

**Otelo Pons:** Ya,

**Daniel ACOSTA:** Lo

**Otelo Pons:** ya, ya, ya, Por eso,

**Daniel ACOSTA:** plantear

**Otelo Pons:** por eso fue una una decisión de decir, pues vamos a cortar aquí y el trading diario es hasta aquí.

**Daniel ACOSTA:** Claro, claro. Hombre,

**Otelo Pons:** Punto.

**Daniel ACOSTA:** la el problema es si haces dos cortes vas a tener números que se mueven durante el día.

**Otelo Pons:** ¿Correcto? Cuantos más cortes hagas, más discrepancias habrá entre unas cosas y otras.

### 00:05:42

**Daniel ACOSTA:** tiene más

**Otelo Pons:** Por eso decidimos hacer solo uno a esta hora que entraba todo,

**Daniel ACOSTA:** comp.

**Otelo Pons:** que entraba todo más o menos ya de de de APAC entra de

**Daniel ACOSTA:** Claro,

**Otelo Pons:** más,

**Daniel ACOSTA:** claro.

**Otelo Pons:** ¿vale? Pero como no significaba nada hasta ahora muy poco,

**Daniel ACOSTA:** Y después, claro. Y una pregunta, ¿y después? O sea,

**Otelo Pons:** pues

**Daniel ACOSTA:** y cuando pasa el día siguiente, después se hace el settlement de de ese día que está todavía que queda un fleco o no se toca ese día ya. O sea, tú haces más un y el menos2 lo actualizas o solo actualizas el

**Otelo Pons:** no se apica todo porque Es que en cada momento te pueden llenar modificaciones

**Daniel ACOSTA:** solo.

**Otelo Pons:** de reservas de hace un mes, o sea,

**Belen Torres:** Claro, o sea,

**Daniel ACOSTA:** Claro.

**Belen Torres:** cogéis la cogéis a lo mejor la última fecha cargada,

**Otelo Pons:** ya no del día todas las

**Belen Torres:** ¿no? O sea, la última fecha que tenéis en la

**Otelo Pons:** modificaciones que se hayan hecho en una oía.

**Daniel ACOSTA:** Modificaciones. Claro.

**Belen Torres:** Vale.

**Daniel ACOSTA:** y las modificaciones vas hacia atrás y actualiza el setmen hacia atrás, ¿no?

### 00:06:50

**Otelo Pons:** Correcto.

**Daniel ACOSTA:** Vale,

**Otelo Pons:** Y puede ser que modifique reserv

**Belen Torres:** Vale, entonces os parece perdona.

**Otelo Pons:** incluso,

**Daniel ACOSTA:** vale.

**Otelo Pons:** perdón,

**Belen Torres:** No,

**Otelo Pons:** incluso de analytic aunque no seamos nosotros, a veces nos vienen cambios de hace tiempo y eso que es Google y se supone que y

**Daniel ACOSTA:** No,

**Belen Torres:** adelante.

**Daniel ACOSTA:** no,

**Otelo Pons:** se supone que los eventos no cambian.

**Daniel ACOSTA:** claro.

**Otelo Pons:** Un clic que has hecho, has hecho ese click, no lo puedes modificar,

**Daniel ACOSTA:** Bueno, bueno, bueno,

**Otelo Pons:** pero hay cambios.

**Daniel ACOSTA:** pero si el cliente si el cliente pide que se elimine los datos a a Google, Google se los

**Otelo Pons:** Bueno,

**Daniel ACOSTA:** carga.

**Otelo Pons:** no lo sé. Google hace lo que le da la gana y a veces incluso cambia los campos y

**Daniel ACOSTA:** Sí, sí, sí, sí, sí, sí.

**Otelo Pons:** sinalizar.

**Daniel ACOSTA:** Este fin de estaba hablando yo con un con un un amigo mío que es ingeniero de Google aquí en Málaga y me ha contado

**Belen Torres:** Sí.

**Daniel ACOSTA:** que su máximo problema, él es experto en base de datos, es la eliminación de datos a pasado, porque claro, hay base de datos que ya está encistada, ya estás en el iceberg, ya está archivada y claro, modificar esos archivos y la Unión Europea cada vez tira la ventana de Windows más hacia atrás.

### 00:07:54

**Daniel ACOSTA:** Había al principio eran como 6 meses, pero es que ya puedes eliminar el histórico de 2 años y es un es un challenge para muchas

**Otelo Pons:** Sí,

**Daniel ACOSTA:** empresas y un

**Otelo Pons:** sí. Es es un dolor de cabeza.

**Daniel ACOSTA:** coste también porque modificar ahora tablas de hace un año, ¿sabes?

**Belen Torres:** Eh, vale. Entonces, si a las 8:30 ya esa tabla eh no se vuelve a actualizar hasta ya al día siguiente, ¿no? O sea, esa tabla ya a las

**Otelo Pons:** No, la la de bookings cada Bueno,

**Belen Torres:** 8:30

**Otelo Pons:** sí, correcto. La de bookings se actualiza cada hora.

**Belen Torres:** la de bookings cada hora.

**Otelo Pons:** Vale.

**Belen Torres:** Vale, eso es

**Otelo Pons:** Sí. Lo que pasa es que nosotros las que las que cogemos a partir de ahí ya

**Belen Torres:** importante.

**Otelo Pons:** ya no las modificamos hasta el día segundo de todos los dibors y tal y pues ya

**Belen Torres:** Vale, o sea, espera,

**Otelo Pons:** no

**Belen Torres:** o sea, en cada una cada una entonces tiene un proceso, una hora de actualización diferente,

**Otelo Pons:** ehm

**Belen Torres:** ¿no? Vale, vamos a empezar por la de booking, que es la más importante.

### 00:08:56

**Belen Torres:** de booking se actualiza cada hora, pero la tabla como tal cada hora se actualiza,

**Otelo Pons:** sí

**Belen Torres:** ¿vale? La tabla de de data warehouse, ¿vale? El resto de tablas, las de Analytics

**Otelo Pons:** eh las de análisis y no creo o sea, creo que son dos veces, creo que lo pusimos ya dos veces al día, pero se actualiza según los datos que nos haya mandado Google, es decir, cada dos veces al día se pasan los procesos de recoger la información de todo. todas las cuentas. Puede ser que Google nos ha de mandado información.

**Belen Torres:** Vale, puede ser que no. Vale,

**Otelo Pons:** Puede

**Belen Torres:** ejecución dos veces. Vale. Eh, y ahora las que vienen de Salesford.

**Otelo Pons:** esa es cada día, pero no sé.

**Belen Torres:** Vale, vale. Y creo que no hay más. Bueno, luego está el la de la de

**Otelo Pons:** Si los maestros y tal que son son a porque vienen de y tal,

**Belen Torres:** Mo.

**Otelo Pons:** pues si se dicen pues pues lo cargo y ya está.

**Belen Torres:** Vale, vale. ¿Y cuándo os interesaría a vosotros que estuviera la tabla

**Otelo Pons:** Pues

**Belen Torres:** superactualizada? O sea, la tabla que vaya a utilizar el modelo, esa tabla tiene que estar refrescada también al igual que Bookings cada hora.

### 00:10:20

**Belen Torres:** O interesaría que a lo mejor pusiéramos una latencia de dos, tres, cu horas.

**Otelo Pons:** hombre, cuanto más fresco estuviese mejor,

**Belen Torres:** Cuanto más fresco, mejor.

**Otelo Pons:** pero como todo es unidor porque si luego tienes que cada, si yo te digo no, cada minuto, cada 10 minutos y tienes que lanzar todos los algoritmos que hagan o lo que sea de la información

**Belen Torres:** H

**Otelo Pons:** cada 10 minutos, pues posiblemente no vay coste de

**Belen Torres:** lo suyo sería depender un poco de cuándo se actualiza la de booking,

**Otelo Pons:** esto.

**Belen Torres:** ¿no? O sea,

**Juan Ezquerro:** Ah.

**Belen Torres:** si esa es cada hora intentar hacerlo

**Otelo Pons:** Y ya te digo tenemos cada hora porque sí podría ser 10 minutos o lo que sea,

**Belen Torres:** pues

**Otelo Pons:** lo que dependiendo de lo que necesitemos ahora, o sea, hasta ahora ni siquiera lo usamos lo de cada ahora, ¿vale? Porque siempre vamos a hasta hasta ayer,

**Belen Torres:** hm

**Otelo Pons:** ¿vale? Lo que te decía,

**Belen Torres:** M.

**Otelo Pons:** claro, para lo que nos aplica ahora lo cuanto más fresco mejor, pero es que yo yo lo lo separaría según los casos de uso. Es decir, para una alarma, yo que sé, para el tema de alarmas que que te esté mirando si te está

### 00:11:34

**Belen Torres:** Hm.

**Otelo Pons:** cayendo que se la de pues posiblemente no hace falta que se mire cada minuto o cada 10 minutos que te está cayendo la ide Bueno,

**Belen Torres:** H

**Otelo Pons:** no iba a decir el tráfico sí, pero es que el tráfico depende de lo que te mande Google y como Google tienes un par de días de decalaje, pues h ahí con mucha frecuencia que es vas a

**Belen Torres:** Ya, pero o sea, lo que me quieres decir con que con que una vez,

**Otelo Pons:** tenerado.

**Belen Torres:** o sea, con que os traéis los datos del día anterior, eso es porque ahora mismo vuestro proceso de, o sea, me quieres decir que tu proceso ahora de reservas te trae la información. O sea, es que eso lo quiero entender bien.

**Otelo Pons:** No,

**Belen Torres:** O sea, la tabla la tabla de data warehouse de Booking me dice que cada hora se actualiza.

**Otelo Pons:** sí.

**Belen Torres:** ¿Y qué es qué proceso es el que tenéis que coge la información del día de ayer?

**Otelo Pons:** No, no, no. No es que sea un proceso que coge el día de ayer, sino que todos los dashboards y todo lo que está a partir de la tabla de bookings solo

**Belen Torres:** Vale, vale, vale,

**Otelo Pons:** contamos hasta la fecha de ayer,

**Belen Torres:** vale, vale, vale.

### 00:12:44

**Ana Martín:** Es que claro, yo creo que es un poco,

**Otelo Pons:** ¿vale?

**Ana Martín:** si lo entiendo bien, al final es como dice Otelo, quizá para las alarmas no hace falta tener el dato super preciso, pero en los dashboard sí que sería muy interesante poderlo tener actualizado a pesar de que los das ahora estén enfocados a la parte de alarmas,

**Otelo Pons:** Claro.

**Ana Martín:** pero al final si vamos a llevar hacia allí a la ente lo van a utilizar en el día a día y si pudiésemos tener el dato pues de lo que está sucediendo durante el día de hoy, pues aporta valor, que ahora es verdad que estamos limitados hasta ayer.

**Otelo Pons:** Pero eso, o sea, lanzar los algoritmos de producción y de todo esto cada hora,

**Ana Martín:** No, esto no cre

**Otelo Pons:** pues creo que no tiene ninguno para tener los datos frescos para, yo que sé, las consultas que se puedan hacer desde la gente o talent

**Belen Torres:** Vale,

**Otelo Pons:** mejor.

**Belen Torres:** o sea, que sí que tendría sentido el dashbo al tenerlo actualizado para que lo vaya a ver que de hecho, o sea, si por ejemplo lo actualizáis cada hora, eh, no podemos ponerlo a la misma hora porque si no te va a coger la actualización de, o sea, hay que ponerlo como un poquito más tarde siempre, que eso ya lo

**Otelo Pons:** Bueno, ya veníamos a ver cómo podemos enganchar una cosa con la otra.

### 00:13:55

**Belen Torres:** Bueno, y luego la alarma, o sea, el tema de la la los procesos de alarma de de modelado y tal, eso eh tendría sentido a lo mejor hacerlo No sé, dos veces al día o tres.

**Otelo Pons:** No sé cómo la discotecación.

**Belen Torres:** Pues es que depende, o sea, cuándo, por ejemplo, soléis, Claro, es que no hay un a lo mejor una un intervalo temporal en el que tengáis más anomalías que otras, ¿no? Es que puede ser en cualquier momento del día, que tampoco digo, a lo mejor si por ejemplo por la mañana es cuando más anomalías puede haber, pues a lo mejor ponerlas varias veces por la mañana o pues es que no lo sé. A ver, incluso podemos empezar primero poniendo dos veces y si veis que es mejor añadir más horas de ejecución, pues podemos poner más horas sin problema.

**Otelo Pons:** Pues más, pero yo creo que no es necesario tener más.

**Belen Torres:** Lo ponemos

**Otelo Pons:** Es que todo depende. Imagínate, o sea,

**Belen Torres:** M.

**Otelo Pons:** no no hemos dicho qué alarmas habría o o los casos de uso bien definidos, pero imagínate que quieres monitorizar, por ejemplo, a la las reservas que te van entrando por por para ver un posible problema de que se te haya caído la luz, por ejemplo.

### 00:15:39

**Otelo Pons:** Pues entonces házmelo cada 10 minutos de eso. Si si resulta que que lo que te decía que llevo al

**Belen Torres:** H

**Otelo Pons:** día pues 8 o 9000 modificaciones y y a esta hora debería llevar 3000 y llevo 100, pues entonces hay un problema. ¿Sabes? En este caso sí que necesitas que sea live live lo más lo más fresco posible, pero para todo el resto de indicadores y tal,

**Belen Torres:** Ya,

**Otelo Pons:** lo que te varíe eh eh el o lo que sea durante el día es que

**Belen Torres:** ya es

**Otelo Pons:** no tiene sentido.

**Belen Torres:** verdad.

**Otelo Pons:** Tendría sentido si pudiésemos tener el tráfico, por ejemplo, en streaming y decir,

**Belen Torres:** Sí.

**Otelo Pons:** "Ostras, no, es que ahora estoy teniendo un problema en esta web de tráfico y tal, pero es que como no es el

**Belen Torres:** Vale, pues si os parece eh lo incluso al principio a lo mejor lo podemos dejar una vez al día y luego ya si nos ponemos dos o y ya está. Una y dos. Vale. ¿Qué más por aquí? Vale. Eh, esta, vale, esta realmente también es hacer lo, o sea, llegar a un acuerdo también entre los dos.

### 00:17:03

**Belen Torres:** O sea, esto es por si a lo mejor falla, o sea, esto más que nada simplemente un orquestador, pero en principio vamos a utilizar el orquestador que tiene propio data formáis tener un proceso de tele totalmente automatizado de desde la ingesta hasta la visualización del dato. Entonces, bueno, como en principio vamos a utilizar Datform, eh, sería eso. Si hay algún error de código, lo vais a ver rápido y lo vais a poder resolver y volver a ejecutar. Entonces,

**Otelo Pons:** Ahí sí, ahí sí que bueno,

**Belen Torres:** tampoco

**Otelo Pons:** entiendo que vosotros ya tenéis super controlado, pero que todas las cargas y tal deberían ser importantes, ¿vale?

**Belen Torres:** eh sí,

**Otelo Pons:** Porque si no,

**Belen Torres:** sí,

**Otelo Pons:** o sea, las tenemos que poder lanzar en cualquier momento y y que y que y que el resultado sea el mismo,

**Belen Torres:** sí. H,

**Otelo Pons:** Ok.

**Belen Torres:** vale, vale. Y luego ya por aquí abajo tenía otra esta que sería la, bueno, la de la de clastering y partición, que esto porfa, si puede a lo mejor acceder aquí y escribirlo aquí en esta pestaña o si no directamente escribirlo en el chat. Esto era lo de qué campos son los que utilizáis para clusterizar y particionar,

### 00:18:18

**Otelo Pons:** para participar.

**Belen Torres:** ¿vale? de todas las tablas que tengas cruzadas y particionadas, ¿vale? O sea, si puede darnos esa información ya por donde si quieres subir un cheat nuevo con esa información, ¿vale? Por la parte de arquitectura ya estaría y ya quedaría la de observabilidad de costes.

**Otelo Pons:** O sea, como general y te digo que las que tienen fechas y y y cadenas, que son todas, ah, pues está participado por fecha la la de Bookings está participada por fecha de última

**Belen Torres:** Hm.

**Otelo Pons:** actualización, que es el modification. Te hablo de memorial, pero es es la fecha de

**Belen Torres:** Modificación.

**Otelo Pons:** últimación y

**Belen Torres:** yizad todas por cadena, entonces.

**Otelo Pons:** customizada por cin particionada por día y dentro de cada partición ordenada por y la de eventos igual está

**Belen Torres:** Vale, igualmente eh están

**Otelo Pons:** por fecha de evento particionada y y luego por

**Belen Torres:** vale las dos, ¿no? Imagino.

**Otelo Pons:** Sí. Y y el que son las tablas del de

**Belen Torres:** Y la y el resto de las de

**Otelo Pons:** Mateo,

**Belen Torres:** Selford.

**Otelo Pons:** ¿vale?

**Belen Torres:** Esas no están ni cruerizadas tampoco. Vale.

### 00:19:42

**Belen Torres:** Sí, porque ficha ha visto que no tienen. Digo, pero a lo mejor tienes alguna clusterización puesta.

**Otelo Pons:** No son tan pequeñas que sería

**Belen Torres:** Vale, pues lo voy a poner en hecho. Vale, vale. Ahora vamos a pasar con la parte de observabilidad de costes. ¿Vale? Eh, la primera pregunta que sería esta, esto es para tener un poco en cuenta el tema del presupuesto. Uy, perdón, espérate que se me ha puesto en grande la esto. Más que nada por si queréis que implementemos algún tipo de presupuesto mensual rollo, ¿vale? Pues teniendo en cuenta de que al final es un proyecto en el que vamos a meter inteligencia artificial, chatb y tal de que no queráis, mira, pues que no queremos gastar más de 1000 € por ejemplo, ¿no? O sea, para poner ese tope. Luego aparte también es importante porque tenéis e las tablas de Google Analytics que son bastante tochas, que hablamos de teras de datos también para saber si queréis poner algo, eso, algún tipo de límite,

**Otelo Pons:** H

**Belen Torres:** eh, o si, por ejemplo, ocurre que llegáis al tope, ¿qué habría que hacer? A lo mejor simplemente un aviso y y ya está.

### 00:20:43

**Belen Torres:** Oye, mira, pues habéis superado los 500 € que teníais de presupuesto, ¿sabes? O cosas así. Entonces, eso no sé si queréis hablarlo y lo hablamos mañana, por ejemplo, o si ya lo tenéis medio claro, pues lo apuntamos

**Otelo Pons:** No,

**Belen Torres:** yo.

**Otelo Pons:** la verdad es que no no tenemos porque tampoco sabemos qué vamos a enchufar ahí,

**Belen Torres:** Ya,

**Otelo Pons:** ¿sabes?

**Belen Torres:** hombre, es que te, o sea, más que nada esto es por tener un control, ¿sabes?

**Otelo Pons:** Claro, claro. Hay que ponerlo.

**Belen Torres:** Porque sí.

**Otelo Pons:** Sí, obviamente hay que ponerlo. ¿Cuál? Pues no sé, depende de qué que vayamos a enchufar ahí

**Belen Torres:** Ya queréis que os lo escriba en por el chat para que luego lo habléis y tal. Vale, voy a poner aquí RB,

**Otelo Pons:** Himo.

**Belen Torres:** ¿vale? Y luego por aquí hay algunas respuestas que sí que he puesto que conforme vayamos trabajando lo añadamos. por ejemplo, esta de añadir alguna etiqueta para eh pues no sé, depende de si se implementa algún servicio pues o datafone tal. Luego cuando estás en el billing sí que puedes hacer filtros.

### 00:21:46

**Belen Torres:** Entonces bueno, solo he puesto que ya lo definiremos, pero que se va a implementar.

**Otelo Pons:** Mhm.

**Belen Torres:** Y luego también estos límite de gastos, pues al final tendremos un entorno de desarrollo que será en el que hagamos prueba, luego tendremos el de producción. También hay que ver los límites de cada uno, que a lo mejor en ambos pues ponéis el mismo límite, ¿vale? Entonces, bueno, luego os escribo esas preguntas y ya está. Esta que también eh qué regiones se van a utilizar, que en este caso son eh Multirregión y Europe West 1 para los modelos que que dijimos que era muchísimo mejor esta región para para los modelos y luego la disponibilidad de cuota en cada una. Esto ya lo veremos. En principio creo que no hace falta que miréis por aquí vosotros nada, ¿vale?

**Daniel ACOSTA:** Okay.

**Belen Torres:** Y creo que creo que ya creo que estaría ya todo, ¿vale? Pues os escribo las preguntas que para que lo habléis entre vosotros internamente,

**Otelo Pons:** Vale,

**Belen Torres:** ¿vale? Y ya

**Otelo Pons:** bueno,

**Belen Torres:** estaría.

**Otelo Pons:** más que nosotros e el verlo entre todos, o sea, ¿qué vamos a poner ahí?

**Belen Torres:** Ah, pues entonces lo hablamos ya.

**Otelo Pons:** A ver,

### 00:22:53

**Belen Torres:** Yo que pensaba que lo tenéis que hablar más entre vosotros o vamos como

**Otelo Pons:** no, no. que,

**Belen Torres:** queráis.

**Otelo Pons:** o sea, yo pondría pues eso, una una un un budget de una alerta de budget para poder ir de momento viendo ah por dónde nos vamos a ir

**Belen Torres:** A ver,

**Otelo Pons:** moviendo.

**Belen Torres:** yo sé que las tablas de Google Analytics eso eh a lo mejor filtrando por fecha, no sé de qué fecha tenéis, no me acuerdo que cuál es la fecha.

**Otelo Pons:** analiticis es por fecha de

**Belen Torres:** Claro,

**Otelo Pons:** venta.

**Belen Torres:** pero esos por ejemplo son de muchos teras. Entonces ya es que de ahí de por sí ya van a haber costes en esa query y luego también el modelo al final también consume y el tema de eso ya Dani controla mejor,

**Otelo Pons:** Ya.

**Daniel ACOSTA:** A ver, eh, para mí la mejor forma de manejar en Bquery el coste es con una reserva.

**Belen Torres:** Pero

**Daniel ACOSTA:** No sé si utilizáis reservas.

**Otelo Pons:** No, no, no usamos reservas.

**Daniel ACOSTA:** Ah, pues eso es un ahorro de coste considerable. Eh,

**Otelo Pons:** Bueno,

**Daniel ACOSTA:** yo he visto, no, no, yo he visto hasta hasta corta 90%,

**Belen Torres:** el tema de CUTs,

### 00:23:56

**Otelo Pons:** dependem.

**Daniel ACOSTA:** ¿eh? O sea, de 5000 € al día gastar 500\. Eh,

**Belen Torres:** No.

**Daniel ACOSTA:** viendo que Belén tú tú también has visto,

**Otelo Pons:** Sí,

**Daniel ACOSTA:** o

**Otelo Pons:** pero nosotros pero nosotros h gastamos 1000 € al

**Daniel ACOSTA:** sea,

**Otelo Pons:** mes por

**Daniel ACOSTA:** bueno, muy poco, muy poco me parece para mover todo es

**Otelo Pons:** eso porque lo bastante y de momento las cuotas no llegamos a

**Daniel ACOSTA:** porque

**Otelo Pons:** necesitarlas, aunque posiblemente para este proyecto sí.

**Daniel ACOSTA:** hombre es que claro, el de Vale, vamos a suponer que después de durante este proyecto y hasta que esté todo, vamos a suponer que de 1000 pasamos a 2000, pero vamos a intentarnos quedan 2000 o en 15 ahora te crezca el consumo

**Otelo Pons:** No,

**Daniel ACOSTA:** a 4000 o 5000 € al mes

**Otelo Pons:** no, no, no. Totalmente, totalmente de acuerdo. O sea,

**Daniel ACOSTA:** porque

**Otelo Pons:** que hasta ahora no lo hemos usado, ¿no? Por dos motivos, por motivos justificados, porque no hacía falta.

**Daniel ACOSTA:** claro.

**Otelo Pons:** Ah, que que ahora sí que lo necesitemos.

### 00:25:00

**Belen Torres:** H.

**Otelo Pons:** Y estoy convencido que que

**Daniel ACOSTA:** Porque entiendo, o sea,

**Otelo Pons:** sí,

**Daniel ACOSTA:** aquí la clave es qué consultas se le hacen a Bisquery, o sea, lo el coste de la reserva.

**Otelo Pons:** por eso te digo, ¿a qué le vamos a enchufar ahí? Pues yo no lo

**Daniel ACOSTA:** Claro.

**Otelo Pons:** sé.

**Daniel ACOSTA:** Eh, o sea, bueno, sí lo sabemos porque leamos tenemos que hacer cálculos de todo contra todo, o sea,

**Otelo Pons:** Bueno,

**Daniel ACOSTA:** tenemos que hacer

**Otelo Pons:** vosotros si lo sabéis que vais a hacer los modelos y qué tablas se van a tener que rellenar y cada cuánto y tal.

**Daniel ACOSTA:** Claro,

**Otelo Pons:** Yo ahora no. Yo no te lo sé

**Daniel ACOSTA:** claro. Los modelos al final acceden a datos. los eh tenemos que ver qué pasa con los datos históricos, si hay que reprocesarlo,

**Otelo Pons:** decir.

**Daniel ACOSTA:** que ya hemos dicho que probablemente tendremos castigo una ventana de tiempo para modificar esos datos históricos. O sea, tenemos que hacer algunos cálculos. Belén,

**Belen Torres:** Uz.

**Daniel ACOSTA:** aquí mi recomendación es que hagamos un catchap eh también con Chema nosotros internos, veamos un poco el tema de la reserva y hagamos unas pongamos nosotros unos límites y un y un Es cierto que la reserva el único problema es me parece muy bajo.

### 00:26:10

**Daniel ACOSTA:** O sea, yo no sé si tenemos esos límites tan bajos en las reservas. Estamos hablando de 1000 € al mes, es muy poco. Quizá una reserva como mínimo necesitamos 100 € al día,

**Belen Torres:** H

**Daniel ACOSTA:** creo que 200 € al día, no lo sé. No, no, no tengo ese en la cabeza. Tenemos que investigarlo. Quizás 10 € o 30 50 € al día sea muy poco para una reserva.

**Otelo Pons:** Yo haría una prueba, o sea, cuando tengáis claro un poco que que se va a montar y tal, hacer una prueba con una cuenta de tamaño pequeño,

**Belen Torres:** Hm.

**Otelo Pons:** una de tamaño mediano y una de tamaño grande, que es una ventana temporal y eso no una idea de por dónde van a ir los para todos.

**Belen Torres:** Si ya conforme empecemos a trabajar con eso ya también nos daremos cuenta porque al final estaremos haciendo pruebas y veremos

**Otelo Pons:** Claro, claro. Pero cogería pues una cuenta pequeña y y y con la cuenta pequeña hago los y ya voy a saber un poco por dónde van los tiros. Luego me paso a una mediana y luego ya cuando esté un poco más claro, pues a una más grande porque es que hay mucha diferencia de unas cuentas a

**Belen Torres:** Hm.

### 00:27:17

**Urbano Llamas:** Eso siempre se puede eso gestionar a posterior y lo único A lo mejor el el

**Otelo Pons:** otras.

**Urbano Llamas:** billet de gastos es más importante por no tener un susto, es decir,

**Otelo Pons:** Sí,

**Urbano Llamas:** poner un billet de gasto a nivel proyecto

**Otelo Pons:** sí, claro. Pero para poner un número inicial, pues primero empieza por una pequeña y te y te da una idea de de de del

**Belen Torres:** Hm.

**Urbano Llamas:** para

**Otelo Pons:** ejército en el que te estás moviendo,

**Daniel ACOSTA:** Claro,

**Otelo Pons:** del orden de

**Daniel ACOSTA:** claro.

**Otelo Pons:** magnitud.

**Daniel ACOSTA:** Pero el tema está aquí va por proyecto, o sea, lo podemos poner por data set y por y por región. Es como va la reserva. Pero bueno, lo veo. Bueno,

**Otelo Pons:** Sí, sí,

**Daniel ACOSTA:** o podemos añadir varios dat No,

**Otelo Pons:** pero para estimar los números lo puedes hacer con con una cuenta.

**Daniel ACOSTA:** no. Claro, claro. Vale. Bueno, lo veo yo con Belén y con Chema el tema de la estimación de coste que vamos a necesitar y os hacemos una propuesta. Yo pondría eso, un budget ya. Hm. Claro,

**Otelo Pons:** H

### 00:28:10

**Daniel ACOSTA:** en esta cuenta en la que estamos trabajando es donde tenemos el acceso, o sea, dónde tenéis este coste o esta es una cuenta de sting temporal. No, no, nosotros tenemos directo acceso a producción, ¿no, Belén?

**Belen Torres:** No, eh, lo que tenemos es acceso.

**Otelo Pons:** son vistas. son vistas que he creado en un proyecto específico para vosotros.

**Belen Torres:** Claro,

**Otelo Pons:** O sea, yo ahora veo lo que estáis consumiendo.

**Daniel ACOSTA:** son vistas y y estás dentro de ese proyecto o son vistas hacia otro proyecto.

**Otelo Pons:** Están son vistas hacia otro

**Belen Torres:** hacia otro.

**Daniel ACOSTA:** Hacia otro proyecto. Vale, vamos a tener que que que hacer un poquito de threading ahí.

**Otelo Pons:** proyecto.

**Daniel ACOSTA:** Tenemos que seguir un poco esa esa madriguera de conejo, ¿sabes? Para ver esos costes hacia dónde van. que si yo te hago una vista,

**Otelo Pons:** Ya.

**Belen Torres:** Hm.

**Daniel ACOSTA:** el coste va hacia tu vista origen porque el engine que hace

**Otelo Pons:** M.

**Daniel ACOSTA:** el proceso es tu vista

**Otelo Pons:** Depende.

**Daniel ACOSTA:** origen.

**Otelo Pons:** Y ahora estoy viendo los costes que que generáis vosotros en el proyecto

**Daniel ACOSTA:** Vale, vale.

**Belen Torres:** Vale, pues sí, lo vemos internamente y vemos a ver qué les puede venir mejor.

### 00:29:17

**Belen Torres:** Lo que pasa que es eso que hasta que no veamos bien cuánto va a salir a lo mejor al día o algo así haciendo pruebas,

**Otelo Pons:** Hm.

**Belen Torres:** o sea, se podría ver realmente, o sea,

**Daniel ACOSTA:** Vamos.

**Belen Torres:** con el acceso a, o sea, con viendo vuestro proceso actual, lo que gasta sí que se podría sacar, ¿sabes? Pero bueno, como no tenemos ese acceso hasta que realmente no trabajemos con haciendo queries reales y tal, en plan ya en tiempo real.

**Otelo Pons:** Es que lo tenéis que que que pensar con las cuales que vais a hacer vosotros, no con las que ya hay hechas, porque ahora mismo las que ya hay muchas son para un prepósito específico, que por ejemplo las de Analytic desk para escambiar todas las cuentas nuevo que hay y añadirlo

**Belen Torres:** Claro.

**Otelo Pons:** a estas dos tablas.

**Daniel ACOSTA:** Claro.

**Belen Torres:** O sea,

**Otelo Pons:** punto y es un muy específico,

**Belen Torres:** lo que sí podemos sacar es ya costes de almacenamiento. si podemos porque tenemos las las tablas,

**Otelo Pons:** eso

**Belen Torres:** pero por ejemplo lo que vaya a gastar el modelo eh creo que

**Daniel ACOSTA:** Pero no es el modelo. El modelo no me preocupa a mí. Me preocupa más los costes de querer porque para el que que el modelado al final es muy

### 00:30:10

**Belen Torres:** No.

**Daniel ACOSTA:** pequeño porque son son a raíz de datos pequeños, ¿vale? Esto no es una un agente que hay un montón de bueno, habrá un agente, pero después pero primero hay que analizar y decir, "Venga, por esta cadena vamos a hacer el análisis, por esta cadena, esta cadena y este establecimiento, vamos a hacer este análisis, este análisis y eso hay que reproducirlo todos los días." Entonces eso son unas queries que le va a pegar un palo considerable a la base de datos. Si vamos materializando en diferentes stages, vamos a reducir el número de datos, pero claro, no vamos a poder profundizar los datos y traer más análisis. Por eso es importante decidir esas queries. Tenemos que avanzar un poco en esto. No vamos a poder hacerlo. Decir, aquí tenemos el documento, lo tenemos todo cerrado a 95%.

**Belen Torres:** No, no,

**Daniel ACOSTA:** Es muy difícil cerrar ya.

**Belen Torres:** por supuestísimo. Vamos que ellos lo saben también, que no podemos, o sea, que luego se puede modificar cosas más adelante,

**Daniel ACOSTA:** Es que si es lo que he dicho antes,

**Otelo Pons:** Tam.

**Belen Torres:** que no es que se asocia sea la Biblia y ya

**Daniel ACOSTA:** si no entramos en análisis parálisis,

### 00:31:11

**Belen Torres:** está.

**Daniel ACOSTA:** ¿vale? porque analizamos y nos paralizamos porque no sabemos y tenemos que seguir analizando hasta que nos veamos un poquito más en profundidad y y y compart digamos que hacemos compartimentos, ¿no?, de los datos. Tenemos que tenemos que empezar eso materializando hacia arriba y sobre todo la parte de análisis me preocupa también como tú dices, que hay muchísimos datos. Tenemos que reducir eso drásticamente y quedarnos con lo que nos

**Belen Torres:** Sí, sí. O sea,

**Daniel ACOSTA:** interese.

**Belen Torres:** lo que nos comentó es como 3 años de antigüedad, si acaso. Lo que pasa que no sabemos que va a necesitar el modelo tampoco.

**Daniel ACOSTA:** Yo diría 3 años me parece muy poco, pero bueno, es cierto que la estacionalidad ha cambiado.

**Belen Torres:** Si

**Daniel ACOSTA:** tenías el año de COVID ya hace tres no

**Otelo Pons:** Y no solo de COVID, es lo que decía la semana pasada,

**Daniel ACOSTA:** quiere

**Otelo Pons:** el el 22 sobre todo hubo un subidón post COVID que que que tampoco que tampoco era normal,

**Belen Torres:** no.

**Otelo Pons:** ¿sabes?

**Daniel ACOSTA:** 2021, ¿no?

**Otelo Pons:** más al 22\.

**Daniel ACOSTA:** Claro,

**Otelo Pons:** El 21 empezó, pero 22 fue una

**Daniel ACOSTA:** claro, claro,

**Otelo Pons:** locura.

**Daniel ACOSTA:** claro. La gente ya el wish list, ¿no? Me voy a morir por ya me Bueno,

**Otelo Pons:** Pues ya, claro. Sí, sí. Y claro, eso fue una locura.

**Daniel ACOSTA:** chicos, tengo otra col. Vale.

**Belen Torres:** Vale,

**Daniel ACOSTA:** Eh,

**Belen Torres:** vale. Pues sí, en principio ya la con las preguntas ya eso hemos terminado.

**Otelo Pons:** Venga.

**Belen Torres:** En principio, ¿vale? Cuando ya me ponga eso otra vez ya con el documento y vea si falta algo más, pues ya os lo comento, ¿vale? Y os mando estas preguntas también para que vosotras la para que vosotros lo tengáis también en cuenta, ¿vale? Y y ya está.

**Otelo Pons:** Muy bien,

**Belen Torres:** Eso sería, ¿vale? Así que bueno,

**Otelo Pons:** muy bien.

**Belen Torres:** mañana sí que nos vemos otra vez la en la daily, ¿vale?

**Urbano Llamas:** De acuerdo.

**Otelo Pons:** Vale,

**Urbano Llamas:** Venga,

**Otelo Pons:** genial.

**Urbano Llamas:** gracias.

**Belen Torres:** Pasar buen día.

**Otelo Pons:** Venga, saludo.

**Belen Torres:** Hasta luego.

### La transcripción finalizó después de 00:33:10

*Esta transcripción editable se generó por computadora y puede contener errores. Los usuarios también pueden cambiar el texto después de que se cree.*