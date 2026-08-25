# Bitácora · descargas

Aquí viven **solo los instaladores** de Bitácora, la aplicación de gestión de la
consulta. El código fuente está en un repositorio privado aparte.

## Instalar

Ve a [Releases](../../releases) y descarga el instalador más reciente
(`Bitacora-win-Setup.exe`). Una vez instalada, la aplicación se actualiza sola: no
hace falta volver por aquí.

## Por qué este repositorio existe

El repositorio del código es privado, y descargar de las *releases* de un repositorio
privado exigiría llevar un token dentro de la propia aplicación. Eso es justo lo que no
se debe hacer con algo que se distribuye. La salida limpia es publicar los binarios en
un repositorio público aparte, que es este.

## Qué NO hay aquí

Ningún dato de pacientes, ninguna base de datos y ninguna copia de seguridad. Los datos
de la consulta viven cifrados en el ordenador de la profesional y no salen de ahí; lo
que se publica aquí es únicamente el programa.

## Aviso al instalar

Mientras el ejecutable no esté firmado, Windows mostrará un aviso de SmartScreen
("Windows protegió tu PC"). Hay que pulsar **Más información → Ejecutar de todas
formas**. Es esperable en cualquier programa sin certificado de firma de código.
