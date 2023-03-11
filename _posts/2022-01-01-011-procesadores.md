---
layout: post
title: "Procesadores vs editores de texto"
date: 2022-01-01
badges:
 - type: primary
   tag: edición
 - type: primary
   tag: LaTeX
---

# Análisis comparativo entre procesadores y editores de texto

Los procesadores de texto son programas para la composición de páginas, en donde las palabras se colocan dentro de un archivo, una a continuación de la otra de manera visible en la pantalla --esto sucede en tiempo real-- por consiguiente lo que se ve en la pantalla debería ser igual a lo que va a obtenerse como salida final en la impresora (de escritorio) o en la imprenta y no debería haber sorpresas respecto de lo esperado. En este tipo de programas hay una fuerte interacción entre la etapa de composición (léase la persona que está utilizando el programa) y la presentación que el programa hace en pantalla de lo solicitado, ya que cada tecla o función del programa produce un efecto de manera instantánea, así como también cualquier movimiento o clic hecho con el mouse, a este tipo de composición se la conoce como **composición sincrónica**, precisamente porque cada acción sobre el teclado se traduce en una variación inmediata de lo mostrado en pantalla.

<!--more-->

No hace falta abundar en detalles para especificar que en este tipo de programas, la velocidad sincrónica --es decir el tiempo entre la acción sobre el teclado y la visualización de su consecuencia-- existe una relación directa entre la potencia de la computadora y la calidad (a nivel de programación) del programa que se está ejecutando. Mantener un equilibrio entre estas dos situaciones (composición/visualización) no es tarea fácil, hasta ahora la historia viene mostrado que una va en detrimento de la otra. Es verdad que hoy los programas para procesar textos hacen uso de microprocesadores cada vez más potentes y, por lo tanto, a cada ciclo evolutivo de la tecnología la velocidad de respuesta mejora, sin embargo, el vínculo entre la velocidad y la calidad siempre va a tener limitaciones.

A su vez, la **composición asíncrona**, consiste en introducir el texto en un archivo de [texto plano](https://es.wikipedia.org/wiki/Archivo_de_texto), donde se presta menos atención a su apariencia visual, para procesarlo más tarde con un programa que genere una salida, la persona que escribe interviene todo lo necesario para cambiar la apariencia visual de la salida, pudiendo incorporar mucho más que características de la composición tipográfica, me refiero a que la intervención puede incluir: trabajar con bases de datos, interactuar con otros programas, hacer uso paralelo de lenguajes de programación, manejar una estructura de respuesta a consultas internas dentro del mismo archivo (trabajo con condicionales), tener un manejo particular del corte de palabras y de la ortotipografía, trabajar con múltiples sistemas operativos, hacer cálculos matemáticos, indexar datos de manera aleatoria y un etcétera muy extenso.

Es por eso que en este modo de trabajo se tienen tres momentos:

1. la introducción del texto;
2. el procesamiento para generar la salida;
3. visualizar la salida.

La **composición asíncrona** puede garantizar una mayor capacidad de procesamiento de los datos y con múltiples salidas en comparación con la **composición sincrónica**, esto se debe a que se pueden realizar tareas desvinculadas de la presentación visual en tiempo real y, al no ser necesario tener en cuenta la velocidad de redibujo de la pantalla durante el procesamiento, todos los recursos son aplicados al procesamiento mismo.

## Veamos el caso de LaTeX

LaTeX pertenece al grupo de programas de **composición asíncrona**, con características específicas (ya que es un lenguaje de composición tipográfica); con un editor de texto, el autor/editor/diseñador inserta el texto en un archivo que luego se procesa con un compilador, dependiendo del *driver* de salida que elijamos, podremos obtener diferentes salidas.

El primer archivo generado con el programa editor no solo contiene texto en el sentido estricto del tema contenido, sino también contiene las instrucciones (en el caso de LaTeX las llamaremos «marcas») que luego permiten al compilador saber qué se espera obtener a la salida. Por consiguiente, el texto generado con el editor de texto es un archivo que contiene tanto texto para compilar, como instrucciones necesarias para manipular el texto que se está procesando.

Cuando usamos LaTeX, es común escuchar que «estamos programando», y es verdad, no hay que asustarse con expresiones del tipo «usamos un lenguaje de programación», utilizar LaTeX es estar dando indicaciones de programación a un texto determinado para especificar resultados que esperamos obtener: títulos, secciones, textos con tratamiento especial, composición de fórmulas y similares. Las instrucciones y otras especificaciones generalmente se expresan en inglés (muy simple, reducido a lo esencial) evitando abreviaturas o acrónimos.

Las imágenes a continuación permiten comprender mejor este tipo de lenguaje de marcas. El texto y todas las instrucciones del ejemplo son procesadas por el compilador dando como resultado lo que se observa en la derecha de la figura. El lector aún con pocos conocimientos podrá entender --o al menos darse una idea-- de qué significan las marcas (instrucciones) indicadas dentro del texto.

![]({{site.baseurl}}/assets/img/procesadoreseditores.png){:class="img-responsive"}

![]({{site.baseurl}}/assets/img/procesadoreseditores2.png){:class="img-responsive"}

