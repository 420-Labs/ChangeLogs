# Registro de cambios desde 0.2.0

## 🛒 [0.2.0] La actualización de la tienda

### MLNL (TL;DR)

- 🎨 Tienda de personalización rediseñada completamente
- 👤 Perfiles de usuario
- 🍎 Ratios de frutas
- ⌛ Cooldown por server
- 🔒 Sistemas de administración mejorados
- 🪴 Fertilizantes duran más tiempo
- 🌲 El ratio de crecimiento de los fertilizantes fue cambiado
- 🍎 Las frutas que consigas ahora son mostradas publicamente
- 🪲 Arreglos de Bugs

---

### 🎨 Tienda de personalización rediseñada completamente

Con esta actualización, ahora puedes ver cuatro fondos por página, lo que facilita navegar por la tienda y encontrar exactamente lo que estás buscando. Esta mejora reduce el número total de páginas de fondos de `36` a solo `9`, simplificando tu experiencia de compra.

#### Tienda 0.1.x

![Old Shop](../images/old_shop0.1.x.png)

#### Tienda 0.2.0

![New Shop](../images/new_shop0.2.0.png)

Además, debajo de cada fondo puedes ver el precio actual, o si el fondo ya fue comprado por ti u otro usuario, dirá `Comprado por <usuario>` (El usuario también puede ser reemplazado por `Treebot` para el fondo predeterminado o `Staff de TreeBot` si fue otorgado a través de comandos de administración, debido a un error o un sorteo, ¿por qué no?).

### 👤 Perfiles de Usuario

¿Alguna vez quisiste ver tu inventario sin abrir la tienda?
¡Ahora es posible con `/perfil`!
Puedes ver tu propio perfil dejando el campo `usuario` vacío o llenándolo con un usuario para ver el perfil de ese usuario. Y como sabemos que quieres mostrar esas increíbles 6 monedas que obtuviste de una fruta, puedes establecer el campo `público` en `Sí` para que otros usuarios puedan ver tu increíble progreso en el servidor y a nivel global.

Espera... ¿Progreso en el servidor?
Sí, desde la versión `0.1.0`, Treebot estaba guardando cuántas veces regaste el árbol, cuántas veces fertilizaste el árbol, cuántas veces mega fertilizaste el árbol, cuántas frutas obtuviste y el fondo que compraste. Bueno, ahora es posible verlo con `/perfil`.

![alt text](../images/profile.png)

### 🍎 Tasas de Frutas

Las Tasas de Frutas han sido implementadas, ahora, obtendrás una cantidad determinada de frutas dependiendo de la altura del árbol. Antes, siempre había una posibilidad de obtener **1** fruta, ahora tienes la posibilidad de obtener más frutas dependiendo de la altura.

*Nota: Los fertilizantes harán que las frutas tengan más probabilidades de aparecer, pero no te darán más frutas.*

### ⌛ Cooldown por Servidor

¿Alguna vez intentaste regar los árboles de dos servidores diferentes al mismo tiempo y recibiste un mensaje de cooldown? ¡Ahora puedes regar tantos árboles de servidor como desees al mismo tiempo!
*Este cambio no modifica el tiempo de cooldown, simplemente separa tu tiempo de cooldown de los otros servidores.*

### 🔒 Mejoras en los sistemas de administración

Esta no es una actualización que los usuarios puedan ver directamente, pero con esto nosotros (el Personal de TreeBot) podemos gestionar los perfiles de usuario/servidor de una manera mucho más fácil, lo que beneficiará a todos ya que el personal podrá resolver cualquier problema que los usuarios puedan tener.

### 🪴 Ahora el fertilizante dura más

Antes, el fertilizante y el mega fertilizante solo aumentaban el impulso del árbol para el próximo riego y nada más. Para ser más considerados con otros usuarios, el impulso del árbol se reducirá un 10% con cada riego, así que, si mi árbol tiene un impulso del 30%, durará 3 riegos
30% -> 20% -> 10% -> 0%

### 🌲 Cambio en la Tasa de Crecimiento del Fertilizante

Los fertilizantes tenían un valor de crecimiento fijo en metros, ahora depende del impulso.
*Por ejemplo, si el impulso es del 40%, el árbol crecerá en 4 + (40 - 30) / 10 * 3 = 7*

*(4 (impulso-30)/10\*3)*

### 🍎 Ahora las ganancias de frutas son públicas

Cuando regabas un árbol y obtenías una fruta, nadie podía ver esa increíble fruta que conseguiste, ¡así que ahora todos pueden ver lo que obtuviste en el mensaje de riego! (Mensaje del árbol o los canales de notificación)

#### Mensaje del árbol

![alt text](../images/treefruitsearning.png)
> Nota: No es posible obtener 90% de boost, solo para muestra

#### Canal de notificaciones

![alt text](../images/notificationfruits.png)

### 🪲 Arreglo de bugs

Algunas correcciones de errores :D

## [0.2.2] Correcciones de errores

### El comando de ayuda no estaba buscando

El comando `/help` no estaba buscando la información del comando que querías conocer. Parece que estaba bloqueando todas las descripciones de comandos como "comandos de administrador", y los comandos de administrador no se deberian mostrar en el comando de ayuda. ¡Todo esto se ha solucionado ahora!

### Búsqueda de comandos en varios idiomas

Ahora puedes buscar ayuda para comandos tanto en el idioma predeterminado (inglés) como en español, y en el futuro funcionará con más idiomas si se agregan.

### Traducción de comandos que no se mostraban

- Water (Agua)
- Fertilize (Fertilizar)
- Mega Fertilize (Mega Fertilizar)

Todos estos comandos no mostraban su traducción en el cliente de Discord.

## [0.2.3] Recompensas por votar

### Recompensas por votar incluidas

¡Como leíste! Ahora puedes votar por TreeBot en [Top.gg](https://top.gg/bot/1169844816176230480/vote) y [DiscordBotList](https://discordbotlist.com/bots/treebot-1943/upvote) para obtener **5x 🪴 Mega Fertilizantes**, ¡solo por votar!

Y, por supuesto, se agregó el comando `/vote` para que puedas acceder fácilmente a los enlaces de votación.

> [!NOTE]
> Mientras Top.gg notifica a TreeBot instantáneamente sobre tu voto, DiscordBotList puede tardar hasta una hora en notificar a TreeBot. Como resultado, deberás esperar al menos una hora para recibir la recompensa en DiscordBotList.

### Algunas correcciones de errores

- Se actualizó la biblioteca que interactúa con Discord a la última versión, corrigiendo algunos errores con las interacciones fallidas.
- `/profile` mostraba *"No traducido (BACKGROUND.BACKGROUND-XX.NAME)"* debido a una actualización en cómo se gestionan los códigos de idioma de los fondos.
- Algunas otras correcciones menores
