# SCS Information

En este repositorio, incluyo documentación del software SCS (Seismodule Controller) que voy recolectando desde mi experiencia e internet. Además del uso que se aplica en las practicas de sismica de refracción con este software y el sismógrafo Geode, ambos de Geometrics.

## Configuraciones iniciales

Lo principal es dar inicio a un nuevo survey, para lo cual debe elegirse un modo en "Survey Mode".

La sismica de refracción de ondas P, es indica con un tilde refracción mientras que la sismica con ondas superficiales (MASW) se indica con un tilde en Others. Luego de estos parametros debe setearse el intervalo de Geófonos junto con el intervalo en la ventana temporal donde se indica el Record Length y la extensión. El delay debe dejarse en 0.

Ondas P:
62.500 us y 0.2 sec

MASW:
0.500 ms y 3 secs

Luego en la configuración de las Boundaries temporales pueden modificarse esos valores.

La polaridad se matiene positiva.

## Geometría

Aquí se establecen las coordenadas de los geófonos y del tiro. Por obvias razones estos valores (del tiro) se deben modificar a medida que se avanza en la energización. Las ganancias se irán cambiando en este avance para evitar saturación en geófonos cercanos, con lo cual se ponen en baja aquellos en un rango de 3 y más alla se dejan en alta. 

## Trigger

Se debe armar con la tecla 1 para habilitar el golpe. En esta instancia el color de la parte inferior de la barra es verde y en el golpe cambia a amarillo.

El programa pregunta si se desea hacer un "unstacking", se indica que no para que continue con más disparos y hacer el stacking con estos. Cuando el valor convence al operador, entonces se almacenan los datos en un archivo .dat que contiene el tiro stackeado.

## Display

En cada tiro, la ondicula puede visualizarse individualmente traza por traza. La opción ofrece un desplazamiento lateral a lo largo de cada canal usando las flechas derecha e izquierda, iluminando de color verde cada traza. En el canal actualmente seleccionado, las flechas arriba y abajo permite aumentar la amplitud de esa traza especifica.

En esta pestaña también pueden modificarse las dimensiones de la ventana del display ("boundaries"), como se había mencionado anteriormente en la configuración inicial.

# Syscal

Una vez hechas las conecciones se enciende el equipo (interruptor on/off). En caso de haber datos grabados, se procede a su eliminación o extracción para comenzar a grabar desde 0. En todo caso se puede continuar con la grabación anterior de datos aunque se prefiere lo primero para tener mayor control de la memoria del equipo ya que es bastante limitada.

Para eliminar datos se navega a la pestaña "Memory", de ella se va a "Delete data". Lo proximo será una pregunta, entre que puntos se encuentran los datos a eliminar. Ingresarlos y confirmar.

## Mode

Es importante el seteo del modo de survey o protocolo. Para lo cual se elige PINCHAR36, ya que en este caso se trabaja con 36 electrodos/conectores.

PINCHAR36 es un procolo de revisión para verificar el estado de las conexiones de cada electrodo. 

## Survey

Una vez elegido el protocolo se da inicio al survey con START, esto da comienzo a la revisión mencionada anteriormente, antes preguntara si queremos cambiar el nombre del survey o los limites de puntos. En negro se marcaran aquellos que muestren resistividades altas (999.999 kOhm), demostrando que no existe conductividad y ese electrodo debe revisarse. 

## Medición

Se debe cambiar el protocolo con la opción Mode, ya sea a Wenner o Sch. Luego con Start se da comienzo al survey, para lo cual cambiaremos
su nombre. La medición comienzo y los datos se guardan.

## Finalizando

El archivo se guarda automaticamente. El equipo se apaga y desconecta. El survey termino.

## Los datos del survey

Solo resta obtener los datos, para cual se utiliza un adaptador a SD card. Debe hacerse la descarga de datos en download data.

Listo, los datos pueden accederse conectado la SD card a la PC.
