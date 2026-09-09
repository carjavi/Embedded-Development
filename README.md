<p align="center"><img src="./img/banner.jpg" width="600"   alt=" " /></p>
<h1 align="center"> Embedded Development </h1> 
<h4 align="right">Sep 26</h4>

<p>
  <img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
  <img src="https://img.shields.io/badge/OS-Windows%2011-blue">
  <img src="https://img.shields.io/badge/Hardware-Raspberry%20ver%204-red">
  <img src="https://img.shields.io/badge/Hardware-ESP32-red">
  <img src="https://img.shields.io/badge/Hardware-STM32-red">
</p>

<br>

# Table of contents
- [Table of contents](#Table-of-contents)
- [Install](#Install)
- [Troubleshooting](#Troubleshooting)

<br>


## The Embedded Systems Roadmap 
* Core Embedded Skills (Non-Negotiable)
* C / Embedded C & Linux embedded
* Microcontrollers (ARM, ESP, STM32)
	* ARM Cortex-M (used in automotive and industrial systems)
	* ESP32 (popular for IoT and smart devices)
	
* RTOS Concepts
	* Tasks and scheduling
	* Semaphores and mutexes
	* Inter-task communication
	* Real-time constraints

* Communication Protocols (UART, SPI, I2C, CAN)
	* UART – debugging and serial communication
	* SPI & I2C – sensor and peripheral communication
	* CAN – automotive and EV systems

* AI-Assisted Tools (Career Boosters)
	* AI Code Assistants
		* AI coding tools help embedded engineers:
		 	* Generate boilerplate driver code
			* Explain legacy firmware
			* Suggest optimizations
			* Reduce development time
			* Optimized for memory and timing
* Embedded ML Frameworks (TinyML Basics)
	* Smart sensors
	* Predictive maintenance
	* Wearable and medical devices

* Simulation & Testing Automation Tools
	* Use simulators before hardware arrives
	* Automate unit testing
	* Validate firmware using logs and test cases

<br>
<br>


## Linux embedded:
```Yocto```: Es un conjunto de herramientas y plantillas muy potente.sirven para crear ese sistema operativo a la medida.Es el estándar en la industria para proyectos grandes y complejos.

```Buildroot```: Es una herramienta simple y ligera para generar sistemas Linux. sirven para crear ese sistema operativo a la medida. Es más fácil de usar y más rápido de compilar que Yocto


## Diferencia entre Raspbian vs Yocto/Buildroot:
* Un Linux embebido puro solo hace una tarea específica.
* No apt install. En sistemas hechos con Buildroot o Yocto, el sistema es fijo y no se cambia fácilmente una vez instalado.
* Un Linux embebido puro pesa pocos megabytes porque solo incluye lo estrictamente necesario para su hardware.

nota: 
* Arduino, chips STM32 comunes o el ESP32 no soportan Linux embebido. El estándar para ESP32 es FreeRTOS
* Linux embebido requiere mínimo: 8 MB a 16 MB de RAM para arrancar y una unidad MMU (Memory Management Unit)

<br>

# Diferencia entre un Entorno (IDE) y un Sistema Operativo (RTOS):
```El Software de Desarrollo (IDE / Compilador)```: Es tu caja de herramientas y el taller donde trabajas (ej. STM32CubeIDE, VS Code + PlatformIO, Arduino IDE, Keil uVision).

```FreeRTOS```: Es como los planos de organización de la casa. Es una librería de software opcional que le enseña al microcontrolador a hacer "multitarea" de forma eficiente

## ¿Cómo entra FreeRTOS en el juego?
Si usas el software oficial STM32CubeIDE, la ventaja es que viene con un configurador visual (STM32CubeMX) que te permite activar FreeRTOS marcando una casilla, y el programa escribe la estructura inicial por ti. Si usas VS Code, simplemente descargas la librería de FreeRTOS y la incluyes en tu código con un #include "FreeRTOS.h".

<br>

# STM32 family of 32-bit microcontrollers (MCUs)

Boards: https://stm32-base.org/boards/

La familia STM32 actualmente consta de quince series. Estas series se agrupan en cuatro categorías diferentes: Alto Rendimiento , Uso General , Ultrabajo Consumo e Inalámbricas . La siguiente lista describe lo mas comunes:

```STM32F1```: Placa "Blue Pill" (Uso general) Cuesta una fracción de una placa Nucleo. Requiere un programador externo (ST-LINK V2 dongle). Además, el mercado está inundado de chips clones/falsos. STM32 F103C8T6 

```STM32F4```: (Alto Rendimiento)
1. Son el estándar educativo actual.(Placas NUCLEO) STM32 F407VET (no encuentro) / STM32 F405RGT6 
2. Programador integrado: No necesitas comprar herramientas externas; incluye el programador ST-LINK en la misma placa. Solo requieres un cable USB.
3. Poder equilibrado: Su núcleo ARM Cortex-M4 tiene suficiente memoria y velocidad para que no te preocupes por optimizar el código al inicio.
4. Compatibilidad: Sus pines son compatibles con los shields de Arduino, facilitando conectar sensores básicos.
5. Soporte de software: Es la familia con más tutoriales, videos y ejemplos disponibles en internet utilizando el software oficial STM32CubeIDE.

```STM32G4/G0```: (modelo convencional/Ubicación principal) Son los reemplazos modernos de la serie F1/F4. Son excelentes, pero tienen menos tutoriales para principiantes.

```STM32H7```: (de alto rendimiento) Es demasiado compleja. Tiene tanta potencia y opciones de configuración que abrumará a quien empieza desde cero.


## Development boards
STMicroelectronics ofrece tres gamas diferentes de placas de desarrollo:
* ```Nucleo boards```: Estas placas son muy similares a las placas Arduino. Solo incluyen el microcontrolador y un depurador ST-Link integrado. Hay tres formatos disponibles.
* ```Discovery kits```: Estas placas contienen dispositivos de entrada y salida, además del microcontrolador. También incluyen un depurador ST-Link integrado.
* ```Evaluation boards```: Estas placas son muy completas e incluyen muchos dispositivos e interfaces adicionales, además del microcontrolador.

<br>

# Entornos de desarrollo integrados (IDE)

* ```Arm Keil MDK``` - Gratuito para las series STM32G0, STM32F0 y STM32L0 (Windows)
* ```Entorno de desarrollo integrado (IDE) PlatformIO``` - Gratuito (Windows, Linux, macOS)
* ```STM32CubeIDE``` - Gratuito (Windows, Linux, macOS)El entorno de desarrollo gratuito basado en Eclipse donde escribirás tu código en C utilizando las librerías HAL (Hardware Abstraction Layer), las cuales simplifican enormemente el control del chip.
* ```STM32CubeMX```: Herramienta gráfica oficial para configurar los pines, relojes y periféricos con un par de clics.
* ```Segger Embedded Studio``` - Gratuito para uso no comercial (Windows, Linux, macOS)
* ```SW4STM32``` - Gratuito (Windows, Linux, macOS)

## Platforms
* ```STM32duino```: Esta plataforma implementa la conocida API de Arduino para microcontroladores STM32. Se puede usar con el IDE de Arduino .

mas información: https://stm32-base.org/guides/getting-started.html



<br>
<br>


# Hardware STM32 

## Programación boot loader
ICSP, JTAG y SWD no son el mismo puerto, aunque todos sirven para el mismo propósito general; programar y depurar microcontroladores directamente en la placa base.
ICSP, JTAG y SWD se pueden usar perfectamente con Tag-Connect.ICSP, JTAG y SWD son los "idiomas" (protocolos) de comunicación, mientras que Tag-Connect es el "puerto físico"

Nota: el SWD puede ser un micro USB

## ¿Cómo se conectan con ICSP, JTAG y SWD?
* Para SWD (2 a 4 señales): Se suele utilizar el cable de 6 pines (Tag-connect modelo TC2030). Es ultra pequeño y basta para llevar las líneas de reloj, datos, alimentación y reinicio.
* Para ICSP (5 a 6 señales): También utiliza la versión de 6 pines (Tag-connect TC2030). Existen cables específicos que en el extremo del programador terminan listos para conectarse directamente a un PICKit de Microchip.
* Para JTAG (4 a 10 señales): Requiere la versión de 10 pines (Tag-connect modelo TC2050) o superiores debido a que JTAG exige más líneas de datos. El extremo del programador suele terminar en un conector compatible con depuradores profesionales como el Segger J-Link o el ST-Link.

## Tag-connect para ESP32, Raspberry y otros TC2030-USB
USB A connector to a TC2030 6-pin Plug-of-Nails™ “With Legs” connector. https://www.tag-connect.com/product/tc2030-usb

## Diferencia entre USBasp ISP & ST-Linkv2?
La principal diferencia entre el USBasp ISP y el ST-Link v2 es la familia de microcontroladores que programan: el USBasp ISP está diseñado exclusivamente para chips AVR de Atmel/Microchip (como el ATmega328P), mientras que el ST-Link v2 se usa para chips STM32 (ARM Cortex-M) y STM8 de STMicroelectronics. Además, el ST-Link v2 permite depuración en vivo (debugging) paso a paso, una función de la que carece el USBasp tradicional.


***USBasp ISP***
* Propósito principal: Grabar bootloaders o firmware directamente en la memoria flash de microcontroladores AVR.
* Interfaz de conexión: Utiliza pines de programación serial ISP (MOSI, MISO, SCK, RESET).
* Limitación: Es solo un programador; no puedes pausar la ejecución del código ni revisar variables dentro del chip mientras funciona.

***ST-Link v2***
* Propósito principal: Programar y depurar sistemas avanzados basados en arquitecturas ARM y de 8 bits de ST.
* Interfaz de conexión: Usa protocolos modernos como SWD (Serial Wire Debug) de pocos pines (SWDIO, SWCLK) o SWIM.
* Ventaja clave: Permite hacer debugging completo (poner puntos de ruptura o breakpoints, inspeccionar registros y memoria en tiempo real).
Driver: https://www.st.com/en/development-tools/stsw-link009.html#
Software: https://www.st.com/en/development-tools/st-link-v2.html


<br>
<br>




# Comparativa Tecnológica: STM32 vs ESP32 vs Raspberry Pi

La elección de la tecnología depende del **equilibrio entre potencia, consumo de energía y costo** que requiera tu proyecto.


## STM32 (Microcontrolador Industrial)
Ideal para control de hardware preciso, bajo consumo y aplicaciones industriales en tiempo real.

### Ventajas
* **Tiempo real:** Ejecución de código ultra precisa y sin retrasos de sistema operativo.
* **Bajo consumo:** Modos de ahorro de energía extremadamente eficientes (ideal para baterías).
* **Variedad:** Cientos de modelos con hardware específico para cada necesidad.
* **Fiabilidad:** Diseñado para resistir entornos industriales exigentes.

### Desventajas
* **Curva de aprendizaje:** Programación compleja que requiere entender la arquitectura de hardware.
* **Sin conectividad nativa:** La mayoría de los modelos no incluyen Wi-Fi ni Bluetooth.
* **Costo de desarrollo:** Las herramientas avanzadas y el tiempo de diseño suelen ser mayores.


## ESP32 (El Rey del IoT)
Ideal para dispositivos conectados a internet, hogares inteligentes y prototipos de bajo costo.

### Ventajas
* **Conectividad:** Wi-Fi y Bluetooth integrados de fábrica.
* **Costo:** Precio extremadamente bajo para las funciones que ofrece.
* **Doble núcleo:** Permite separar las tareas de comunicación de las tareas de control.
* **Comunidad:** Gran compatibilidad con el entorno de Arduino y miles de librerías.

### Desventajas
* **Consumo intermedio:** Consume mucha más energía que un STM32 cuando el Wi-Fi está activo.
* **Menos pines:** Menor cantidad de pines GPIO en comparación con chips STM32 grandes.
* **Conversor ADC básico:** Los lectores analógicos integrados son poco lineales y menos precisos.



## Raspberry Pi (SBC - Computadora de Placa Única)
Ideal para procesamiento de datos pesados, interfaces gráficas, inteligencia artificial local y servidores.
*(Nota: Se excluye la Raspberry Pi Pico, que entra en la categoría de microcontroladores).*

### Ventajas
* **Sistema Operativo:** Corre Linux completo, permitiendo multitarea real.
* **Poder de cómputo:** Capacidad para procesar video, bases de datos y algoritmos pesados.
* **Lenguajes avanzados:** Puedes programar en Python, C++, Node.js, Java, etc.
* **Periféricos de PC:** Salida HDMI, puertos USB, Ethernet y soporte para cámaras de alta resolución.

### Desventajas
* **Consumo alto:** Requiere alimentación constante de pared; no es viable para usar con baterías pequeñas.
* **No es tiempo real:** Linux puede retrasar milisegundos el control crítico de un pin.
* **Arranque lento:** Tarda segundos o minutos en encender, a diferencia de los microcontroladores que son instantáneos.
* **Precio:** Es significativamente más cara que las otras dos opciones.



## ¿Cómo elegir qué tecnología usar?

Hazte las siguientes preguntas para descartar opciones:

1. **¿Tu proyecto necesita procesar imágenes, bases de datos locales o una interfaz gráfica compleja?**
   * **Sí:** Elige **Raspberry Pi**.
   * **No:** Pasa a la siguiente pregunta.

2. **¿El dispositivo necesita enviar datos por Wi-Fi o conectarse por Bluetooth?**
   * **Sí:** Elige **ESP32** (es la opción más rápida y económica).
   * **No:** Pasa a la siguiente pregunta.

3. **¿El sistema funciona con baterías por meses, requiere control de motores de alta precisión o es para uso industrial?**
   * **Sí:** Elige **STM32**.
   * **No:** Si es un proyecto general o educativo, **ESP32** sigue siendo la opción más versátil y fácil de implementar.

<br>
<br>



# Simulation & Testing Automation Tools

## Metodologías de prueba usadas en sistemas embebidos para producción en masa
* ```Software-in-the-Loop (SIL)```: Prueba el código de control dentro de un entorno virtual o computadora, sin usar el hardware final.
* ```Hardware-in-the-Loop (HIL)```: Prueba la integración conectando el hardware físico real (como una unidad de control electrónico) a un simulador en tiempo real.
* ```Firmware CI/CD Pipeline```: El término general más usado. Indica la integración y entrega continua de código para microcontroladores.
* ```Hardware-in-the-Loop (HIL) Testing Pipeline```: Crucial para IoT. Significa que el flujo automatizado carga el código y lo prueba directamente en tarjetas físicas reales conectadas a una computadora.
* ```Firmware Compilation & Toolchain Pipeline```: Automatiza la compilación cruzada usando herramientas como GCC, Arm Compiler o Keil.
* ```Static Code Analysis Pipeline```: Flujo dedicado a la revisión de calidad y seguridad del código C/C++ antes de compilar (usando herramientas como Misra C, SonarQube o Coverity).
* ```IoT Data Pipeline```: El flujo que recibe, limpia y procesa los datos enviados por los sensores del dispositivo hacia la nube.
* ```OTA (Over-the-Air) Deployment Pipeline```: El sistema automatizado que empaqueta, firma digitalmente con seguridad y distribuye las actualizaciones de firmware a miles de dispositivos conectados.
* ```Device Provisioning Pipeline```: Flujo automático para registrar, dar de alta y autenticar nuevos dispositivos IoT en la base de datos de forma segura.


## Embedded CI/CD pipeline (DevOps)
```Pipeline CI/CD -DevOps- (Integración Continua y Entrega/Despliegue Continuo)```:  es una serie de pasos automatizados que ayuda a los equipos de desarrollo de software a entregar código de forma más rápida, segura y fiable. Las canalizaciones son una parte esencial de la integración continua y la entrega continua (CI/CD) y resultan fundamentales para el desarrollo de software moderno.

```Pipeline (tubería o flujo)```: es una cadena de pasos automáticos.

```Integración Continua (CI)```: Junta el código nuevo de varios programadores y pasa pruebas automáticas para detectar errores rápido.

```Entrega/Despliegue Continuo (CD)```: Prepara y envía el código ya probado hacia los servidores reales para que los usuarios lo usen.<br>
nota: lo usan los DevOps o desarrolladores. herramientas populares como GitHub Actions o Jenkins.

## Pipeline con HIL(Hardware-in-the-Loop) en Hardware
Un pipeline con HIL automatiza lo siguiente:
1. Subes tu código a GitHub o GitLab.
2. El pipeline compila el código automáticamente.
3. El pipeline "inyecta" el binario (flashea) a una tarjeta de desarrollo real (un ESP32, STM32, etc.) que está físicamente conectada a un servidor en la oficina o laboratorio.
4. Un equipo de prueba simula estímulos eléctricos (como falsos datos de sensores o caídas de voltaje) instalados en los pines del chip.
5. El pipeline evalúa si el hardware real respondió correctamente y aprueba o rechaza el código.

<br>

```¿Para que es importante para un ingeniero?```<br>
Reduce costos: Probar el firmware en hardware de forma automatizada evita tener que reparar miles de dispositivos ya vendidos o instalados en el campo.
Agilidad: Permite hacer pruebas de estrés (como desconectar la energía a mitad de un proceso) miles de veces por noche sin intervención humana.
Madurez técnica: Un ingeniero que sabe integrar pipelines HIL demuestra que entiende tanto el desarrollo de software moderno como las limitaciones físicas del hardware.

Framework para HIL:
* ```Robot Framework```
* ```Python con Pytest``` es un framework de pruebas nativo de Python, te permite interactuar fácilmente con instrumentos de laboratorio, puertos seriales y herramientas de flasheo. En un pipeline HIL, Python actúa como el "orquestador" que manipula el entorno para probar el chip real.

```¿Cómo funciona la arquitectura HIL con Pytest?```<br>
En este flujo, tu computadora o servidor de CI/CD ejecuta el script de Pytest, el cual se comunica con el hardware a través de tres capas:
1. ```Estímulo (Entradas)```: Pytest controla herramientas para enviar señales al chip (ej. activar un relé, usar un generador de señales o enviar comandos por bus CAN/I2C).

2. ```Monitoreo (Salidas)```: El microcontrolador ejecuta su firmware y reporta su estado. Pytest lee esta respuesta a través de UART (Puerto Serie), logs de consola o instrumentación.

3. ```Verificación (Asserts)```: Pytest compara la respuesta real del hardware contra el resultado esperado.

## Fixtures de Pytest clave para HIL:
- Setup de Hardware:
- Teardown de Hardware:

## Herramienta de flasheo automática:  
```J-Link```: hardware debug probes used by embedded developers to program and debug microcontrollers. usa poerto JTAG / SWD
```esptool```: ????????????????

```El debugging (depuración)```: En sistemas embebidos es diferente y más complejo: necesitas meterte directo al silicio del chip para ver qué está pasando en los registros de memoria y el hardware real, muchas veces mientras el dispositivo sigue funcionando. En el mundo moderno de LinkedIn y pipelines avanzados, el debugging se divide en dos enfoques: 
1. ```debugging manual en tu escritorio```: localmente en el dispositivo.
	* ```Protocolos de Hardware (JTAG / SWD)```: conectores y líneas físicas que permiten pausar el procesador, leer la RAM y avanzar línea por línea de 
	* ```Depuradores Físicos (Hardware Debuggers)```: Dispositivos como J-Link (Segger) o ST-LINK (STMicroelectronics). Se conectan por USB a tu PC y por 	JTAG/SWD a tu tarjeta objetivo código.
	* ```Herramientas de Software (GDB, Ozone, STM32CubeIDE)```: GDB (GNU Debugger) es el motor estándar. Interfaces como Ozone de Segger te permiten ver 	variables en tiempo real, gráficos de consumo de memoria y registros del procesador sin detener el chip.

2.  ```debugging automatizado en el pipeline (El Debugging Moderno: "Post-Mortem" y en Pipelines)```: Cuando escalas la producción o usas un pipeline de CI/CD, no puedes conectar un J-Link manualmente para ver qué falló. Ahí entra el debugging automatizado:
	* ```Análisis de Volcado de Memoria (Core Dumps / Hard Fault Handlers ```: ???????????
	* ```RTT (Real-Time Transfer) de Segger```: Es un reemplazo moderno del clásico printf. Permite enviar logs desde el chip a la PC a través del J-Link a 	velocidades extremas y sin alterar los tiempos físicos del microcontrolador
	* ```Trace (Rastreo de Instrucciones)```: Captura el historial exacto de las últimas miles de instrucciones

## Herramientas de debugging:
* ```Analizador Lógico Saleae```: es el estándar de la industria debido a su software intuitivo.
* ```Osciloscopio```: puedes descartar Glitches y Ruido, el osciloscopio te mostrará la caída de voltaje exacta que provoca el Brownout Reset (reinicio por bajo voltaje) del chip.


<br>

---

<div>
  <p>
    <img  align="top" width="42" style="padding:0px 0px 0px 0px;" src="./img/carjavi.png"/> Copyright &nbsp;&copy; 2023 Instinto Digital <a href="https://carjavi.github.io/" title="carjavi.github">carjavi</a>
  </p>
</div>

<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="./img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>
