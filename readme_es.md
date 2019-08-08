# RetroPack
RetroPack - Una imagen con RetroReloaded + Emunand + Android

# ¿Porqué RetroPack?

Simple. En vez de tener 2 tarjetas SD, una para switch y otra para android, RetroPack te da la posibilidad de disponer estos dos en una única SD..

# Tamaño de las particiones

Algunos querrán saber el tamaño de las particiones así que esta es la configuración que estoy usando:

emuMMC requiere alrededor de unos 30 GBytes.

Android requiere alrededor de unos  20 Gbytes.

El resto es una partición FAT32 donde se almacenará RetroReloaded, Atmosphere, homebrews, etc .
Así que básicamente esta es mi configuración. Si tú SD es de 64 GBytes, tendrás un total de  14 Gbytes de espacio libre para todo lo mencionado antes, en caso de tener una SD de 128 GBytes, dispondrás de unos 78 GBytes libres y si es de 256 GBytes, serán alrededor de unos 206 Gigabytes.

Siempre será más grande la partición en FAT32 (menos en la imagen de 64Gbytes por ser una SD de menor tamaño que las demás) porque será usado por el sistema operativo de la switch y por android (android podrá acceder a esta partición con lo cual no requiere de una nueva partición más grande).

# Instalación

Debido a que hacer las particiones es muy difícil, y el uso obligatorio de Linux he decidido empaquetar todo en una imagen flasheable.

Y es tal que así:

Hay dos tipos de versiones de RetroPack, según las opciones que quieras y el espacio de tu SD.

Para bootear la SD una vez finalizado el flasheo, deberás de copiar el payload que hay en la raíz de la partición “HOS_DATA” y abrirlo con tegrarcmgui u otro lanzador de payloads, recuerda no eliminar el payload de la SD.
Para la gente que usa un dongle deberá ejecutar el payload forwarder que ejecuta el payload.bin de la SD.

## Versión Roja ( RetroPack Red )

RetroPack Red está listo para poder ejecutar EmuMMC y android juntos. La partición de la EmuMMC está lista para instalar.

### Pasos para la versión roja

Flashea la imagen con Etcher-Balena

Aquí está el link: [Etcher-Balena](https://www.balena.io/etcher/)

Select image file -> Select your microSD destination -> Flash

1 .- El el primer booteo iniciará RetroReloaded y verás que el botón de al lado del icono de atmosphere está desactivado. Esto es porque tú EmuMMC todavía no ha sido creada.

![alt text](rr_boot_v2_noemu.png)

Pulsa sobre el icono de hekate.

2.- Una vez ya en hekate, toca la opción de EmuMMC.

![alt text](hekate1.png)

3.- A la derecha toca “Create EmuMMC”

![alt text](hekate2.png)

4.- Selecciona “SD partición”.

5.- Y continua.

6.- Y eso es todo. Cuando termine (habitualmente suele tardar unos 10 minutos aproximados), podrás tocar “Close” situado arriba a la derecha de la pantalla, y presiona “back to RR” para volver a RetroReloaded.

![alt text](rr_boot_v2.jpg)

7.- Ahora ya podrás ver el botón de EmuMMC.

8.- Para iniciar android solo selecciona hekate y pulsa el botón de “launch options” y verás un botón para iniciar Switch-root Android.

#### Descargas

Aquí está el link de descarga, recuerda escoger tu versión y tamaño de SD.

Note: De todas formas la versión roja ahora mismo solo dispone de la imagen de 128gb (estoy trabajando en los otros tamaños).

[RetroPack Images](https://mega.nz/#F!TvYyGS5D!4CRLomt3FVgD2c4UvcB_fQ)

## Versión Azul ( RetroPack Blue )

RetroPack Blue está lista para usar RetroReloaded + android. Esta versión no dispone de una partición lista para EmuMMC. Así que si quieres RetroReloaded + EmuMMC + Android, deberías instalar RetroPack Red.

### Pasos para la versión azul

Flashea la imagen en tu SD con EtcherBalena.

Aquí el link: [Etcher-Balena](https://www.balena.io/etcher/)

Select image file -> Select your microSD destination -> Flash

1.- Descarga la imagen correspondiente a tu tarjeta SD y eso es todo.

![alt text](rr_boot_v2_noemu.png)

Recuerda, Para lanzar android debes de ir a Hekate => Launch option.

2.- En la primera pantalla de RetroPack, verás el menú de RetroReloaded y selecciona hekate.

![alt text](hekate1.png)

3.- Una vez en hekate selecciona “Launch options”.

4.- Una vez dentro verás el icono de Android de Switchroot android.

#### Descargas

Aquí está el link de descarga, recuerda escoger tu versión y tamaño de SD.

Note: De todas formas la versión azul ahora mismo solo dispone de la imagen de 128gb (estoy trabajando en los otros tamaños).

[RetroPack Images](https://mega.nz/#F!TvYyGS5D!4CRLomt3FVgD2c4UvcB_fQ)

