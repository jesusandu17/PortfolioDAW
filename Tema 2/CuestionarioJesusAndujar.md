# Cuestionario de servidores web

Autor: Jesús Andújar Fernández

## 1. ¿Qué significa las siglas HTTP y para qué se utiliza?

HTTP significa Protocolo de Transferencia de Hipertexto. Sirve para ver páginas web en Internet.

## 2. ¿En qué puerto funciona normalmente el protocolo HTTP?

HTTP funciona normalmente en el puerto 80.

## 3. ¿Cuál es la diferencia principal entre HTTP y HTTPS?

HTTP envía la información sin cifrar. HTTPS la protege para que sea más segura.

## 4. ¿Qué función cumple el servidor web Apache dentro de una arquitectura web?

Apache es un programa que permite mostrar páginas web a quienes entran desde su navegador.

## 5. ¿Cómo puedes comprobar si el servicio de Apache está activo en un sistema Ubuntu?

En la terminal escribimos: sudo systemctl status apache2

## 6. Explica brevemente en qué consiste una arquitectura cliente-servidor.

El cliente, como nuestro ordenador, pide información y el servidor se la envía.

## 7. ¿Qué diferencia hay entre una arquitectura de dos capas y una de tres capas en entornos web?

La de dos capas tiene cliente y servidor. La de tres separa la presentación, la aplicación y los datos.

## 8. ¿Qué es el protocolo FTP y para qué se usa?

Es un protocolo que sirve para enviar y recibir archivos entre un ordenador y un servidor.

## 9. Menciona un ejemplo de cliente FTP y un ejemplo de servidor FTP.

Un cliente FTP es FileZilla y un servidor FTP es vsftpd.

## 10. ¿Qué diferencia existe entre FTP y SFTP?

FTP no cifra la información. SFTP envía los archivos de manera segura y protegida.

## 11. Indica tres tipos de alojamiento web y explica brevemente en qué se diferencian.

Compartido: varias webs comparten servidor.

VPS: tienes recursos propios.

Dedicado: tienes un servidor entero.

## 12. ¿Qué ventajas ofrece un servidor VPS frente a un alojamiento compartido?

Un VPS ofrece más control, recursos propios y normalmente mejor rendimiento.

## 13. Describe brevemente los componentes principales de una arquitectura web moderna.

Son el navegador, el servidor web, el servidor de aplicaciones y la base de datos.

## 14. ¿Qué papel cumple el servidor de aplicaciones dentro de dicha arquitectura?

Se encarga de realizar tareas de la web, como comprobar usuarios o gestionar pedidos.

## 15. ¿Qué software o paquete puedes usar para instalar Apache fácilmente en Windows?

XAMPP, que permite instalar Apache, PHP y una base de datos fácilmente.

## 16. ¿Qué carpeta suele contener los archivos del sitio web en una instalación de Apache en Windows (por ejemplo, con XAMPP)?

Normalmente se guardan en C:\xampp\htdocs.

## 17. Escribe el comando para instalar Apache en Ubuntu desde la terminal.

sudo apt install apache2

## 18. ¿Qué comando se usa para iniciar el servicio Apache en Ubuntu?

sudo systemctl start apache2

## 19. ¿En qué ruta se almacena normalmente la página web por defecto de Apache en Ubuntu?

Normalmente en /var/www/html.

## 20. ¿Qué es el protocolo SSH y cuál es su propósito principal?

Permite conectarse y controlar otro ordenador a distancia de forma segura.

## 21. ¿Qué comando se usa para conectarse a un servidor remoto mediante SSH?

ssh jesus@192.168.10.10

## 22. Menciona una ventaja de usar autenticación mediante claves SSH frente a contraseñas.

Es más segura porque las claves son mucho más difíciles de adivinar que una contraseña.
