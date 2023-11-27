---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Funcionamiento y advertencia legal

{% hint style="danger" %}
## <mark style="color:red;">Advierto que este código está desarrollado única y exclusivamente con fines educativos, jamás intentes utilizarlo contra otro sistema sin permiso previo del propietario.</mark>

##

## <mark style="color:red;">Asegúrate también de utilizarlo en un entorno seguro, como por ejemplo una máquina virtual desechable.</mark>&#x20;

##

## <mark style="color:red;">El uso de ransomware en España puede conllevar penas de hasta seis años de prisión, según el Código Penal.</mark>
{% endhint %}

##

## Funcionamiento

En la siguiente sección está el código con comentarios detallados de su funcionamiento, pero para facilitar su comprensión aquí hay un breve resumen a vista general de como funciona:

1. Se generan 2 claves asimétricas RSA en tu máquina atacante, una publica "public.pem" y una privada "private.pem".
2. Se realiza ingeniería social para engañar a la víctima a descargar el ransomware junto a la "public.pem" y el desencriptador, por ejemplo haciéndolo pasar por un videojuego pirata y ocultando estos archivos bajo accesos directos.
3. Una vez se ejecuta, este recorrerá todo el directorio de Usuarios en el disco "C:" guardando en una variable las direcciones de todos los archivos que tengan las extensiones indicadas, por ejemplo ".pdf", ".jpg", ".mp4", etc.
4. A continuación generará una llave simétrica AES aleatoria y encriptará todos los archivos de la lista con ella, después guardará la llave en un archivo.
5. Hasta aquí todo era reversible, la victima dispone de la llave en texto claro, sin embargo el siguiente paso será encriptar el archivo que contiene la llave simétrica con la llave de criptografía asimétrica, es decir utilizando la llave "public.pem" que hemos enviado.
6. Ahora la victima está atrapada, no puede acceder a la llave con la que se han encriptado sus archivos a menos que disponga de la clave privada que desencripte el archivo que ha encriptado la clave pública. La duración del proceso dependerá de la cantidad de archivos que tenga que recorrer el ransomware, pero al utilizar una llave simétrica en lugar de asimétrica para estos, debería ser cuestión de segundos.
7. Una vez realizado el ataque se creará en su escritorio una nota de rescate con las instrucciones a seguir y el método de pago, también se cambiará su fondo de pantalla para generar presión psicológica.
8. Una vez la víctima ha hecho el pago y lo ha comunicado mediante un servicio de correos privado, se envía el archivo "private.pem", se ejecuta el desencriptador en el mismo directorio de la llave y los datos se restaurarán.
