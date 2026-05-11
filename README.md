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

El programa pregunta si se desea terminar, se indica que no para que continue con más disparos y hacer un stacking con estos. Cuando el valor convence al operador, entonces se almacenan los datos en un archivo .dat que contiene el tiro stackeado.

## Display

En cada tiro, la ondicula puede visualizarse individualmente traza por traza. La opción ofrece un desplazamiento lateral a lo largo de cada canal usando las flechas derecha e izquierda, iluminada de color verde. En el canal actualmente seleccionado, las flechas arriba y abajo permite aumentar la amplitud de esa traza especifica.

En esta pestaña también pueden modificarse la ventana que se visualiza como se había adelante anteriormente en la configuración inicial.
