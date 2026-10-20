<p align="right"><a href="overview.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) · **Presentación** · [Descargas e instalación](releases.es.md) · [Manual](manual.es.md)

# Presentación

## Qué es STV OS

STV OS es un custom firmware basado en Android 13, hecho para la TrimUI Smart Pro S. Parte del Android de la
Radxa Cubie A5E, una placa con el mismo procesador (Allwinner A523), y suma un kernel Linux propio, apps
propias para la consola y un emulador de PSP optimizado para esta consola.

Se instala en la memoria interna o en una tarjeta microSD:
[cuál elegir](releases.es.md#qué-instalación-elegir).

## Rendimiento en PSP

La PSP es el sistema más exigente que esta consola ejecuta bien. Cada cambio se mide escena por escena en los
juegos más pesados, con los mismos ajustes antes y después.

| Juego y escena | Antes de los cambios de STV | Con STV OS | Resolución |
|---|---|---|---|
| *Dante's Inferno*, una pelea con nueve personajes | 58-69 % de la velocidad completa | **99,5 %** | La misma antes y después |
| *God of War: Ghost of Sparta*, la pelea con Callisto | 33,7 fps | **60 fps** | 2× PSP |
| *God of War: Ghost of Sparta*, un combate con varios enemigos | 46,4 fps | **59,5 fps** (mediana) | *Panel 1:1 (STV)* |

Todos los resultados son sin overclock y sin bajar la resolución ni la calidad. Son de **PPSSPP - STV**, una
versión de PPSSPP optimizada para la GPU de la consola (Mali-G57) y su memoria. El PPSSPP oficial también
viene instalado. Qué cambia y cómo: [PPSSPP - STV](manual.es.md#ppsspp---stv) en el manual.

## Qué más cambia

- **Kernel.** Controladores de pantalla, energía, batería y temperatura ajustados a esta consola: 60 Hz
  reales, la pantalla apagada del todo al dormir, un porcentaje de batería que no cae justo después de
  cargar y el ventilador automático.
- **Memoria.** Android sin las partes que una portátil no necesita, para que los juegos tengan más de su
  1 GB de RAM.
- **Apps STV.** La interfaz de Android está hecha para pantallas táctiles. STV OS la reemplaza por la suya:
  centro de control (HOME), apps abiertas (MENU), avisos, pantalla de bloqueo, indicador de volumen y
  capturas de pantalla.
- **Menú de juegos.** Pegasus con el tema STV: un menú de sistemas, los últimos jugados, favoritos, cuatro
  vistas de juegos y una ficha de cada juego, con el tema STV Neo como alternativa. *Administrar Sistemas*
  agrega sistemas, instala cores de emuladores, busca carátulas y respalda partidas, todo desde la consola.
- **Sticks analógicos.** Calibración desde Ajustes STV, que se aplica en todas las apps y emuladores.
- **Otros sistemas.** RetroArch para GBA, PS1, NES, SNES, Game Boy y más; Mupen64Plus FZ para Nintendo 64.
- **Actualizaciones.** Paquetes firmados que se instalan desde la consola, con vuelta a la versión anterior.

## Estado

**Beta**, probada en una sola consola. No es un sistema oficial de TrimUI y no incluye juegos ni BIOS. Antes
de instalar, lea los [problemas conocidos](releases.es.md#problemas-conocidos).

## Créditos

STV OS se apoya en el trabajo de estos proyectos:

- **Radxa**: la base de Android 13 para el Allwinner A523 (Cubie A5E).
- **Orange Pi**: el árbol del kernel Linux 5.15 para el A523.
- **KNULLI**: el cargador de arranque de la instalación en microSD.
- **TrimUI**: la consola, el cargador de arranque de la instalación en memoria interna y el servicio de los
  controles.
- **PPSSPP**, **RetroArch** y los cores de **libretro**, **Mupen64Plus FZ**, **Pegasus Frontend**,
  **Aurora Store** y **LeanKeyboard**.
- **hazem-abdelghani** (Retro Mega Neo), **plaidman** (RetroMega Next) y **David Fumberger** (RetroMega):
  los temas en los que se basa STV Neo.
- Las fuentes **IBM Plex**.

La lista completa, con la licencia de cada uno, está en `NOTICE.txt` y en
**Ajustes STV › Acerca de la consola › Licencias**.
