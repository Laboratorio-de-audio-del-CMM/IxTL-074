# IxTL-074

El IxTL-074 es un sintetizador DIY semimodular de frecuencia modulada desarrollado en el Laboratorio de Experimentación Sonora del Centro Multimedia entre agosto y octubre del 2026. Se compone de cuatro osciladores de onda cuadrada especializados en distintas frecuencias:

* Oscilador 1: 1.7 - 140 Hz aproximadamente
* Oscilador 2: 6.5 - 463 Hz aproximadamente
* Oscilador 3: 137 - 2266 Hz aproximadamente 
* Oscilador 4: 147 - 5848 Hz aproximadamente

La frecuencia y amplitud de cada oscilador puede ser controlada mediante las perillas señaladas en la placa como "frec" y "amp".

Cada oscilador cuenta con:
* Tres salidas: 

    Correspondientes a la frecuencia y a la amplitud establecida con las perillas. Pueden usarse como: 
    * salidas de audio (cuando se conectan a la mezcladora)
    * frecuencias de modulación [^1] (cuando se conectan a las entradas de otro oscilador, o a su propia entrada)

* Tres entradas

    Receptoras de las ondas que modularán la frecuencia base del oscilador

Las conxiones entre salidas y entradas y mezcladora se establecen utilizando cables puente con puntas macho (también conocidos como cables "jumpers" o DuPont).

El sinteizador funciona con una fuente de alimentación de 9v conectada a un barril jack de 5.5mm x 2.1mm con punta positiva. 

Es un sintetizador monofónico (todo suena en un solo canal) pero posee salida de audio estéreo (duplicando la señal mono) por medio de un conector jack hembra de 3.5 mm

El nombre del sintetizador proviene de un juego de palabras derivado del nombre de la fibra vegetal extraida de algunas especies de maguey (Ixtle[^2]) y uno de los componentes del sintetizador (el amplificador operacional TL-074). Busca trazar un paralelismo entre el tejido material de fibras orgánicas y al sonido derivado de las interconecciones entre operadores de la síntesis FM. 

# Lista de materiales

La lista completa de materiales necesarios para la construcción del IxTL-074 es:

* **Circuitos integrados**
    * Inversor Schmitt trigger 40106 x1
    * Amplificador operacional TL-074 x1

* **Potenciómetros**
    * 10k x1
    * 50k x6
    * 100k x2

* **Capacitores electrolíticos**
    * 0.22μF x1
    * 1μF x2
    * 4.7μF x1
    * 10μF x1

* **Capacitores cerámicos**
    * 100nF x5

* **Resistencias**
    * 470 x3
    * 1k x6
    * 10k x4
    * 100k x2

* **Otros componentes**
    * Transistor 2N394 x1
    * LED de 5mm x1
    * Header hembra de 2x2 x1
    * Headers hembra de 2x3 x4
    * Switch SPDT x1
    * Conector jack de 3.5mm SJ1-3515
    * Barril jack de 5.5mm x 2.1mm
    * Fuente de alimentación de 9v con salida jack de punta positiva de 5.5mm x 2.1mm (se recomienda una pila de 9v con un broche)

Los headers pueden sustituirse con una tira larga (que usualmente es más fácil de conseguir) y ser recortados posteriormente. 

El conector de jack de 3.5mm también puede ser sustituido por un conector más fácil de conseguir o que se adapte mejor a las necesidades de quien lo construya.

# Apoyo a la documentación 
El repositorio posee una carpeta titualada "Esquemático" que contiene el diagrama esquemático de la versión 1.0.0 del sintetizador en versión pdf y en archivo editable de KiCad .kicad_sch

# Créditos  

* Investigación, desarrollo y diseño de tarjeta de circuito impreso: Francisco Ibrahim :shipit:, colaborador del Laboratorio de Experimentación sonora.
* Investigación, asesoramiento y supervisión: Gonzalo T. Alonso, Jefe del Laboratorio de Experimentación Sonora. 

#### **Agradecimientos**
* Centro Multimedia
* Juan Galindo, Jefe del Laboratorio de Robótica y Sistemas Complejos 
* [Proyecto KiCad](https://www.kicad.org/) de software libre para la automatización del diseño electrónico.
* Productores cafetaleros de Veracruz

[^1]: Variación de frecuencia a la velocidad del oscilador modulante.  
[^2]: Más información sobre el Ixtle y su uso en el Valle del Mezquital: https://tesiunamdocumentos.dgb.unam.mx/ptd2013/octubre/0702151/Index.html
