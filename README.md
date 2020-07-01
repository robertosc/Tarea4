# Tarea4

## Parte 1: Modulación BPSK

La modulación binaria por desplazamiento de fase, conocida como BPSK por sus siglas en inglés, es un tipo de modulación de señales discretas a señales analógicas. Es decir, este método toma datos codificados en binario y los modula en forma de señales sinusoidales. Cuando se lee un bit y este es uno, la modulación tendrá la forma de un seno sin desfase, cuando se lee un 0 la modulación tendrá forma de un seno desplazado 90°, por cuanto, la señal puede ser fácilmente demodulada por medio del proceso inverso, buscando senos con y sin desfase.

Para esta tarea se pedía modular una conjunto de datos conformado por 10000 bits por medio de la modulación BPSK. Para ello se leyó el documento utilizando la librería pandas. Para la modulación se definieron los distintos vectores de tiempo, de modo que se abarcase la cantidad total de bits del archivo. Puesto que se usó una frecuencia de 5000 Hz y 100 puntos de muestra por periodo, la frecuencia de Nyquist es de 500kHz, la cual se utiliza como frecuencia de muestreo. Al leer los bits, si se hallaba un 1, se asignaba un seno a un espacio previamente vacío, caso contrario se asignó un seno negativo. Se este modo se btuvo la señal modulada.

<img src="../master/images/modulada.png" width="450">

En la imagen previa se modulan los primero 10 bits.

## Parte 2: Cálculo de potencia promedio

Se calculó la potencia pormedio de la señal modulada. Esta se calcula por medio de la integral de la señal al cuadrado, dividida entre el tiempo multiplicado por un factor de 2. Para calcular esta integral se utilizó la función integrate.trapz, que calcula integrales por medio de trapezoides. Se obtuvo que la potencia promedio es P = 0.499

## Parte 3: Simulación de un canal ruidoso

# añadir formulas

Se simuló la transmisión de la señal por un medio desconocido. Para este caso solo se consideró la existencia de la aparición de ruido blanco en la señal modulada. En esta sección se añadió ruido con potencias promedio de ditintas magnitudes. Se calculó un ruido de -2dB, -1dB, 0dB, 1dB, 2dB y 3dB. El ruido se generó a partir de valores aleatorios con una distribucion normal, estas magnitudes obtenidas se le sumaron a la señal modulada. Se obtuvieron los siguientes resultados.

<img src="../master/images/ruido_neg_2.png" width="450">

<img src="../master/images/ruido_neg_1.png" width="450">

<img src="../master/images/ruido_0.png" width="450">

<img src="../master/images/ruido_1.png" width="450">

<img src="../master/images/ruido_2.png" width="450">

<img src="../master/images/ruido_3.png" width="450">

Se puede observar que conforme se aumenta el SNR, se disminuye el nivel de ruido y la señal es más clara.


## Parte 4: Densidad espectral de potencia
