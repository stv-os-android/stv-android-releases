<p align="right"><a href="releases.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) › **Versiones**

[Presentación](overview.es.md) · **Versiones** · [Manual](manual.es.md)

# Versiones

- [Qué instalación elegir](#qué-instalación-elegir)
- [Instalar en la memoria interna](#instalar-en-la-memoria-interna)
- [Instalar en una tarjeta microSD](#instalar-en-una-tarjeta-microsd)
- [Después de instalar](#después-de-instalar)
- [Versiones disponibles](#versiones-disponibles)
- [Verificar una descarga](#verificar-una-descarga)

## Qué instalación elegir

STV OS se instala de una de dos maneras. Las dos se mantienen y reciben las mismas versiones.

| | Memoria interna | Tarjeta microSD |
|---|---|---|
| Firmware de fábrica | Se reemplaza (vuelve con el archivo oficial de TrimUI) | Intacto: al sacar la tarjeta, la consola lo arranca como siempre |
| La tarjeta microSD | Una tarjeta FAT32 común para juegos y partidas, legible en cualquier computadora | Es el disco del sistema (los juegos y las partidas viven dentro) |
| Tiempo de arranque | Cerca de 1 minuto | De 1 a 4 minutos, según la tarjeta |
| Espacio para apps y datos | Unos 5,5 GB | La tarjeta entera |
| Se instala con | Un archivo en una tarjeta FAT32 y una combinación de botones | Raspberry Pi Imager en una computadora |

Ante la duda, conviene empezar por la **tarjeta microSD**: nada de la consola cambia, y pasar después
a la memoria interna es una instalación más.

## Instalar en la memoria interna

Reemplaza el firmware de fábrica con el mismo mecanismo que usa TrimUI para sus actualizaciones. Se
borra la partición de datos interna (con el firmware de fábrica, eso incluye *Apps/ports* y sus
partidas). Los juegos y las partidas de la tarjeta microSD no se tocan.

**Hace falta:** una tarjeta microSD con formato **FAT32** y 1,5 GB libres (puede ser la tarjeta que
después se use para los juegos) y el cargador de la consola.

1. Descargar `stv-os-<versión>-trimui-smart-pro-s-internal-memory.zip` de
   [Versiones disponibles](#versiones-disponibles) y descomprimirlo. Queda el archivo
   `trimui_tg5050.awimg` (unos 1,3 GB). **No cambiarle el nombre**: la consola busca exactamente
   ese.
2. Copiar `trimui_tg5050.awimg` a la **raíz** de la tarjeta (no dentro de una carpeta).
3. **Apagar del todo** la consola. Si hay dudas, mantener pulsado POWER 20 segundos.
4. Insertar la tarjeta y **conectar el cargador**.
5. Mantener pulsado **Volumen −**. Sin soltarlo, pulsar **POWER durante 3 segundos**. Soltar
   POWER pero **seguir con Volumen − pulsado** hasta que aparezca una **barra de progreso verde**.
   Solo entonces soltar Volumen −.
6. Esperar. Cuando termina la barra, la consola **se reinicia sola** y arranca STV OS. El primer
   arranque tarda unos minutos más que los siguientes.
7. Borrar `trimui_tg5050.awimg` de la tarjeta o moverlo a una carpeta. Un encendido normal no lo
   vuelve a instalar, pero es más seguro no dejarlo en la raíz.

Si no aparece la barra y la consola arranca normal, la combinación no se tomó: apagarla y repetir
desde el paso 3, sin soltar Volumen − hasta ver la barra.

> **La tarjeta no puede ser una antigua tarjeta de sistema de STV OS (modo microSD).** La consola
> arranca siempre primero desde la tarjeta cuando la tarjeta tiene una zona de arranque, y
> formatearla no la borra. Use otra tarjeta, o bórrela por completo antes (por ejemplo con
> *SD Card Formatter* y su opción *Overwrite format*).
>
> **Las tarjetas de 64 GB o más** suelen venir con formato exFAT. Hay que formatearlas en FAT32 (en
> macOS: Utilidad de Discos, *MS-DOS (FAT)*; en Windows, una tarjeta de más de 32 GB necesita una
> herramienta de formato FAT32). exFAT no se probó.

**Volver al firmware de fábrica:** dejar el `trimui_tg5050.awimg` oficial de TrimUI (firmware
v1.0.1) en la raíz de la tarjeta y repetir los mismos pasos. Es el procedimiento del fabricante;
con STV OS instalado todavía no se probó de principio a fin.

## Instalar en una tarjeta microSD

La tarjeta pasa a ser el disco del sistema de la consola. La memoria interna no se toca.

**Hace falta:** una tarjeta microSD de **16 GB o más** (se borra todo lo que tenga) y una computadora
con [Raspberry Pi Imager](https://www.raspberrypi.com/software/). Una tarjeta rápida (A1/A2 o U3)
acorta mucho el primer arranque.

1. Descargar `stv-os-<versión>-trimui-smart-pro-s-microsd.img.xz` de
   [Versiones disponibles](#versiones-disponibles). No hace falta descomprimirlo.
2. Abrir Raspberry Pi Imager. En el sistema operativo elegir **Use custom** (al final de la lista) y
   el archivo descargado.
3. En el almacenamiento, elegir la tarjeta microSD. Revisar el tamaño: no elegir otro disco.
4. Si pregunta por *OS customisation*, responder **No**. Confirmar y esperar a que grabe y
   verifique.
5. Si después la computadora dice que no puede leer el disco, elegir **Ignorar** o **Expulsar**,
   nunca *Inicializar* ni *Formatear*.
6. Insertar la tarjeta en la consola y encenderla normalmente.

El **primer arranque** prepara las apps e instala los emuladores. Con una tarjeta lenta puede tardar
más de 10 minutos, con la pantalla negra durante varios de ellos: hay que esperar sin apagar.

Para usar la tarjeta entera: **Ajustes STV › Almacenamiento › Ampliar a toda la tarjeta**, y
reiniciar.

**Volver al firmware de fábrica:** apagar la consola y sacar la tarjeta.

> balenaEtcher 2.1.7 no muestra ningún disco en macOS 26; Raspberry Pi Imager funciona.

## Después de instalar

- La consola arranca en **inglés** y con la hora **UTC**. Se cambian en **Ajustes STV › Idioma del
  sistema** y **Ajustes STV › Fecha y hora**.
- Conectarse a Wi-Fi desde **Ajustes STV › Wi-Fi**: el reloj se ajusta solo y *Administrar
  Sistemas* puede descargar núcleos de emuladores y carátulas.
- **La depuración por USB y el acceso root vienen apagados.** Se encienden sólo si hacen falta, en
  **Ajustes STV › Desarrollo**.
- Los juegos van en `Roms/<sistema>/` (por ejemplo `Roms/psp/`): en la raíz de la tarjeta en la
  instalación en memoria interna, y en el almacenamiento interno de la consola en la instalación en
  microSD. Ver el [manual](manual.es.md#los-juegos-y-la-carpeta-roms).

## Versiones disponibles

### 0.0.1-beta · 2026-10-10

Primera versión pública. Compilación f194 · kernel STV #122 (Linux 5.15.147).

| Archivo | Qué es | Tamaño |
|---|---|---|
| [stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip) | Instalación en la memoria interna | 974 MB |
| [stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz) | Instalación en una tarjeta microSD | 845 MB |
| [stv-os-0.0.1-beta-gpl-source.tar](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-gpl-source.tar) | **Código fuente del kernel que usa esta versión** (STV #122), sus parches y su configuración, y el resto del código GPL | 206 MB |
| [NOTICE.txt](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/NOTICE.txt) | Software de terceros y licencias | |
| [SHA256SUMS](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/estebanrios/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS.sig) | Sumas de verificación y su firma | |

**Qué trae:** el sistema descrito en la [presentación](overview.es.md), con inglés y UTC de fábrica,
la depuración por USB y el acceso root apagados en una instalación limpia, y el Wi-Fi en el dominio
regulatorio mundial. Notas completas (en inglés): [en GitHub](https://github.com/estebanrios/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.1-beta).

**Actualizaciones:** a partir de la próxima versión, cada una incluye también los paquetes de
actualización que se instalan desde la consola sin perder datos (Ajustes STV › Actualización del
sistema). El manual explica cómo.

## Verificar una descarga

Cada versión publica `SHA256SUMS`, firmado con la clave de [`keys/`](../../keys/).

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

```bash
openssl pkeyutl -verify -pubin -inkey stv-release-ed25519.pub.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

El segundo comando necesita OpenSSL 3 (el `openssl` que trae macOS no verifica firmas Ed25519; el
de Homebrew sí).
