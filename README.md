# Respuestas Evaluación 2 Introducción a Tecnologías de la Información 

## Integrantes 
1. Paula Sánchez
2. Danna Tapiero 
3. Brigitte Rodriguez 
4. Miguel Camargo

---

## Pregunta 1
D. 11000 milisegundos.
### Justificación: 
El ciclo del semáforo dura 11.000 milisegundos, porque es la suma de los tiempos: verde 5000, amarillo 2000 y rojo 4000.

## Pregunta 2 
C.  Ejecuta el subcomando compile e indica el identificador de la placa.
### Justificación: 
Permite verificar que el código esté bien escrito y corregir errores de sintaxis antes de cargarlo en la placa Arduino.

## Pregunta 3
D. Los LEDs de los bits 0, 2 y 3.
### Justificación:
 Al realizar 13 pulsaciones, el contador llega al número 13, que en binario es 1101. Por eso, los LEDs de los bits 0, 2 y 3 quedan encendidos, mientras que el bit 1 permanece apagado.

 ## Pregunta 4
C. Ignora nuevas lecturas del pulsador durante un breve intervalo tras detectar el primer cambio.
### Justificación:
 La técnica de debounce evita que las pequeñas variaciones eléctricas del pulsador se registren como múltiples pulsaciones. Así, cada presión real se cuenta una sola vez y el contador funciona correctamente.

 ## Pregunta 5
A. 4 patrones.
### Justificación:
Como los canales 1 y 2 son los únicos que arman el patrón de encendido usando una tabla de verdad, y cada uno tiene dos posiciones posibles, te dan un total de 4 combinaciones distintas, mientras que los otros dos canales se quedan solo controlando la velocidad.

  ## Pregunta 6
 D. Nivel LOW porque el contacto cerrado impone sobre el pin una tensión de cero voltios.
### Justificación:
 Cuando el interruptor se coloca en ON, el contacto se cierra y conecta el pin directamente a tierra. Por eso, el pin recibe una tensión de 0 voltios y la función digitalRead() devuelve un nivel LOW.

  ## Pregunta 7
 B. 800 milisegundos.
### Justificación:
El recorrido tiene 6 pasos de ida y 6 de regreso, pero los LED de los extremos se encienden una sola vez. Por eso, se realizan 10 pasos en total. Como cada paso dura 80 milisegundos, el ciclo completo dura 10 × 80 = 800 milisegundos.

  ## Pregunta 8
A. Agregar el usuario al grupo dialout y reiniciar su sesión en Debian 13.
### Justificación:
 En Debian, el grupo dialout permite a los usuarios autorizados acceder a los puertos serie. Agregar el usuario a este grupo y reiniciar la sesión permite que los nuevos permisos se apliquen y facilita la comunicación entre Arduino CLI y la placa.
 
  ## Pregunta 9
 D.  204.
### Justificación:
 La función map() convierte la lectura analógica de 819, cuyo rango es de 0 a 1023, al rango de 0 a 255. El cálculo es aproximadamente 819 × 255 ÷ 1023 = 204, que es el valor enviado a analogWrite().

  ## Pregunta 10
C. El monitor muestrea los bits con una tasa distinta a la configurada en el sketch.
### Justificación:
 El sketch está configurado a 9600 baudios, pero el monitor serial está a 115200 baudios. Como las velocidades son diferentes, los datos se interpretan incorrectamente y aparecen caracteres ilegibles.

  ## Pregunta 11
C. 4,7 segundos. 
### Justificación:
La constante de tiempo se calcula multiplicando la resistencia por la capacitancia. Con una resistencia de 10000 ohmios y un capacitor de 0,00047 faradios, el resultado es 10000 × 0,00047 = 4,7 segundos.

  ## Pregunta 12
A. Solo la declaración 1 es verdadera.
### Justificación:
Durante la descarga, la tensión del capacitor disminuye exponencialmente hasta aproximarse a cero. Sin embargo, después de una constante de tiempo durante la carga, el capacitor alcanza aproximadamente el 63,2 % de la tensión de la fuente, no el 100 %.

  ## Pregunta 13
 B. 4,3 miliamperios.
