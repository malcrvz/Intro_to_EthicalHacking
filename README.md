# Introducción y marco teórico

## Resumen del proyecto

Este proyecto de síntesis une las dos asignaturas que más disfruto, Seguridad y Sistemas.

La idea principal es realizar una auditoría de seguridad básica con herramientas automatizadas, manuales y un [SO](broken-reference) totalmente personalizable para dar mis primeros pasos en el trabajo de pentester.

Para empezar instalaré en hardware, en mi portátil personal, la distribución de GNU/Linux: Arch Linux. Esta distribución está considerada una de las más difíciles de usar ya que el instalador viene con lo mínimo necesario para arrancar el sistema, es el usuario el que deberá mediante consola de comandos escoger e instalar todas las funciones que necesite, desde el "Network manager" hasta el controlador de sonido o incluso la interfaz gráfica(si es que la desea) por lo que es un trabajo laborioso y muy meticuloso, que requiere muchas horas de consultar guías y tutoriales, pero que vale la pena por el resultado.&#x20;

Una vez instalado Arch, instalaré en él la máquina virtual de Metasploitable2™, qué viene preparada expresamente con cientos de vulnerabilidades para que el usuario pueda practicar sobre ellas el uso de herramientas de pentesting e intentaré vulnerarla de la mayor cantidad de maneras posibles mientras ofrezco una explicación del proceso y las herramientas usadas. \
Para ello utilizaré otra máquina virtual de Kali Linux que nos facilita todas las herramientas necesarias, aunque si el lector lo desea puede instalar estas mismas herramientas en Arch Linux y utilizarlas sin problema.

Explicaré más a fondo qué son los proyectos Arch Linux, Metasploitable y Kali Linux en siguientes entradas.

Una vez esté todo preparado utilizaré el framework de Metasploit para automatizar un ataque contra Metasploitable, aprovechando una vulnerabilidad.

El siguiente apartado consistirá en una explicación de que es SQL y el ataque de inyección SQL y demostrar cómo funciona de manera manual y sus riesgos, utilizando para ello la aplicación web vulnerable "DVWA", con el mismo funcionamiento y objetivos que Metasploitable, que además viene incluida en este.

También añado una inyección de comandos para obtener una reverse shell de un servidor con un código no sanitizado que nos presta un servicio de pings.

Una vez terminados los apartados que utilizan Metasploitable, intentaré llegar lo más lejos posible en programación python realizando cursos online y crearé un ransomware que utiliza cifrado simétrico y asimétrico, realizando una demostración de como se fabrica malware, como funciona contra un SO Windows10 y mostrando su código paso a paso en la presentación final del proyecto.

***

## Objetivos y motivos

* A fecha de 2022, mi objetivo a largo plazo es dedicarme profesionalmente a la ciberseguridad, más concretamente a la rama de auditorias pentesting o también llamado red-teaming. La ciberseguridad es el campo de la informática que más me apasiona por lo que este proyecto que me da la libertad para practicar y explorar el tema a mi ritmo me motiva a llegar lo más lejos posible y aprovechar la oportunidad para "adelantar" temario mientras curso el grado medio.
* Dada la dificultad de la instalación de Arch y la cantidad de errores que surgirán y tendré que corregir, me parece un buen proyecto para aprender a administrar sistemas Linux de una manera práctica y divertida.
* Metasploitable™ es un laboratorio de aprendizaje legal y muy fácil de utilizar que me garantiza que podré poner en práctica conocimientos y así asimilarlos para poder aplicarlos en la vida real a diferencia de simplemente leer cientos de horas de teoría que no me harán retener la información de una manera tan efectiva y además divertida.
* DVWA me introduce al mundo de la seguridad de aplicaciones web, uno de los más demandados y necesarios hoy en día.
* Python es conocido por ser el lenguaje de programación ideal para iniciarse, debido a su facilidad de lectura y capacidades, es por eso que es uno de los más utilizados en el mundo de la ciberseguridad y aprenderlo marca la diferencia entre un aficionado y un profesional que es capaz de fabricar sus propias herramientas o entender como funcionan las de terceros para modificarlas a su antojo.
* Los ataques Ransomware son uno de los más devastadores y comunes que existen, entender como funcionan y como se desarrollan es esencial para aprender a evitarlos y mitigarlos.

***

## Materiales y software utilizado

* Arch Linux: es una distribución de Linux que viene prácticamente vacía, con lo justo para arrancar el sistema, hay que configurar desde el wifi a la interfaz gráfica. Explico más detallado  en [¿Qué es Arch Linux?](broken-reference)
* Metasploitable™: es una distribución de Linux, que a propósito viene configurada con decenas de vulnerabilidades, es una herramienta de aprendizaje para poder practicar técnicas de hacking en un entorno legal y seguro.
* DVWA: incluida en Metasploitable, es una aplicación web vulnerable con el mismo propósito que Metasploitable.
* Metasploit framework: es una herramienta de automatización hacking que despliega una base de datos llena de exploits y payloads listos para usarse contra un objetivo de una manera relativamente sencilla.
* Visual Studio Code (VSCode) es un editor de código fuente desarrollado por Microsoft, gratuito y de código abierto. Es compatible con múltiples lenguajes de programación y plataformas, lo utilizaré para desarrollar python.
* Kali Linux es el sistema operativo por excelencia en el ámbito de las auditorias, aunque haya otras buenas opciones como ParrotOS o BlackArch he escogido Kali por la familiaridad que ya tengo con él.
* Gitbook: escribiré el proyecto en esta aplicación web Gitbook de Github, que me permite almacenar el proyecto en la nube y editar desde clase y desde mi casa, además de estar fácilmente organizado en categorías. Además me permitirá compartir el enlace con los alumnos que estén interesados en el tutorial.
* Portátil personal: utilizaré mi portátil personal para el proyecto.

***

## Implicaciones técnicas y conocimiento requerido

* Debo entender primero cómo funciona un sistema GNU/Linux en profundidad para poder instalarlo sin una interfaz gráfica, además de resolver la enorme cantidad de problemas que vayan surgiendo por el camino en una distribución avanzada como es Arch Linux. Explicaré los errores más relevantes en la página de [Errores comunes](broken-reference)
* Debo saber usar con facilidad y ligereza la herramienta Metasploit que implica conocimientos de redes, ciberseguridad, código, ingeniería de software y en general conocimientos de seguridad informática.
* Debo utilizar cursos gratuitos y de pago para adquirir los conocimientos necesarios ya que la mayoría del temario que necesito no lo damos en la escuela. Utilizaré plataformas como Youtube, HackTheBox, Mastermind, ArchWiki además de búsquedas generales en Google y ChatGPT4.
* Debo aprender SQL para aprender que hace que un código sea malicioso o no y para entender como funciona el ataque de inyección SQL.
* Debo aprender Python al menos a un nivel básico para poder fabricar el ransomware, hacer modificaciones y entender como funciona.
