# IxTL-074
<img width="2764" height="1589" alt="IMG_3580 copia" src="https://github.com/user-attachments/assets/387dcf2d-a052-4936-80d5-69bd0890ddc7" />

<img width="3024" height="4032" alt="IMG_3504" src="https://github.com/user-attachments/assets/8c8e8c67-cf4a-4a8e-9c1f-e11158738296" />

<img width="3000" height="3336" alt="IMG_3519 copia" src="https://github.com/user-attachments/assets/eb4f5485-d7bf-42f3-8d24-669f75c97459" />

El IxTL-074 es un sintetizador DIY de frecuencia modulada (FM) desarrollado en el Laboratorio de Experimentación Sonora del Centro Multimedia entre agosto y octubre del 2026.

Su nombre proviene de un juego de palabras derivado del nombre de la fibra vegetal extraída de algunas especies de maguey (Ixtle[^1]) y uno de los componentes del sintetizador (el amplificador operacional TL-074). Busca trazar un paralelismo entre el tejido material de fibras vegetales y el sonido derivado de las interconexiones entre operadores de la síntesis FM.

## Funcionamiento
El IxTL-074 se compone de cuatro osciladores de onda cuadrada, cada uno con un rango de oscilación dedicado:

* **Oscilador 1:** 1.7 - 140 Hz aproximadamente
* **Oscilador 2:** 6.5 - 463 Hz aproximadamente
* **Oscilador 3:** 137 - 2266 Hz aproximadamente
* **Oscilador 4:** 147 - 5848 Hz aproximadamente

La frecuencia y amplitud de cada oscilador son determinadas por controles dedicados. La frecuencia puede ser variada mediante una señal moduladora [^2].

Cada oscilador cuenta con:
* **Tres salidas:**
    
    Correspondientes a la frecuencia y a la amplitud establecida con los controles dedicados. Cada salida puede funcionar como:
    * señal de audio, al conectarse a la mezcladora integrada
    * señal moduladora, al conectarse a las entradas de otro oscilador, o a su propia entrada

* **Tres entradas**

    Receptoras de señales moduladoras que derivarán en variaciones de frecuencia de las señales portadoras.

Cada oscilador tiene la capacidad de operar como señal portadora y moduladora simultaneamente.

Las conexiones entre salidas, entradas y mezcladora se establecen utilizando cables puente con puntas macho (también conocidos como "jumpers" o cables DuPont).

El sintetizador funciona con una fuente de alimentación de 9v con punta positiva.

La salida de audio integrada duplica una señal monofónica de audio (doble mono).

## Esquemático
<a href="esquemático.pdf"><img width="5846" height="4134" alt="IxTL-074_JPEG_v 1 0 0" src="https://github.com/user-attachments/assets/0dbc00f7-55a3-4c42-8d35-56736e94ea89" /></a>


## Documentación 
El repositorio posee tres archivos y dos carpetas de apoyo a la documentación:

1. Archivo [_**esquemático.pdf**_](esquemático.pdf)

    Diagrama esquemático de la versión 1.0.0 del sintetizador en formato _pdf_ para su consulta en alta resolución.
2. Archivo [_**lista-de-piezas-y-referencias.pdf**_](lista-de-piezas-y-referencias.pdf)

    Lista detallada de piezas, cantidades y su referencia en el esquemático y la serigrafía de la placa de circuito impreso.

3. Archivo [_**diseño.md**_](diseño.md)

    Descripción general del diseño electrónico del sintetizador para quien desee profundizar en su funcionamiento.

4. Carpeta [**proyecto-kicad**](proyecto-kicad)

    Archivos de diseño electrónico incluyendo esquemático (_.kicad_sch_), diseño de tarjeta de circuito impreso (_.kicad_pcb_) y proyecto (_.kicad_pro_).
   
5. Carpeta [**archivos-de-fabricacion**](archivos-de-fabricacion)

    Contiene los archivos gerber de diseño de tarjeta de circuito impreso usados para la fabricación de la placa.


## Licencia
En concordancia a los valores del conocimiento abierto, que promueven un acceso justo y equitativo a la información, la investigación y la producción de aprendizaje, el presente hardware se distribuye bajo la licencia **CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S-2.0)**, con las siguientes implicaciones:

