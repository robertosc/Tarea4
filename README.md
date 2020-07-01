# Tarea4

## Parte 1: Modulación BPSK

La modulación binaria por desplazamiento de fase, conocida como BPSK por sus siglas en inglés, es un tipo de modulación de señales discretas a señales analógicas. Es decir, este método toma datos codificados en binario y los modula en forma de señales sinusoidales. Cuando se lee un bit y este es uno, la modulación tendrá la forma de un seno sin desfase, cuando se lee un 0 la modulación tendrá forma de un seno desplazado 90°, por cuanto, la señal puede ser fácilmente demodulada por medio del proceso inverso, buscando senos con y sin desfase.

Para esta tarea se pedía modular una conjunto de datos conformado por 10000 bits por medio de la modulación BPSK. Para ello se leyó el documento utilizando la librería pandas. Para la modulación se definieron los distintos vectores de tiempo, de modo que se abarcase la cantidad total de bits del archivo. Puesto que se usó una frecuencia de 5000 Hz y 100 puntos de muestra por periodo, la frecuencia de Nyquist es de 500kHz, la cual se utiliza como frecuencia de muestreo. Al leer los bits, si se hallaba un 1, se asignaba un seno a un espacio previamente vacío, caso contrario se asignó un seno negativo. Se este modo se btuvo la señal modulada.

<img src="../master/images/modulada.png" width="80">

En la imagen previa se modulan los primero 10 bits.

## Parte 2: 




