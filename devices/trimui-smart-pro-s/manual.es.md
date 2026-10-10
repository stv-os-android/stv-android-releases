<p align="right"><a href="manual.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) › **Manual**

[Presentación](overview.es.md) · [Versiones](releases.es.md) · **Manual**

# Manual

Todo lo que STV OS agrega a la consola, pantalla por pantalla. Vale para la versión **0.0.1-beta** y
para las dos instalaciones (memoria interna y microSD); donde difieren, se aclara.

> [!NOTE]
> **Términos de este manual.** *Instalación en memoria interna* e *instalación en microSD* son las dos
> formas de instalar STV OS (consulte [Versiones](releases.es.md#qué-instalación-elegir)). El
> *almacenamiento interno* es el almacenamiento compartido de Android, el que ve una computadora por
> USB y donde están carpetas como `Roms` y `Download`: en la instalación en microSD está dentro de la
> tarjeta. La *tarjeta de ROMs* es la microSD de la instalación en memoria interna.

- [Botones y atajos](#botones-y-atajos)
- [La pantalla de inicio](#la-pantalla-de-inicio)
- [Centro de control (HOME)](#centro-de-control-home)
- [Apps abiertas (MENU)](#apps-abiertas-menu)
- [Avisos](#avisos)
- [Pantalla de bloqueo](#pantalla-de-bloqueo)
- [Ajustes STV](#ajustes-stv)
- [Administrar Sistemas](#administrar-sistemas)
- [Emuladores](#emuladores)
- [Los juegos y la carpeta Roms](#los-juegos-y-la-carpeta-roms)
- [Partidas](#partidas)
- [Actualizaciones](#actualizaciones)
- [Problemas y respuestas](#problemas-y-respuestas)
- [Reportar un problema](#reportar-un-problema)

## Botones y atajos

Funcionan en todas partes, también dentro de un juego:

| Botón | Qué hace |
|---|---|
| **HOME** (botón superior) | Abre y cierra el [centro de control](#centro-de-control-home) |
| **MENU** | Abre y cierra las [apps abiertas](#apps-abiertas-menu): pasar de una app a otra o cerrarlas |
| **Volumen + / −** | Cambia el volumen con el indicador de STV; mantenerlo pulsado lo sigue cambiando |
| **POWER**, pulsación corta | Apaga la pantalla y suspende la consola; otra pulsación la despierta |
| **POWER**, 20 segundos | Fuerza el apagado (solo si la consola no responde) |
| **L1 + R1** a la vez | Desbloquean la [pantalla de bloqueo](#pantalla-de-bloqueo) |
| **Switch FN** | Hace lo elegido en [Ajustes STV › Switch FN](#ajustes-stv): modo puntero (de fábrica), rendimiento alto para PSP, silencio, bloquear HOME y MENU en el juego, o nada |

Y dentro de cada emulador:

| Emulador | Su menú | Otros |
|---|---|---|
| PSP (PPSSPP - STV) | **L2** (menú de pausa) | **R2**: avance rápido. Los botones siguen la posición de los de la PSP: Equis abajo, Círculo a la derecha, Cuadrado a la izquierda, Triángulo arriba |
| Nintendo 64 (Mupen64Plus FZ) | **START + SELECT** | Para salir de un juego, use *Salir* en ese menú: en ese momento se copian las partidas a la tarjeta |
| Todo lo demás (RetroArch) | **START + SELECT** | Bisel y filtro de pantalla por sistema, ya configurados |

![Indicador de volumen](images/es/volume.png)

## La pantalla de inicio

La consola arranca en **Pegasus** con el tema STV: una pantalla por sistema y la carátula de cada
juego.

![Pantalla de inicio](images/es/home.png)

| Botón | Qué hace |
|---|---|
| **L1 / R1** | Sistema anterior / siguiente |
| **Cruz direccional** | Se mueve entre los juegos |
| **A** | Abre el juego con su emulador predeterminado |
| **X** | Opciones del juego (más abajo) |
| **Y** | Buscar por nombre |
| **START** | Actualiza la biblioteca (después de agregar o borrar juegos) |
| **SELECT** | Menú de Pegasus (sus ajustes, ayuda, cerrar) |

**X, opciones del juego:** elegir con qué emulador abrirlo (para PSP, *PPSSPP - STV*, afinado para
esta consola y el predeterminado, o el *PPSSPP* oficial), cambiar la vista del sistema entre grilla
y lista, o eliminar el juego y su arte de la consola.

![Opciones del juego](images/es/game-options.png)

El sistema **Android** muestra las apps instaladas: *Administrar Sistemas*, *Ajustes STV*, los
emuladores, la tienda Aurora y cualquier app que se instale.

![Apps de Android](images/es/android-apps.png)

## Centro de control (HOME)

**HOME** abre un panel a la derecha, sobre lo que haya en pantalla, también en un juego.

![Centro de control](images/es/control-center-display.png)

| Fila | Qué hace |
|---|---|
| **Wi-Fi**, **Bluetooth** | Encienden o apagan la radio |
| **Puntero** | Modo mouse: el stick derecho mueve un cursor y el izquierdo hace scroll (para apps pensadas para pantalla táctil) |
| **LEDs de los sticks** | Encienden o apagan los aros de los sticks |
| **Cooler** | Ventilador: *auto* (de fábrica), *leve*, *medio*, *máximo* o *apagado* |
| **CPU** | Perfil de rendimiento: *ahorro*, *normal*, *alto*, *alto · psp* (de fábrica) o *máximo* |
| **GPU** | Perfil de la parte gráfica, con la misma idea |
| **Brillo** | Izquierda y derecha lo ajustan |

Debajo de los perfiles, los relojes actuales de la CPU y la GPU. **A** cambia la fila elegida, **B**
cierra el panel, **X** saca una captura de pantalla (se guarda en `Pictures/Screenshots`) y
**START** abre los [avisos](#avisos).

**Y** sobre la fila de CPU o de GPU abre el **monitor de rendimiento**: el reloj de cada núcleo en
los últimos 15 minutos, junto al techo del perfil vigente. Izquierda y derecha amplían un núcleo.

![Monitor de rendimiento](images/es/performance-graph.png)

## Apps abiertas (MENU)

**MENU** muestra las apps abiertas y qué hace cada una (en juego, en uso, en segundo plano).

![Apps abiertas](images/es/open-apps.png)

**A** abre la app elegida, **X** la cierra, **Y** va a la pantalla de inicio, **B** vuelve y
**SELECT** reinicia Pegasus. Arriba se ve la memoria libre.

## Avisos

Batería baja, temperatura alta, un cable USB conectado, una captura guardada o las notificaciones de
las apps. **START** en el centro de control los abre: **A** abre uno, **X** lo descarta e **Y** los
limpia todos. Con *Vibración en avisos* encendida, la consola vibra una vez por cada aviso nuevo.

![Avisos](images/es/notices.png)

## Pantalla de bloqueo

Al despertar, la consola muestra el reloj, la fecha y la batería. **L1 + R1** a la vez la
desbloquean.

![Pantalla de bloqueo](images/es/lock-screen.png)

Se elige en **Ajustes STV › Seguridad**: *Ninguno*, *L1 + R1* (de fábrica) o un *PIN* de 4 a 16
dígitos, que se escribe con el mando (la cruz direccional se mueve, A escribe, B borra, START confirma).

## Ajustes STV

La app de ajustes propia de la consola, pensada para el mando: **A** elige, **B** vuelve, izquierda
y derecha ajustan.

![Ajustes STV](images/es/settings.png)

| Sección | Qué hay |
|---|---|
| **Transferencia USB** | Convierte la consola en una unidad para una computadora, para copiar juegos. Mientras está activa, la consola no se puede usar |
| **Pantalla** | Brillo, tiempo de espera, temperatura de color, tamaño del texto y tema (claro u oscuro; cambia a la vez Android, las apps STV y Pegasus) |
| **Sonido y vibración** | Vibración al pulsar y en los avisos, ganancia de auriculares y el micrófono para los juegos |
| **Wi-Fi** | La pantalla de Wi-Fi de Android |
| **LEDs de los sticks** | Color y brillo de cada aro, con un color RGB a medida |
| **Puntero (modo mouse)** | Encendido o apagado, y la velocidad del cursor |
| **Switch FN** | Qué hace el switch FN al pasarlo a ON |
| **Seguridad** | La [pantalla de bloqueo](#pantalla-de-bloqueo) |
| **Desarrollo** | Depuración por USB (adb) y acceso root. **Apagados** en una instalación limpia: enciéndalos solo si los necesita |
| **Almacenamiento** | Espacio usado en la memoria interna y en la tarjeta de ROMs y, en la instalación en microSD, *Ampliar a toda la tarjeta* |
| **Sistema** | Reiniciar, apagar y los ajustes completos de Android (vincular Bluetooth, teclado, permisos de las apps) |
| **Idioma del sistema** | La lista de idiomas de Android. STV OS está en inglés y en español; las apps STV y Pegasus lo siguen |
| **Fecha y hora** | Zona horaria: *Tiempo universal coordinado (UTC)* o una región y una ciudad. La hora se ajusta sola con Wi-Fi |
| **Actualización del sistema** | Instalar una versión nueva o volver a la anterior ([actualizaciones](#actualizaciones)) |
| **Apoyar el proyecto** | Un código QR que lleva a la página de apoyo |
| **Acerca de la consola** | Versión, kernel, memoria, almacenamiento, tipo de instalación y las [licencias](#problemas-y-respuestas) del software de terceros |

<table>
<tr><td><img src="images/es/settings-display.png" alt="Pantalla"></td><td><img src="images/es/settings-sound.png" alt="Sonido y vibración"></td></tr>
<tr><td><img src="images/es/settings-leds.png" alt="LEDs de los sticks"></td><td><img src="images/es/settings-fn-switch.png" alt="Switch FN"></td></tr>
<tr><td><img src="images/es/settings-developer.png" alt="Desarrollo"></td><td><img src="images/es/settings-storage.png" alt="Almacenamiento"></td></tr>
<tr><td><img src="images/es/settings-date-time.png" alt="Fecha y hora"></td><td><img src="images/es/settings-about.png" alt="Acerca de la consola"></td></tr>
</table>

## Administrar Sistemas

*Administrar Sistemas* (en el sistema Android de la pantalla de inicio) hace sin computadora lo que
de otro modo necesita una: agregar sistemas, instalar núcleos de emuladores, buscar carátulas y
respaldar partidas.

![Administrar Sistemas](images/es/systems.png)

- **A sobre un sistema** muestra sus juegos, con un punto en los que ya tienen carátula y datos.
  *Obtener lo que falta* los busca en internet (necesita Wi-Fi y tarda unos segundos por juego);
  *Obtener todo de nuevo* lo repite para todos.
- **Y dentro de un sistema** muestra el núcleo de su emulador: cuál se usa y *Actualizar core* para
  descargar el último.
- **START** abre el catálogo de sistemas: al elegir uno se crea su carpeta `Roms/<sistema>`, se
  prepara su emulador y, si hace falta, se descarga el núcleo.
- **Y sobre la lista** abre las [partidas](#partidas): *Respaldar* y *Restaurar*.

<table>
<tr><td><img src="images/es/systems-psp.png" alt="Un sistema y sus juegos"></td><td><img src="images/es/systems-new.png" alt="Sistema nuevo"></td></tr>
<tr><td><img src="images/es/systems-core.png" alt="Núcleo del emulador"></td><td><img src="images/es/systems-saves.png" alt="Partidas"></td></tr>
</table>

## Emuladores

| Sistema | Emulador | Notas |
|---|---|---|
| PSP | **PPSSPP - STV** (predeterminado) y el PPSSPP oficial | Afinado para esta consola. Resoluciones extra *2.25x PSP (STV)* y *Panel 1:1 (STV)* en Gráficos › Resolución de renderizado. Los ajustes se pueden guardar por juego |
| Nintendo 64 | Mupen64Plus FZ | GLideN64, el más rápido en esta consola |
| PlayStation | RetroArch (PCSX-ReARMed) | Funciona sin archivo de BIOS en la mayoría de los juegos (STV OS no incluye BIOS) |
| Game Boy Advance | RetroArch (mGBA) | |
| Game Boy, Game Boy Color, NES, SNES | RetroArch (Gambatte, FCEUmm, Snes9x 2010) | Incluidos: funcionan sin Wi-Fi |
| Neo Geo, arcade, CPS-1, CPS-2 | RetroArch (FinalBurn Neo) | **No viene incluido** (su licencia solo permite el uso no comercial): la primera vez que se abre uno de estos juegos, *Administrar Sistemas* ofrece *Instalar core* (necesita Wi-Fi, unos 70 MB) |
| Otros | RetroArch | Se agregan desde el catálogo de *Administrar Sistemas* |

El perfil de CPU **alto · psp** (de fábrica) es el afinado para PSP. *máximo* sube todavía más los
límites, con más calor y más consumo de batería.

## Los juegos y la carpeta Roms

Los juegos viven en una carpeta `Roms`, con una subcarpeta por sistema en minúsculas: `Roms/psp`,
`Roms/n64`, `Roms/gba`, `Roms/ps1`, `Roms/neogeo`, `Roms/nes`, `Roms/snes`…

- **Instalación en memoria interna:** `Roms` está en la raíz de la **tarjeta microSD** (FAT32). Los
  juegos se copian con un lector de tarjetas, o por USB (*Transferencia USB* muestra la tarjeta como
  una segunda unidad). La tarjeta se puede insertar y quitar con la consola encendida: la biblioteca se
  actualiza sola.
- **Instalación en microSD:** `Roms` está en el **almacenamiento interno** de la consola (dentro de
  la tarjeta). Los juegos se copian con **Ajustes STV › Transferencia USB**.

Reglas: los juegos van directamente dentro de la carpeta del sistema (no en subcarpetas), y su
nombre de archivo no puede tener más de tres puntos, contando la extensión. *Administrar Sistemas*
crea las carpetas y el archivo `metadata.pegasus.txt` que describe cada sistema; después de copiar
juegos, **START** en la pantalla de inicio actualiza la biblioteca.

## Partidas

| Emulador | Instalación en memoria interna | Instalación en microSD |
|---|---|---|
| PSP | En la tarjeta: `Android/data/org.ppsspp.ppsspp.stv/files/PSP/` | Almacenamiento interno, misma ruta |
| RetroArch | En la tarjeta: `Android/data/com.retroarch.aarch64/files/` | Almacenamiento interno: `RetroArch/saves` y `RetroArch/states` |
| Nintendo 64 | En la tarjeta: `STV/saves/n64/` | Almacenamiento interno: `M64Plus/GameData/` |

**Respaldar:** *Administrar Sistemas* › **Y** › *Respaldar* junta las partidas de los tres
emuladores en un solo archivo, `STV/backups/saves-<fecha>.zip` (en la tarjeta en la instalación en
memoria interna). Conviene copiarlo a una computadora: reinstalar borra el almacenamiento interno.
**Restaurar** muestra los respaldos y puede guardar una copia de las partidas actuales antes de
restaurar.

En la instalación en memoria interna las partidas viven en la tarjeta: sin tarjeta, los emuladores no
pueden guardar, y la consola lo avisa. No quite la tarjeta con un juego abierto.

## Actualizaciones

1. Copie el paquete de actualización (`STV-TSPS-update-<compilación>.zip`) a la carpeta
   `STV/update` o `Download` del almacenamiento interno o, en la instalación en memoria interna, a
   `STV/update` de la tarjeta.
2. **Ajustes STV › Actualización del sistema** lo encuentra, muestra sus notas y pide confirmar.
   Prepara la actualización en unos dos minutos mientras la consola se puede seguir usando; después
   reinicia y la instala en 3 a 4 minutos. No la apague.
3. Juegos, partidas, apps y ajustes se conservan. La versión anterior queda guardada: **Volver a
   <compilación>** regresa a ella.

Hace falta 40 % de batería o el cargador. Un paquete hecho para el otro tipo de instalación se
rechaza antes de escribir nada, y solo se aceptan paquetes firmados.

## Problemas y respuestas

**La consola no arranca.** Instalación en microSD: sin la tarjeta arranca el firmware de fábrica,
así que el problema está en la tarjeta; hay que grabarla de nuevo (se borra lo que tenga).
Instalación en memoria interna: instálelo de nuevo con el archivo `trimui_tg5050.awimg` y Volumen − +
POWER; se borran los datos de la memoria interna, y los juegos y las partidas de la tarjeta se
conservan.

**La pantalla quedó negra después de un reinicio del sistema.** Pulse POWER una vez para apagarla y
otra vez para encenderla.

**Los dos aros de los sticks se pusieron rojos.** El almacenamiento interno quedó en solo lectura
por un error del sistema de archivos (por ejemplo, después de un corte de energía): no se está
guardando nada. Apague la consola desde **Ajustes STV › Sistema › Apagar** y vuelva a encenderla; al
arrancar revisa y repara el almacenamiento.

**Se olvidó el PIN.** No hay forma de recuperarlo desde la consola.

**Un juego no aparece.** Revise que esté directamente en `Roms/<sistema>/`, que la carpeta del
sistema tenga su `metadata.pegasus.txt` (lo crea *Administrar Sistemas*), que la extensión figure en
él y que el nombre no tenga más de tres puntos. Después pulse **START** en la pantalla de inicio.

**Al abrir un juego de Neo Geo o de arcade aparece la pantalla del núcleo.** FinalBurn Neo no viene
incluido: pulse A en *Instalar core* (con Wi-Fi) y después B para volver; el juego se abre.

**Licencias.** **Ajustes STV › Acerca de la consola › Licencias** muestra cada componente de
terceros, su licencia, su origen y si STV OS lo modificó. STV OS es gratuito y no se vende; no
incluye juegos ni archivos de BIOS.

## Reportar un problema

Incluya:

- la versión y la compilación que muestra **Ajustes STV › Acerca de la consola** (por ejemplo,
  *0.0.1-beta · compilación f195*);
- el tipo de instalación (memoria interna o microSD);
- qué hizo, qué esperaba y qué pasó, con una captura de pantalla si es posible (**HOME** y después
  **X**).

Repórtelo en los [Issues](https://github.com/littlewild47/stv-android-releases/issues) de este
repositorio.
