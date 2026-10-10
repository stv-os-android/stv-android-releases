<p align="right"><a href="overview.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) › **Presentación**

**Presentación** · [Versiones](releases.es.md) · [Manual](manual.es.md)

# Presentación

## Qué es STV OS

STV OS es un sistema Android 13 hecho para la TrimUI Smart Pro S. Se basa en el Android de la Radxa
Cubie A5E, una placa con el mismo procesador (Allwinner A523), y rehace lo que la consola necesita:
un kernel Linux propio, un sistema reducido para que quepa en 1 GB de RAM, apps propias para todo lo que la consola
hace fuera de un juego y un emulador de PSP ajustado para este hardware.

Se instala de una de dos maneras, y las dos se mantienen:

- **En una tarjeta microSD.** La tarjeta es el disco del sistema. La memoria interna no se toca:
  sin la tarjeta, la consola arranca su firmware de fábrica como siempre.
- **En la memoria interna.** STV OS reemplaza el firmware de fábrica. Arranca más rápido, y la
  microSD pasa a ser una tarjeta FAT32 común para juegos y partidas.

## El objetivo: PSP

La PSP es el sistema más exigente que esta consola puede ejecutar bien, y es la razón del proyecto.
El trabajo se mide escena por escena en los juegos más pesados, con la misma compilación y los
mismos ajustes, antes y después de cada cambio.

| Juego y escena | Antes de los cambios de STV (misma consola) | Con STV OS | Condiciones |
|---|---|---|---|
| *Dante's Inferno*, una pelea con nueve personajes | 58-69 % de la velocidad completa | **99,5 %** | misma resolución e imagen, sin overclock |
| *God of War: Ghost of Sparta*, la pelea con Callisto | cerca del 56 % | **60 fps** | resolución 2× PSP |
| *God of War: Ghost of Sparta*, un combate con varios enemigos | 46,4 fps | **59,5 fps** (mediana) | 1271×720, la pantalla a 1:1 |

Estos resultados son de **PPSSPP - STV**, una versión de PPSSPP ajustada a la GPU de la consola
(Mali-G57) y a su memoria: sombras más ligeras de calcular, menos dibujos inútiles, copias de
texturas limitadas a lo que se usa y un hilo de gráficos que ya no se queda esperando a otros
procesos. El PPSSPP oficial
también viene instalado, como alternativa.

## Qué más cambia

- **Kernel.** Controladores de pantalla, energía, batería y temperatura ajustados a esta consola:
  60 Hz reales, el panel apagado del todo al dormir, un porcentaje de batería que no cae justo
  después de cargar y el ventilador manejado por el pequeño núcleo RISC-V del procesador.
- **Memoria.** Android sin las partes que una portátil no usa (SystemUI entre ellas), para que los
  juegos tengan más de ese 1 GB.
- **Apps STV.** Un centro de control (botón HOME), una vista de apps abiertas (botón MENU),
  avisos, una pantalla de bloqueo con el mando, el indicador de volumen y las capturas de
  pantalla: todo lo que la consola hace fuera de un juego, pensado para el mando.
- **Menú de juegos.** Pegasus con el tema STV. *Administrar Sistemas* agrega sistemas, instala los
  núcleos de los emuladores, busca carátulas sin computadora y respalda las partidas de todos los
  emuladores en un solo archivo.
- **Otros sistemas.** RetroArch para GBA, PS1, NES, SNES, Game Boy, Neo Geo y más; Mupen64Plus FZ
  para Nintendo 64.
- **Actualizaciones.** Paquetes firmados que se instalan desde la consola, con vuelta a la versión
  anterior.

## Estado

Es una **beta**. Se usa a diario desde hace semanas en una consola. Lo que conviene saber antes
de instalar:

- No es un sistema oficial de TrimUI. En la memoria interna reemplaza el firmware de fábrica (la
  vuelta atrás es el archivo de firmware oficial de TrimUI, instalado de la misma forma).
- El sistema está firmado con las claves de prueba públicas de Android y SELinux funciona en
  modo permisivo. Instale apps solo de fuentes de confianza.
- STV OS no incluye juegos ni archivos de BIOS.

## Créditos

STV OS se apoya en el trabajo de muchos proyectos:

- **Radxa**: la base de Android 13 para el Allwinner A523 (Cubie A5E).
- **Orange Pi**: el árbol del kernel Linux 5.15 para el A523.
- **KNULLI**: las piezas de arranque de las que parte STV OS en esta consola.
- **TrimUI**: la consola, y su cargador de arranque y su servicio de entrada de fábrica.
- **PPSSPP**, **RetroArch** y los núcleos de **libretro**, **Mupen64Plus FZ**, **Pegasus Frontend**,
  **Aurora Store** y **LeanKeyboard**.
- Las fuentes **IBM Plex**.

La lista completa, con la licencia de cada uno, está en `NOTICE.txt` (se publica con cada versión) y
en **Ajustes STV › Acerca de la consola › Licencias**.
