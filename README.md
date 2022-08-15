## Grain generator
This is a granular synthesis patch that can be run on Pure Data vainilla (^0.49) or Purr Data. It has been designed as a grain generator which you can use to produce sound materials for further compositions. By the moment, synchronous and asynchronous synthesis are supported. Please note that this is not a final version, so it may have bugs.

### How it works
The grain generator takes an input signal that comes from an array loaded with a soundfile sample that you can choose and read from disk. The patch takes smaller samples from the loaded soundfile, which are called __grains__. Those grains can be played in an iterative way (at regular time intervals), or either sequenzed or triggered by the user -pressing the 'play button'-. Soundfiles must be in .wav format (44100Hz).
### How to use
To use this patch you must have Pure Data vanilla (0.49 or newer) installed in your computer. To run the patch, just open the 'main.pd file' located in the project folder and follow the instructions written on the main screen of the user interface.
NOTE: For now, instructions are written in spanish (They will be translated in the future).
### Technical specs
- There are two grain playback methods available: "single line ramp" and "continuos sawtooth". By default, the single line ramp is used to play grains when using asynchronous synthesis. Both methods are available to be used for synchronous synthesis. You can test them to hear the differences.

## Generador de granos
Éste patch es una implementación de sintesis granular que se puede utilizar en Pure Data Vainilla (^0.49) o bien en Purr Data. Fue pensado como un generador de granos para utilizar como generador de materiales para futuras composiciones. Por el momento, soporta síntesis sincrónica y síntesis asincrónica. 
NOTA: ésta no es una versión final del patch

### Funcionamiento
Se trata de un generador de granos que toma como señal de entrada la lectura de una muestra de audio almacenada en memoria. A partir de la lectura de aquella muestra, se toman muestras más pequeñas de duración variable (__granos__) que se "recortan" y se reproducen de forma iterada o a disposición del accionar del usuario. Se pueden cargar archivos de audio en formato .wav y 44100Hz.
### Uso
Este patch funciona correctamente con pd vanilla 0.49. Abrir el archivo desde el mismo programa y seguir las instrucciones detalladas para el seteo inicial y el manejo de la interfaz que se encuentran en el mismo patch.
### Generalidades técnicas
- Se dispone de dos métodos de lectura diferentes: "rampa lineal única" y "señal diente de sierra contínua". Por defecto, el método de "rampa lineal única" se utiliza en síntesis asincrónica (es más fácil de controlar a nivel temporal). Para síntesis sincrónica, se pueden usar ambos métodos. Podés testear cuál te sirve mejor, ya que arrojan resultados sonoros diferentes -en especial para duraciones de granos muy cortas-. El método the phasor (o diente de sierra) suele ser mejor para sintetizar sonidos tónicos partiendo de granos muy breves. 
- Para el manejo de las velocidades de reproducción se optó por leer distintas cantidades de muestras. Otra opción a revisar es la lectura de más de un ciclo de una misma cantidad de muestras en el mismo intervalo de tiempo (duración del grano).
