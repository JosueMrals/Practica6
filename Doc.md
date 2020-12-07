## 1.1: Crear el proyecto con dos Activities

> *Cree una app con las siguientes características:*

<img src="medios\1.png"/>

> *Cree la segunda Activity yendo al panel **Project > Android** y dar clic derecho sobre la carpeta app de su proyecto y dar a **New > Activity > Empty Activity**,nombre este activity como **Segunda**.*

<img src="medios\2.png"/>
<img src="medios\3.png"/>


## 1.2: Diseñando la primera Activity 

## Detallando las propiedades del activity_main

> *Abra activity_main.xml desde el panel Proyecto > Android si aún no está abierto. Si la pestaña Design (diseño) aún no está seleccionada, haga clic en ella.*

<img src="medios\4.png"/>

> *A continuación, se le presenta la estructura del activity, su trabajo será diseñar en base a lo mostrado, es posible que no obtenga el mismo diseño solicitado, pero se le recomienda explorar al momento de crear, es libre de diseñar a su manera, pero cuidando la estructura otorgada.*

<img src="medios\6.png"/>
<img src="medios\7.png"/>

> *Establezca la propiedad visibility a invisible a los TextView del activity_main, estos serán activados en el momento en que la segunda activity le mande un resultado, en primera instancia están ocultos.*

<img src="medios\5.png"/>

> *Establezca el evento onClick al botón del activity_main que tiene el identificador btEnviar, puede usar el siguiente código XML. Puede usar la corrección automática para generar el código correspondiente a este manejador de evento.*

<img src="medios\8.png"/>

> *En el caso de que no pueda generar el método a través de las correcciones automáticas, tiene la siguiente estructura*

<img src="medios\9.png"/>

## Agregando un Intent al MainActivity.kt

> *Abra el fichero MainActivity.kt*

> *Agregue un object companion dentro de la clase MainActivity, no dentro de algún método, este servirá para simular un objeto estático que no cambia el valor de sus propiedades en toda la aplicación. El valor EXTRA_MESSAGE nos servirá para la clave del extra en el intent.*

<img src="medios\10.png"/>

> *Agregue el siguiente código en el método lanzarSegundaActivity, relacionado a la creación de un intent.*

<img src="medios\11.png"/>

> *Muestre el resultado en el momento en que la segunda activity fue lanzada*

> *Regrese a la activity principal e indique que instancias del ciclo de vida del activity se han ejecutado*

## 1.3: Compartiendo datos de Activity principal a la segunda

> *Agregue el siguiente código para enviar datos activities, debe reemplazar el código anterior del método **lanzarSegundaActivity**. Muetre los resultados.*

<img src="medios\13.png"/>

## Modificando la segunda activity para obtener los extras

> *Abra el fichero **Segunda.kt** para agregar código al método **onCreate()**.*

<img src="medios\14.png"/>

> *Obtenga el intent que activó esta activity*

<img src="medios\15.png"/>

> *Obtenga la cadena que contiene el mensaje de los extras de Intent usando el valor del objeto creado en la activity principal y obtenerlo usando la clave **MainActivity.EXTRA_MESSAGE**:*

<img src="medios\16.png"/>

> *Use **findViewById()** para obtener la referencia del **TextView** para el mensaje del layout.*

<img src="medios\17.png"/>

> *Establezca el texto del **TextView** con la cadena obtenida del extra del intent*

<img src="medios\18.png"/>

> *Ejecute la aplicación. Cuando escriba el mensaje en el **MainActivity**, haga clic en el botón **Enviar**, se lanza la **SegundaActivity** y se muestra el mensaje*

> *Muestre resultados a través de capturas de pantalla y comentarios*

<img src="medios\19.jpg"/>
<img src="medios\20.jpg"/>

        Ahi se puede observar en la primer captura que se ingresa la palabra "Hola", y se manda a la segunda ventana, mostrandose en el segundo texto en la parte superior de la pantalla.

## 1.4 Devolver datos al activity principal

> *Abra el fichero **activity_segunda.xml** y verifique que dispone de la estructura indicada al principio de estas tareas con sus identificadores correspondientes.*

> *Establezca el evento **onClick** al botón con identificador **btRes**.*

<img src="medios\19.png"/>

> *Solamente queda crear el método **devolverRespuesta()**, el cual puede agregarlo después del cierre de llave del método **onCreate()**.*

<img src="medios\20.png"/>

## Crear respuesta del intent en la segunda Activity

> *Abre **Segunda.kt** por si aún no lo está.*

> *Agrega un companion object para obtener una sola instancia de objeto sin necesidad de crear una nueva, esto se debe agregar después de la apertura de la llave de la clase Segunda, al inicio para no generar confusiones.*

<img src="medios\21.png"/>

> *Agregue el código del método **devolverRespuesta()**.*

<img src="medios\22.png"/>


