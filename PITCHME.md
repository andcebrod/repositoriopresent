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
