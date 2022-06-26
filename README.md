## Generador de granos
### Funcionamiento
Se trata de un generador de granos que toma como señal de entrada la lectura de una muestra de audio almacenada en memoria. A partir de la lectura de aquella muestra, se toman muestras más pequeñas de duración variable (__granos__) que se "recortan" y se reproducen de forma iterada o a disposición del accionar del usuario. Se pueden cargar archivos de audio en formato .wav y 44100Hz. La
### Uso
Este patch funciona correctamente con pd vanilla 0.49. Abrir el archivo desde el mismo programa y seguir las instrucciones detalladas para el seteo inicial y el manejo de la interfaz que se encuentran en el mismo patch.
### Generalidades técnicas
- Se dispone de dos métodos de lectura diferentes: "rampa lineal única" y "señal diente de sierra contínua".
- Para el manejo de las velocidades de reproducción se optó por leer distintas cantidades de muestras. Otra opción a revisar es la lectura de más de un ciclo de una misma cantidad de muestras en el mismo intervalo de tiempo (duración del grano).
