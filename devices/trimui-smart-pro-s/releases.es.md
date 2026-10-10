<p align="right"><a href="releases.md">English</a> · <b>Español</b></p>

[STV OS](../../README.es.md) › [TrimUI Smart Pro S](README.es.md) › **Versiones**

[Presentación](overview.es.md) · **Versiones** · [Manual](manual.es.md)

# Versiones

- [Qué instalación elegir](#qué-instalación-elegir)
- [Instalar en la memoria interna](#instalar-en-la-memoria-interna)
- [Instalar en una tarjeta microSD](#instalar-en-una-tarjeta-microsd)
- [Después de instalar](#después-de-instalar)
- [Versiones disponibles](#versiones-disponibles)
- [Problemas conocidos](#problemas-conocidos)
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

**Necesitará:** una tarjeta microSD con formato **FAT32** y 1,5 GB libres (puede ser la tarjeta que
después use para los juegos) y el cargador de la consola.

> [!WARNING]
> **La tarjeta no puede ser una antigua tarjeta de sistema de STV OS (modo microSD).** La consola
> arranca siempre primero desde la tarjeta cuando la tarjeta tiene una zona de arranque, y
> formatearla no la borra. Use otra tarjeta, o bórrela por completo antes (por ejemplo con
> *SD Card Formatter* y su opción *Overwrite format*).

> [!NOTE]
> **Las tarjetas de 64 GB o más** suelen venir con formato exFAT. Formatéelas en FAT32 (en macOS:
> Utilidad de Discos, *MS-DOS (FAT)*; en Windows, una tarjeta de más de 32 GB necesita una
> herramienta de formato FAT32). exFAT no se probó.

1. Descargue `stv-os-<versión>-trimui-smart-pro-s-internal-memory.zip` de
   [Versiones disponibles](#versiones-disponibles) y descomprímalo. Obtendrá el archivo
   `trimui_tg5050.awimg` (unos 1,3 GB). **No le cambie el nombre**: la consola busca exactamente
   ese.
2. Copie `trimui_tg5050.awimg` a la **raíz** de la tarjeta (no dentro de una carpeta).
3. **Apague del todo** la consola. Si tiene dudas, mantenga pulsado POWER 20 segundos.
4. Inserte la tarjeta y **conecte el cargador**.
5. Mantenga pulsado **Volumen −**. Sin soltarlo, pulse **POWER durante 3 segundos**. Suelte POWER
   pero **siga con Volumen − pulsado** hasta que aparezca una **barra de progreso verde**. Solo
   entonces suelte Volumen −.
6. Espere. Cuando termina la barra, la consola **se reinicia sola** y arranca STV OS. El primer
   arranque tarda unos minutos más que los siguientes.
7. Borre `trimui_tg5050.awimg` de la tarjeta o muévalo a una carpeta. Un encendido normal no lo
   vuelve a instalar, pero es más seguro no dejarlo en la raíz.

Si no aparece la barra y la consola arranca normalmente, la consola no detectó la combinación:
apáguela y repita desde el paso 3, sin soltar Volumen − hasta ver la barra.

**Volver al firmware de fábrica:** deje el `trimui_tg5050.awimg` oficial de TrimUI (firmware v1.0.1)
en la raíz de la tarjeta y repita los mismos pasos. Es el procedimiento del fabricante; con STV OS
instalado todavía no se probó de principio a fin.

## Instalar en una tarjeta microSD

La tarjeta pasa a ser el disco del sistema de la consola. La memoria interna no se toca.

**Necesitará:** una tarjeta microSD de **16 GB o más** (se borra todo lo que tenga) y una computadora
con [Raspberry Pi Imager](https://www.raspberrypi.com/software/) (para Windows, macOS y Linux). Una
tarjeta rápida (A1/A2 o U3) acorta mucho el primer arranque.

1. Descargue `stv-os-<versión>-trimui-smart-pro-s-microsd.img.xz` de
   [Versiones disponibles](#versiones-disponibles). No hace falta descomprimirlo.
2. Abra Raspberry Pi Imager. En el sistema operativo elija **Use custom** (al final de la lista) y
   el archivo descargado.
3. En el almacenamiento, elija la tarjeta microSD. Revise el tamaño: no elija otro disco.
4. Si pregunta por *OS customisation*, responda **No**. Confirme y espere a que grabe y verifique.
5. Si después la computadora dice que no puede leer el disco, elija **Ignorar** o **Expulsar**,
   nunca *Inicializar* ni *Formatear*.
6. Inserte la tarjeta en la consola y enciéndala normalmente.

> [!WARNING]
> El **primer arranque** prepara las apps e instala los emuladores. Con una tarjeta lenta puede
> tardar más de 10 minutos, con la pantalla negra durante varios de ellos. Espere sin apagar la
> consola.

> [!TIP]
> Para usar la tarjeta entera, entre en **Ajustes STV › Almacenamiento › Ampliar a toda la tarjeta**
> y reinicie.

**Volver al firmware de fábrica:** apague la consola y retire la tarjeta.

## Después de instalar

- La consola arranca en **inglés** y con la hora **UTC**. Se cambian en **Ajustes STV › Idioma del
  sistema** y **Ajustes STV › Fecha y hora**.
- Conéctese a Wi-Fi desde **Ajustes STV › Wi-Fi**: el reloj se ajusta solo y *Administrar Sistemas*
  puede descargar núcleos de emuladores y carátulas.
- **La depuración por USB y el acceso root vienen apagados.** Enciéndalos solo si los necesita, en
  **Ajustes STV › Desarrollo**.
- Los juegos van en `Roms/<sistema>/` (por ejemplo `Roms/psp/`): en la raíz de la tarjeta en la
  instalación en memoria interna, y en el almacenamiento interno de la consola en la instalación en
  microSD. Consulte el [manual](manual.es.md#los-juegos-y-la-carpeta-roms).

## Versiones disponibles

### 0.0.1-beta · 2026-10-10

Primera versión pública. Compilación f195 · kernel STV #122 (Linux 5.15.147).

| Archivo | Qué es | Tamaño |
|---|---|---|
| [stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip) | Instalación en la memoria interna | 974 MB |
| [stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz) | Instalación en una tarjeta microSD | 845 MB |
| [stv-os-0.0.1-beta-gpl-source.tar](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-gpl-source.tar) | **Código fuente del kernel que usa esta versión** (STV #122), sus parches y su configuración, y el resto del código GPL | 206 MB |
| [NOTICE.txt](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/NOTICE.txt) | Software de terceros y licencias | |
| [SHA256SUMS](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS.sig) | Sumas de verificación y su firma | |

**Qué trae:** el sistema descrito en la [presentación](overview.es.md), con inglés y UTC de fábrica,
la depuración por USB y el acceso root apagados en una instalación limpia, y el Wi-Fi en el dominio
regulatorio mundial. Notas completas (en inglés): [en GitHub](https://github.com/littlewild47/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.1-beta).

**Actualizaciones:** a partir de la próxima versión, cada una incluye también los paquetes de
actualización que se instalan desde la consola sin perder datos (Ajustes STV › Actualización del
sistema). El manual explica cómo.

## Problemas conocidos

Es una beta. Limitaciones conocidas de la 0.0.1-beta:

- Se probó en una sola consola; otras tandas de fabricación podrían comportarse distinto.
- Las tarjetas de ROMs en exFAT no se probaron: use FAT32.
- Volver al firmware de fábrica con el archivo oficial de TrimUI es el procedimiento del fabricante,
  pero con STV OS instalado todavía no se probó de principio a fin.
- El sistema está firmado con las claves de prueba públicas de Android y SELinux funciona en modo
  permisivo: instale apps solo de fuentes de confianza.
- FinalBurn Neo (Neo Geo y arcade) no viene incluido: se descarga desde *Administrar Sistemas* la
  primera vez que se abre uno de esos juegos.
- balenaEtcher 2.1.7 no muestra ningún disco en macOS 26: use Raspberry Pi Imager.

## Verificar una descarga

Cada versión publica `SHA256SUMS`, firmado con la clave de [`keys/`](../../keys/).

En macOS y Linux:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

En Windows (PowerShell), calcule la suma y compárela con la línea del archivo en `SHA256SUMS`:

```powershell
Get-FileHash .\stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip -Algorithm SHA256
```

La firma se verifica con OpenSSL 3:

```bash
openssl pkeyutl -verify -pubin -inkey stv-release-ed25519.pub.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

El `openssl` que trae macOS no verifica firmas Ed25519; el de Homebrew sí.