* **Libertad de uso y fabricación:** Tienes libertad para copiar, modificar y distribuir los archivos de diseño, así como para fabricar, ensamblar y vender productos físicos basados en ellos.
* **Reciprocidad fuerte (Copyleft fuerte):** Si modificas los archivos de diseño o distribuyes productos físicos creados a partir de ellos, estás obligado a liberar todo el diseño derivado bajo esta misma licencia (CERN-OHL-S v2).
* **Disponibilidad del código fuente:** Debes facilitar a los receptores el acceso al código fuente completo (archivos de diseño, esquemáticos, CAD) o indicar claramente la ubicación digital donde puedan descargarlo.
* **Atribución y registro de cambios:** Es obligatorio conservar los avisos de derechos de autor originales y añadir una nota indicando la fecha y una breve descripción de las modificaciones que hayas realizado.
* **Licencia de patentes:** Incluye una concesión de patentes perpetua y sin regalías para fabricar y vender el hardware. Esta concesión se revoca automáticamente si alguien inicia un litigio de patentes contra el proyecto.
* **Sin garantía:** El diseño y los objetos creados se proporcionan "tal cual" (*as is*), sin garantías de funcionamiento o comercialización, y sin responsabilidad legal para los creadores originales.

Para leer el texto legal completo y detallado, consulta el archivo [LICENCE](LICENCE) en este repositorio.

## Créditos

* #### Investigación, desarrollo, diseño de tarjeta de circuito impreso:
    [Francisco Ibrahim](https://www.instagram.com/mxxdbabgkqhkig9w0/) :shipit:, Colaborador del Laboratorio de Experimentación Sonora.
* #### Investigación, asesoramiento y supervisión del proyecto:
    Gonzalo T. Alonso, Jefe del Laboratorio de Experimentación Sonora.

### Agradecimientos
* [**Centro Multimedia**](https://cmm.cenart.gob.mx/) del Centro Nacional de las Artes.
* **Oscar Márquez y Rogelio**, Servicio Social del Laboratorio de Experimentación Sonora. 
* **Juan Galindo**, Jefe del Laboratorio de Robótica y Sistemas Complejos.
* [**Proyecto KiCad**](https://www.kicad.org/) de software libre para la automatización del diseño electrónico.
* Productores cafetaleros de Veracruz y Chiapas.

## Documentación consultada
* Collins N. (2020). Handmade electronic music. New York: Routledge Taylor & Francis Group.
* Electro-Music. (s. f.). Simple 40106 oscillator with diode-based CV input [Archivo PDF]. https://electro-music.com/forum/phpbb-files/rmr_001__simple_40106_oscillator_with_diode_based_cv_input_905.pdf
* Evil Turtle Productions. (s. f.). Analog FM Drone/Kick Synth. https://www.evilturtle.nl/projects/fm-drone-synth
* Keim, R. (2020). Op-Amp Basics: Introduction to the Operational Amplifier. All About Circuits. https://www.allaboutcircuits.com/video-tutorials/op-amp-basics-introduction-to-the-operational-amplifier/
* Klein, M., & Erica Synths. (2021). mki x es.edu VCO manual [Archivo PDF]. Erica Synths.
* Lis A. (2022). 40106 dual oscillator. SFCS: Synthfox Custom Stuff. https://sfcs.neocities.org/module/SFP21/
* Williams, E. (2015). Logic noise: Sweet, sweet oscillator sounds. Hackaday. https://hackaday.com/2015/02/04/logic-noise-sweet-sweet-oscillator-sounds/


[^1]: Más información sobre el Ixtle y su uso en el Valle del Mezquital: https://tesiunamdocumentos.dgb.unam.mx/ptd2013/octubre/0702151/Index.html
[^2]: La modulación de frecuencia es un método de síntesis sonora. Consiste en variar (modular) la frecuencia de una señal (denominada portadora) con respecto a otra (denominada moduladora). El rango de la modulación de la frecuencia de la señal portadora será proporcional a la amplitud de la señal moduladora. La velocidad de la modulación de la frecuencia de la señal portadora será proporcional a la frecuencia de la señal moduladora.
