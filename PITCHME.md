# HTTP

- Presentación del Protocolo HTTP
- Creada por Andrés Ceballos Rodríguez

---

## Indice

- Características del protocolo HTTP
- Típica Sesión HTTP
- Cabeceras protocolo HTTP
- Peticiones HTTP
- Respuestas HTTP
- Cookies
- Evolución de HTTP
- Características de HTTP 2.0

---

## Caracteristicas del protocolo HTTP
- Nos permite realizar una petición de datos y recursos, como pueden ser documentos HTML. Es la base de cualquier intercambio de datos en la Web, y un protocolo de estructura cliente-servidor.

---

### HTTP es sencillo
- HTTP esta pensado y desarrollado para ser leído y fácilmente interpretado por las personas, haciendo de esta manera más facil la depuración de errores, y reduciendo la curva de aprendizaje para las personan que empieza a trabajar con él.

---

### HTTP es extensible
- las cabeceras de HTTP, han hecho que este protocolo sea fácil de ampliar y de experimentar con él.
- Funcionalidades nuevas pueden desarrollarse, sin más que un cliente y su servidor, comprendan la misma semántica sobre las cabeceras de HTTP.

---

### HTTP es un protocolo con sesiones, pero sin estados
- HTTP es un protocolo sin estado, es decir: no guarda ningún dato entre dos peticiones en la mísma sesión.
- El uso de cookies permite guardar datos con respecto a la sesión de comunicación. Usando la capacidad de ampliación del protocolo HTTP.
- las cookies permiten crear un contexto común para cada sesión de comunicación.

---

### HTTP y conexiones

- HTTP no necesita que el protocolo que lo sustenta mantenga una conexión continua entre los participantes en la comunicación, solamente necesita que sea un protocolo fiable o que no pierda mensajes.
- HTTP se apoya en el uso del protocolo TPC, que está orientado a conexión, aunque una conexión continua no es necesaria siempre.

---

## Típica Sesión HTTP
- Una sesión en el protocolo HTTP consta de 3 fases:
  *  El cliente establece una conexión TCP
  * El cliente manda su petición, y espera por la respuesta.
  * El servidor procesa la petición, y responde con un código de estado y los datos correspondientes.

---
### Estableciendo una conexión

- En el protocolo http es siempre el cliente el que establece la conexión.
- El puerto por defecto para un servidor HTTP es el puerto 80.
- La URL de la página pedida contiene tanto el nombre del dominio, como el número de puerto, aunque este puede ser omitido, si se trata del puerto 80.

---

### Mandando una petición

- Una vez la conexión está establecida, el cliente, puede mandar una petición de datos.
- La  petición de datos de un cliente HTTP, consiste en directivas de texto, separadas mediante CRLF

---

### Respuesta del Servidor

- Después de que el agente de usuario envía su petición, el servidor web lo procesa, y a continuación responde.
- De forma similar a la petición del servidor, la respuesta del servidor está formada por directivas de texto, separadas por el carácter CRLF, y divida en tres bloques.

---

## Cabeceras protocolo HTTP

- Los encabezados HTTP permiten que el cliente y el servidor pasen información adicional con la solicitud o la respuesta.
- Un encabezado de solicitud consiste en su nombre insensible a mayúsculas y minúsculas seguido de dos puntos ' :'.

---

  * Encabezado general : Encabezados que se aplican tanto a las solicitudes como a las respuestas, pero sin relación con los datos que finalmente se transmiten en el cuerpo.
  * Encabezado de solicitud : encabezados que contienen más información sobre el recurso que se va a buscar o sobre el propio cliente.
  * Encabezado de respuesta : Encabezados con información adicional sobre la respuesta.
  * Encabezado de entidad : Encabezados que contienen más información sobre el cuerpo de la entidad.

---

## Peticiones http

- La primera parte, consiste en una linea, que contiene un método, seguido de sus parámetros:
  * la dirección del documento pedido: por ejemplo su URL completa, sin indicar el protocolo o el nombre del dominio.
  * la versión del protocolo HTTP
- La siguiente parte, está formada por un bloque de líneas consecutivas que representan las cabeceras de la petición HTTP y dan información al servidor sobre que tipo de datos es apropiado u otros datos que modifiquen su comportamiento.
- La parte final es un bloque de datos opcional, que puede contener más datos para ser usados por el método POST.

---

### Ejemplo de peticiones :

GET / HTTP/1.1 <br>
Host: www.google.com <br>
Accept-Language: en <br>

---

### Metodos de peticiones

- La peticiones más comunes son  GET y POST:
 * El método GET hace una petición de un recurso específico. Las peticiones con GET unicamente hacen peticiones de datos.
 * El método POST envía datos al servidor de manera que este pueda cambiar su estado. Este es el método usado normalmente para enviar los datos de un  formulario HTML.

---

## Respuesta http

- La primera línea, es la línea de estado, que consiste en una confirmación del la versión de HTTP utilizado, y seguido por el estado de la petición.
- Las líneas siguientes representan cabeceras de HTTP concretas, dando al cliente información sobre los datos enviado.
  * Al igual que las cabeceras HTTP de la petición de un cliente, las cabeceras HTTP del servidor, finalizan con una línea vacía.
