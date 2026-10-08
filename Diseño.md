# Funcionamiento electrónico del IxTL-074
El funcionamiento a nivel electrónico del IxTL-074 se compone de 5 etapas principales:

* [Alimentación](#alimentación)
* [Oscilación](#oscilación)
* [Almacenamiento en buffer](#almacenamiento-en-buffer)
* [Salidas y modulación](#salidas-y-modulación)
* [Mezcladora](#oscilación)

## Alimentación 
El circuito funciona con una fuente de alimentación de 9V. Se enciende y apaga por un medio de un interruptor SPDT `SW1`. 

## Oscilación
La oscilación de onda cuadrada del **IxTL-074** se genera mediante la retroalimentación del circuito integrado 40106 `U1`, un inversor Schmitt trigger séxtuple.

Un **Inversor Schmitt Trigger** es un componente electrónico que combina dos funciones:
1. **Inversor**

    Invierte la señal que recibe. Si entra un **1** (encendido/energía), saca un **0** (bajo/apagado) y viceversa.

2. **Schmitt Trigger**

    Filtro anti-ruido. Añade un margen de tolerancia para evitar que la señal fluctue o cambie de estado por error cuando hay ruido eléctrico. Este componente es clave para convertir señales analógicas y/o ruidosas en ondas cuadradas que generan la frecuencia base de cada oscilador.

Cada circuito de oscilación incorpora además un capacitor y una resistencia.

* El capacitor almacena y libera energía eléctrica. Contribuye a definir la duración del ciclo según el tiempo que tarda en cargarse y descargarse. El tiempo que tarda en cargarse y descargarse se define por su valor de capacitancia.

* La resistencia regula el flujo de corriente hacia el capacitor:
     * A mayor resistencia, el tiempo de carga es más lento, resultando en una frecuencia más baja (grave).
     * A menor resistencia, el capacitor se carga y descarga más rápido, generando una frecuencia más alta (aguda).

    Con la incorporación de resistencias variables (potenciómetros) es posible ajustar la frecuencia del oscilador según nuestras necesidades creativas.

## Almacenamiento en buffer

Para mantener la estabilidad de las frecuencias generadas por los osciladores, se utiliza el circuito integrado **TL-074**, que contiene cuatro amplificadores operacionales.

Cada amplificador operacional está configurado como un buffer de almacenamiento que evita que los circuitos de etapas posteriores (como la mezcladora) alteren el funcionamiento del oscilador, previniendo cambios no deseados de frecuencia.

## Salidas y modulación

Potenciómetros de 50 kΩ (`R3`, `R7`, `R11`, `R15`) regulan la amplitud de cada oscilador.

Los headers hembra (`J1`, `J2`, `J3`, `J4`) permiten la interconexión personalizada de salidas y entradas necesaria para la síntesis FM.

La etapa de modulación incorpora capacitores (`C2`, `C4`, `C6`, `C8`) de 100 nF que eliminan el componente de corriente directa (DC) de la onda cuadrada, permitiendo permitiendo una mejor modulación. 

## Mezcladora
La etapa de mezcla suma las señales de los 4 osciladores en una sola señal de salida estandarizada de audio.

El potenciómetro `R21` atenúa el nivel general de la mezcla antes de enviarla a la salida.

Un capacitor final `C9` remueve cualquier residuo DC restante antes de entregar la señal al conector jack estéreo/mono de 3.5 mm `J6`.

La señal procesada excita la base del transistor **2N3904**, el cual conmuta la corriente a un diodo emisor de luz (LED) brindando retroalimentación visual del ritmo y pulsación de la onda producida.


