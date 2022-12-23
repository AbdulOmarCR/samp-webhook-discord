Filterscript para enviar webhook a discord fácilmente desde SAMP.

Este filterscript es gratuito, ```PROHIBIDO vender```.

Descarga el archivo compilado, ponlo en tu carpeta ```filterscripts``` y en tu server.cfg añade  ```discord_api``` en la línea  ```filterscripts```


Para enviar un mensaje a discord usa:
```c
CallRemoteFunction("MensajeDiscord", "ssss", "Titulo", "Cuerpo del mensaje", "Link del webhook", "Nombre del servidor");
```
Puedes poner este define arriba en tu GM:
```c
#define		MensajeDiscord(%0,%1,%2,%3)		CallRemoteFunction("MensajeDiscord", "ssss",%0,%1,%2,%3)

```
Con este define podrás enviar mensajes a discord con una syntaxis mucho más familiar:
```c
MensajeDiscord("Titulo", "Cuerpo del mensaje", WEBHOOK_CANAL_DUDAS, "Nombre server");
```

En el link del webhook no insertar el enlace completo, solamente usa los parámetros necesarios, por ejemplo:
Si el webhook es: ```https://discord.com/api/webhooks/1517583558423195121/Xft8uhfaYp4QzWzxrxG_hvPvpWq6fuQBzpg40zKQwiLN3SYur9OeKWyJbq21At6Y```
Solo debes usar esta parte:  ```1517583558423195121/Xft8uhfaYp4QzWzxrxG_hvPvpWq6fuQBzpg40zKQwiLN3SYur9OeKWyJbq21At6Y ```


Puedes usar varios webhooks y usar el mismo nombre del servidor fácilmente definiendolos, por ejemplo:
 ```c
#define		MensajeDiscord(%0,%1,%2,%3)		CallRemoteFunction("MensajeDiscord", "ssss",%0,%1,%2,%3)
#define WEBHOOK_CANAL_DUDAS "1517583558423195121/Xft8uhfaYp4QzWzxrxG_hvPvpWq6fuQBzpg40zKQwiLN3SYur9OeKWyJbq21At6Y"
#define SERVER_NAME "Mi gran servidor RP"

//Entonces llamarías la función así:
MensajeDiscord("Titulo", "Cuerpo del mensaje", WEBHOOK_CANAL_DUDAS, SERVER_NAME);
 ```