- El bloque final, es el bloque que puede contener opcionalmente los datos.

---

### Ejemplo de respuesta:

HTTP/1.1 200 OK <br>
Date: Mon, 12 Dec 2017 15:48:00 GMT <br>
Server: Apache <br>
Last-Modified: Tue, 01 Dec 2017 20:18:22 GMT <br>
ETag: "78132bs1-7449-465bk75b28v17" <br>
Accept-Ranges: bytes <br>
Content-Length: 30218 <br>
Content-Type: text/html <br>
<!DOCTYPE html... <br>

---

## Cookies

- Una cookie HTTP, cookie web o cookie de navegador es una pequeña pieza de datos que un servidor envía a el navegador web del usuario.
- El navegador guarda estos datos y los envía de regreso junto con la nueva petición al mismo servidor.
- Se usan generalmente para decirle al servidor que dos peticiones tiene su origen en el mismo navegador web
- Las cookies permiten recordar la información de estado en vista a que el protocolo HTTP es un protocolo sin estado.

---

- Las cookies se utilizan principalmente con tres propósitos:

 * Gestión de sesiones: Inicios de sesión, carritos de compras, puntajes de juegos o cualquier otra cosa que el servidor deba recordar
 * Personalización: Preferencias de usuario, temas y otras configuraciones
 * Rastreo: Grabar y analizar el comportamiento del usuario

---

-  Existen:
  * Cookies de Sesion: se elimina cuando el cliente se cierra, sin embargo, los navegadores web pueden usar la restauración de sesiones
  * Cookies permanentes: En lugar de caducar cuando el cliente cierra, las cookies permanentes caducan en una fecha específica ( Expires) o después de un período de tiempo específico ( Max-Age).

---

## Evolución de HTTP

- HTTP es el protocolo en el que se basa la Web. Fue inventado por Tim Berners-Lee entre los años 1989-1991, HTTP ha visto muchos cambios, manteniendo la mayor parte de su simplicidad y desarrollando su flexibilidad.
- HTTP ha evolucionado, desde un protocolo destinado al intercambio de archivos en un entorno de un laboratorio semi-seguro, al actual laberinto de Internet, sirviendo ahora para el intercambio de imágenes, vídeos en alta resolución y en 3D.
---

### Invencion del Http:
- En 1989, Tim Berners-Lee escribió una propuesta para desarrollar un sistema de hipertexto sobre Internet. Desarrollado sobre los protocolos existentes TCP e IP, creo http basado en cuatro bloques:
* Un formato de texto para representar documentos de hiper-texto.
* Un protocolo sencillo para el intercambio de esos documentos, HTTP
* Un cliente que muestre esos documentos. El primer navegador Web.
* Un servidor para dar acceso a los documentos.

---

### HTTP/0.9 – El protocolo de una sola línea

- HTTP/0.9 es un protocolo extremadamente sencillo:
  * una petición consiste simplemente en una única linea, que comienza por el único método posible GET, seguido por la dirección del recurso a pedir
  * Al contrario que sus posteriores evoluciones, el protocolo HTTP/0.9 no usa cabeceras HTTP, con lo cual únicamente es posible transmitir archivos HTML, y ningún otro tipo de archivos.

---

### HTTP/1.0

- Se añade a la línea de la petición GET.
- Se envía también un código de estado al comienzo de la respuesta, permitiendo así que el navegador pueda responder al éxito o fracaso de la petición realizada, y actuar en consecuencia
- El concepto de cabeceras de HTTP
- Gracias a las cabeceras de HTTP, se pudieron transmitir otros documentos además de HTML.

---
### HTTP/1.1 – El protocolo estándar.
- HTTP/1.1 aclaró ambigüedades y añadió numerosas mejoras:
 * Una conexión podía ser reutilizada, ahorrando así el tiempo de re-abrirla.
 * El enrutamiento se añadió a la especificación, permitiendo realizar una segunda petición de datos antes de que fuera respondida la primera.
 * Se permitió que las respuestas a peticiones podían ser divididas en sub-partes.
 * Se añadieron controles adicionales a los mecanismos de gestión de la cache.
 * La negociación de contenido se añadó a la especificación, permitiendo que servidor y cliente acordasen el contenido más adecuado a intercambiarse.
 * Gracias a la cabecera, Host, pudo ser posible alojar varios dominios en la misma dirección IP.

 ---
### HTTP/2
- El protocolo HTTP/2, tiene notables diferencias fundamentales respecto a la versión anterior HTTP/1.1:
 * Es un protocolo binario. Así pues no se puede leer directamente, gracias a este cambio es posible utilizar en él técnicas de optimización.
 * Es un protocolo multiplexado. Peticiones paralelas pueden hacerse sobre la misma connexión
 * Comprime las cabeceras.
 * Permite al servidor almacenar datos en la caché del cliente, previamente a que estos sean pedidos, mediante un mecanismo denominado 'server push'.

 ---