### Justificación:
  La tensión en la resistencia de base es aproximadamente 4,3 V, porque a los 5 V de alimentación se les resta la caída de 0,7 V de la unión base-emisor. Aplicando la ley de Ohm, la corriente es I = 4,3 V / 1000 Ω = 0,0043 A, es decir, 4,3 mA.

  ## Pregunta 14
B. Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.
### Justificación:
 La bobina del motor genera una tensión inducida cuando se interrumpe la corriente que circula por ella. El diodo conectado en paralelo proporciona un camino para esa corriente y limita el pico de tensión, protegiendo así al transistor.

  ## Pregunta 15
C. Pin digital 9. 
### Justificación:
 El Arduino UNO R3 dispone de salidas PWM en los pines digitales 3, 5, 6, 9, 10 y 11. Como el pin 9 aparece entre las opciones, es el correcto para controlar la señal PWM mediante analogWrite().
 
  ## Pregunta 16
 D. Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.
### Justificación:
 La bobina del relé necesita 72 miliamperios, pero el pin de Arduino soporta como máximo 40 miliamperios, según el enunciado. Por eso, se utiliza un transistor que permite controlar el relé sin exigirle tanta corriente directamente al pin.

  ## Pregunta 17
 B. Solo la declaración 2 es verdadera.
### Justificación:
 La declaración 1 es falsa porque la bobina del relé y los contactos del motor están separados eléctricamente. La declaración 2 es verdadera, ya que el diodo evita los picos de tensión al interrumpirse la corriente y protege los componentes del circuito.

  ## Pregunta 18
 A. Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor. 
### Justificación:
Esta diferencia evita que el relé se encienda y apague repetidamente cuando la lectura está cerca de 700. Al usar 700 para encenderlo y 600 para apagarlo, el sistema funciona de forma más estable.

  ## Pregunta 19
 D. El pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().

### Justificación:
 Cuando la puerta está cerrada, el pin 2 lee HIGH; al abrirse, lee LOW por la resistencia pull-down. El programa detecta el cambio y activa el buzzer con `tone()` para emitir una alerta.

  ## Pregunta 20
 B. La afirmación es verdadera, mientras que la razón es una proposición falsa.

### Justificación:
La afirmación es verdadera porque `tone()` permite que un buzzer pasivo emita una frecuencia definida, pero la razón es falsa, ya que genera una señal que alterna entre HIGH y LOW. La función `noTone()` detiene la generación del sonido.

  ## Pregunta 21
A. Disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.
### Justificación:
En el circuito hay una fotoresistencia LDR conectada entre 5 Voltios y el Pin analógico A0, y una resistencia de 10 Kiloohmios entre el Pin A0 y Tierra; Si se disminuye la luz ambiental, aumenta la resistencia de la fotoresistencia LDR, causando que haya una disminución en el voltaje en el punto del Pin A0 y que el Arduino marque la lectura analógica como menor.

  ## Pregunta 22
 A. 2 LEDs. 
### Justificación:
 La función map() sirve para convertir un valor de un rango a otro. En este caso, el valor de entrada es 450, que está dentro del rango de 0 a 1023, y se convierte al rango de 0 a 5. Como Arduino trabaja con números enteros en esta operación, el resultado es 2. Por eso, si se utiliza ese resultado para encender los LED, se encenderían 2.

  ## Pregunta 23
 C. II, I, III, IV.
### Justificación:
Primero, el semáforo vehicular cambia de verde a amarillo y después a rojo para detener los vehículos. Luego, el semáforo peatonal cambia a verde para permitir el paso de las personas. Finalmente, el semáforo peatonal vuelve a rojo y los vehículos pueden avanzar nuevamente. 

  ## Pregunta 24
B. La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.
### Justificación:
 Al abrir el puerto serie, el Arduino puede reiniciarse. Por eso, si se envía el comando demasiado pronto, la placa todavía no está lista para recibirlo.

  ## Pregunta 25
 D. Ejecutar core update-index y core install con el paquete arduino:avr.
### Justificación:
 Estos comandos actualizan la información de los paquetes e instalan el soporte necesario para la placa Arduino UNO R3, permitiendo compilar el programa.