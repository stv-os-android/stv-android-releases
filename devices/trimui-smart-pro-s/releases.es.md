<p align="right"><a href="releases.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) · [Presentación](overview.es.md) · **Descargas e instalación** · [Manual](manual.es.md)

# Descargas e instalación

- [Qué instalación elegir](#qué-instalación-elegir)
- [Instalar en la memoria interna](#instalar-en-la-memoria-interna)
- [Instalar en una tarjeta microSD](#instalar-en-una-tarjeta-microsd)
- [Después de instalar](#después-de-instalar)
- [Actualizar desde una versión anterior](#actualizar-desde-una-versión-anterior)
- [Versiones disponibles](#versiones-disponibles)
- [Problemas conocidos](#problemas-conocidos)
- [Verificar una descarga](#verificar-una-descarga)

## Qué instalación elegir

| | Memoria interna | Tarjeta microSD |
|---|---|---|
| Firmware de fábrica | Se reemplaza (vuelve con el archivo oficial de TrimUI) | Intacto: sin la tarjeta, la consola lo arranca como siempre |
| La tarjeta microSD | Una tarjeta FAT32 para juegos y partidas, legible en cualquier computadora | El disco del sistema, con los juegos y las partidas dentro |
| Tiempo de arranque | Cerca de 1 minuto | De 1 a 4 minutos, según la tarjeta |
| Espacio para apps y datos | Unos 5,5 GB | La tarjeta entera, después de *Ampliar a toda la tarjeta* |
| Se instala con | Un archivo en una tarjeta FAT32 y una combinación de botones | Raspberry Pi Imager en una computadora |

Si tiene dudas, empiece por la tarjeta microSD: la consola no cambia, y puede pasar a la memoria interna más
adelante.

## Instalar en la memoria interna

Esta instalación reemplaza el firmware de fábrica.

> [!WARNING]
> **Se borran los datos internos de la consola**, incluidas las apps y las partidas del firmware de fábrica
> (*Apps/ports*). Los juegos y las partidas de la tarjeta microSD no se tocan.

**Requisitos:** una tarjeta microSD con formato FAT32 y 1,5 GB libres (puede ser su tarjeta de juegos) y el
cargador de la consola.

> [!WARNING]
> **No use una tarjeta que haya sido de sistema de STV OS (instalación en microSD).** Si la tarjeta tiene una
> zona de arranque, la consola arranca desde ella, y formatearla no la borra. Use otra tarjeta o bórrela por
> completo antes (por ejemplo, con *SD Card Formatter* y su opción *Overwrite format*).

> [!NOTE]
> Las tarjetas de 64 GB o más suelen venir con formato exFAT. Formatéelas en FAT32: en macOS, con Utilidad
> de Discos (*MS-DOS (FAT)*); en Windows, una tarjeta de más de 32 GB necesita una herramienta de formato
> FAT32 de terceros.

1. Descargue `stv-os-<versión>-trimui-smart-pro-s-internal-memory.zip` de
   [Versiones disponibles](#versiones-disponibles) y descomprímalo. Contiene `trimui_tg5050.awimg` (unos
   1,3 GB). **No le cambie el nombre**: la consola busca exactamente ese.
2. Copie `trimui_tg5050.awimg` en la raíz de la tarjeta, no dentro de una carpeta.
3. Apague del todo la consola. Si tiene dudas, mantenga pulsado POWER 20 segundos.
4. Inserte la tarjeta y conecte el cargador.
5. Mantenga pulsado Volumen −. Sin soltarlo, pulse POWER durante 3 segundos. Suelte POWER, pero **siga con
   Volumen − pulsado** hasta que aparezca una barra de progreso verde. Después suelte Volumen −.
6. Espere. Cuando termine la barra, la consola se reinicia sola y arranca STV OS. El primer arranque tarda
   unos minutos más.
7. Borre `trimui_tg5050.awimg` de la tarjeta.

Si la consola arranca normalmente sin mostrar la barra, no detectó la combinación. Apáguela y repita desde
el paso 3, sin soltar Volumen − hasta ver la barra.

**Volver al firmware de fábrica:** use el `trimui_tg5050.awimg` oficial de TrimUI (firmware v1.0.1) y repita
los pasos 2 a 7.

## Instalar en una tarjeta microSD

La tarjeta pasa a ser el disco del sistema de la consola. La memoria interna no se toca.

**Requisitos:** una tarjeta microSD de 16 GB o más (se borra todo lo que tenga) y una computadora con
[Raspberry Pi Imager](https://www.raspberrypi.com/software/). Una tarjeta rápida (A1/A2 o U3) acorta el
primer arranque.

1. Descargue `stv-os-<versión>-trimui-smart-pro-s-microsd.img.xz` de
   [Versiones disponibles](#versiones-disponibles). No hace falta descomprimirlo.
2. Abra Raspberry Pi Imager. En *Sistema operativo*, elija **Usar personalizado** (*Use custom*, al final de
   la lista) y seleccione el archivo descargado.
3. En *Almacenamiento*, elija la tarjeta microSD. Revise el tamaño para no elegir otro disco.
4. Si ofrece personalizar el sistema operativo, omita ese paso. Confirme y espere a que grabe y verifique.
5. Si después la computadora dice que no puede leer el disco, cierre el aviso sin formatear: **Ignorar** o
   **Expulsar** en macOS, **Cancelar** en Windows.
6. Inserte la tarjeta en la consola y enciéndala.

> [!WARNING]
> El **primer arranque** prepara las apps e instala los emuladores. Con una tarjeta lenta puede tardar más
> de 10 minutos, con la pantalla negra durante varios de ellos. No apague la consola.

> [!TIP]
> Para usar la tarjeta entera, entre en **Ajustes STV › Almacenamiento › Ampliar a toda la tarjeta** y
> reinicie.

**Volver al firmware de fábrica:** apague la consola y retire la tarjeta.

## Después de instalar

- La consola arranca en inglés y con la hora UTC. Cámbielos en **Ajustes STV › Idioma del sistema** y
  **Ajustes STV › Fecha y hora**.
- Conéctese a una red Wi-Fi en **Ajustes STV › Wi-Fi**. El reloj se ajusta solo, y *Administrar Sistemas*
  puede descargar cores de emuladores y carátulas.
- La depuración por USB y el acceso root vienen apagados. Enciéndalos en **Ajustes STV › Desarrollo** solo
  si los necesita.
- Copie sus juegos en `Roms/<sistema>/` (por ejemplo, `Roms/psp/`):
  - **Instalación en memoria interna:** en la raíz de la tarjeta microSD, con formato FAT32.
  - **Instalación en microSD:** en el almacenamiento interno de la consola.

  El [manual](manual.es.md#los-juegos-y-la-carpeta-roms) explica cómo.

## Actualizar desde una versión anterior

Una consola que ya tiene STV OS (0.0.1-beta o posterior) se actualiza desde la consola, sin reinstalar:
juegos, partidas, apps y ajustes se conservan. Un mismo paquete se instala sobre cualquier versión anterior,
así que no hace falta pasar por las versiones intermedias.

1. En la última versión de [Versiones disponibles](#versiones-disponibles), descargue el archivo de
   **actualización** de su tipo de instalación: el que termina en `-internal-memory.zip` (memoria interna) o
   el que termina en `-microsd.zip`. No lo renombre ni lo descomprima.
2. Cópielo en la carpeta `STV/update`: en la instalación en memoria interna, en la tarjeta microSD o en el
   almacenamiento interno; en la instalación en microSD, en el almacenamiento interno. Para copiarlo desde
   una computadora, use **Ajustes STV › Transferencia USB**.
3. Abra **Ajustes STV › Actualización del sistema**, elija el paquete y confirme. Antes de instalar se
   muestran las notas de la versión nueva.
4. La consola prepara la actualización en unos minutos; después, **Reiniciar e instalar**. El logo queda en
   pantalla unos 3 minutos y la consola arranca con la versión nueva.

Después, **Actualización del sistema** muestra la versión nueva y ofrece **Volver a** la anterior. Un paquete
del otro tipo de instalación se rechaza antes de escribir nada. El [manual](manual.es.md#actualizaciones)
tiene el detalle.

## Versiones disponibles

### 0.0.2-beta · 2026-10-20

Calibración de los sticks, un menú de sistemas nuevo y el tema STV Neo en el lanzador de juegos, Capcom CPS-3
y MAME, y una corrección de la carga, que podía detenerse con el LED rojo parpadeando. [Notas de la versión](https://github.com/stv-os-android/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.2-beta) (en inglés).

| Archivo | Contenido | Tamaño |
|---|---|---|
| [stv-os-0.0.2-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/stv-os-0.0.2-beta-trimui-smart-pro-s-internal-memory.zip) | Instalación en la memoria interna | 978 MB |
| [stv-os-0.0.2-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/stv-os-0.0.2-beta-trimui-smart-pro-s-microsd.img.xz) | Instalación en una tarjeta microSD | 848 MB |
| [STV-TSPS-update-f217-internal-memory.zip](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/STV-TSPS-update-f217-internal-memory.zip) | Actualización de una instalación en memoria interna | 979 MB |
| [STV-TSPS-update-f217-microsd.zip](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/STV-TSPS-update-f217-microsd.zip) | Actualización de una instalación en microSD | 750 MB |
| [stv-os-0.0.2-beta-gpl-source.tar](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/stv-os-0.0.2-beta-gpl-source.tar) | Código fuente GPL: el kernel de esta versión, con sus parches y su configuración, y el resto del código GPL | 206 MB |
| [NOTICE.txt](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/NOTICE.txt) | Componentes de terceros y licencias | |
| [SHA256SUMS](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.2-beta/SHA256SUMS.sig) | Sumas de verificación y su firma | |

### 0.0.1-beta · 2026-10-10

Primera versión pública. [Notas de la versión](https://github.com/stv-os-android/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.1-beta) (en inglés).

| Archivo | Contenido | Tamaño |
|---|---|---|
| [stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip) | Instalación en la memoria interna | 974 MB |
| [stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz) | Instalación en una tarjeta microSD | 845 MB |
| [stv-os-0.0.1-beta-gpl-source.tar](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-gpl-source.tar) | Código fuente GPL: el kernel de esta versión, con sus parches y su configuración, y el resto del código GPL | 206 MB |
| [NOTICE.txt](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/NOTICE.txt) | Componentes de terceros y licencias | |
| [SHA256SUMS](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS.sig) | Sumas de verificación y su firma | |

## Problemas conocidos

- Se probó en una sola consola; otros lotes de fabricación podrían comportarse distinto.
- Las tarjetas microSD en exFAT no se probaron con la instalación en memoria interna: use FAT32.
- Volver al firmware de fábrica con el archivo oficial de TrimUI no se probó de principio a fin con STV OS
  instalado.
- El sistema está firmado con las claves de prueba públicas de Android y SELinux funciona en modo permisivo.
  Instale apps solo de fuentes de confianza.
- balenaEtcher 2.1.7 no muestra ningún disco en macOS 26: use Raspberry Pi Imager.

## Verificar una descarga

Cada versión publica `SHA256SUMS`, firmado con la clave de [`keys/`](../../keys/).

En macOS y Linux:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

En Windows (PowerShell), calcule la suma y compárela con la línea del archivo en `SHA256SUMS`:

```powershell
Get-FileHash .\stv-os-0.0.2-beta-trimui-smart-pro-s-internal-memory.zip -Algorithm SHA256
```

Para verificar la firma, use OpenSSL 3:

```bash
openssl pkeyutl -verify -pubin -inkey stv-release-ed25519.pub.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

El `openssl` que trae macOS no verifica firmas Ed25519; el de Homebrew sí.
