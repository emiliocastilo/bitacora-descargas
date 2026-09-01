# Bitácora · descargas

Aquí viven **los instaladores y el manual** de Bitácora, la aplicación de gestión de
la consulta. El código fuente está en un repositorio privado aparte.

Web: **https://emiliocastilo.github.io/bitacora-descargas/**

## Instalar

Descarga el instalador más reciente:
<https://github.com/emiliocastilo/bitacora-descargas/releases/latest/download/Bitacora-win-Setup.exe>

O ve a [Releases](../../releases) y coge el `Bitacora-win-Setup.exe` de la versión de
arriba. Una vez instalada, la aplicación se actualiza sola: no hace falta volver por aquí.

## Manual

La guía de uso completa está en **[MANUAL.md](MANUAL.md)** (y en la web de arriba).
Cada versión adjunta además su manual en su
[release](https://github.com/emiliocastilo/bitacora-descargas/releases).

Este archivo, `index.html`, los `_layouts/`, `_config.yml` y `MANUAL.md` se generan
desde el repositorio del código en cada release; no se editan aquí a mano.

## Por qué este repositorio existe

El repositorio del código es privado, y descargar de las *releases* de un repositorio
privado exigiría llevar un token dentro de la propia aplicación. Eso es justo lo que no
se debe hacer con algo que se distribuye. La salida limpia es publicar los binarios en
un repositorio público aparte, que es este.

## Qué NO hay aquí

Ningún dato de pacientes, ninguna base de datos y ninguna copia de seguridad. Los datos
de la consulta viven cifrados en el ordenador de la profesional y no salen de ahí; lo
que se publica aquí es únicamente el programa y su manual.

## Aviso al instalar

Mientras el ejecutable no esté firmado, Windows mostrará un aviso de SmartScreen
("Windows protegió tu PC"). Hay que pulsar **Más información → Ejecutar de todas
formas**. Es esperable en cualquier programa sin certificado de firma de código.
