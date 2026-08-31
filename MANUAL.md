# Bitácora · guía de uso

Para Carmen. Va en el orden en que se hacen las cosas: primero instalar, luego
dejar la consulta configurada, y después el día a día.

No hace falta leerla entera de una vez. Las tres primeras secciones son de una
sola vez; a partir de «El día a día» está lo que se usa siempre.

---

## 1. Instalar

1. Descargar el instalador desde este enlace, que siempre apunta a la última
   versión:
   <https://github.com/emiliocastilo/bitacora-descargas/releases/latest/download/Bitacora-win-Setup.exe>
2. Ejecutarlo. Sale una ventanita de progreso y, al terminar, la aplicación se
   abre sola.

> Si el enlace no funcionara, abrir
> <https://github.com/emiliocastilo/bitacora-descargas/releases> y descargar
> **Bitacora-win-Setup.exe** de la versión de arriba. En esa lista hay más
> archivos (uno acabado en `.nupkg`, otro llamado `RELEASES`…); no hacen falta.

**Windows dirá que no reconoce el programa.** Aparece una pantalla azul,
«Windows protegió tu PC». Es lo normal en un programa sin firma de empresa, no
es un aviso de virus. Hay que pulsar **Más información** y luego **Ejecutar de
todas formas**.

No pregunta dónde instalar ni dónde guardar los datos: eso ya está decidido. El
programa se instala en la carpeta del usuario y los datos van a `Documentos\Bitacora`
(si Documentos estuviera sincronizado con OneDrive, van a una carpeta local del
equipo, para no corromper la base). La ruta exacta se ve luego en
**Administración**, debajo del título; conviene saberla para las copias en USB
(sección 7).

Después, la aplicación se actualiza sola. Cada vez que se abre comprueba si hay
versión nueva; cuando la hay, aparece un botón **Actualizar y reiniciar** al pie
de la barra de la izquierda, y al pulsarlo se reinicia ya actualizada.

---

## 2. Crear la consulta (solo la primera vez)

Al abrirla por primera vez sale **«Vamos a preparar la consulta»**.

1. Elegir un **nombre de usuario** y una **contraseña**. Mínimo doce
   caracteres.
2. Repetirla y pulsar **Crear la consulta**.
3. Aparece una última pantalla, **«Conectar con Google»**. Se puede hacer ahora
   —hace falta el archivo `client_secret.json`, explicado en §3.5— o pulsar
   **Ahora no** y dejarlo para más tarde. En los dos casos se entra a
   continuación en **Administración**.

**Sobre la contraseña, que esto importa de verdad.** Todo va cifrado con ella:
la base de datos y también las copias de seguridad. No se guarda en ninguna
parte, ni siquiera cifrada, así que **nadie puede recuperarla**: ni yo, ni
Google, ni reinstalando. Si se pierde la contraseña y no hay clave de
recuperación, los datos no se abren nunca más.

La clave de recuperación se genera en el paso siguiente y es el único seguro
que existe contra eso.

> Si ya hubiera una consulta en otro ordenador, aquí abajo están **Buscar en
> Drive…**, **Desde una carpeta…** y **Desde un archivo…**. Están explicados en
> la sección 7.

---

## 3. Dejar la consulta lista

Al entrar se aterriza en **Administración**, repartida en pestañas: *Consulta*,
*Tarifas*, *Cuestionarios*, *Seguridad y copias*, *Conexiones* y *Diagnóstico*.

Para dejar la consulta lista hay que pasar por cuatro, y ya no se vuelven a
tocar salvo que cambie algo: **Consulta** (§3.1), **Tarifas** (§3.2), **Seguridad
y copias** (§3.3 y §3.4) y **Conexiones** (§3.5). *Cuestionarios* solo hace falta
si se van a pasar test (§6), y *Diagnóstico* (§3.6) no se toca.

![Pantalla de Administración, abierta por la pestaña Consulta con los datos de la profesional](imagenes/administracion.png)

### 3.1 Consulta

Tres cosas en esta pestaña:

- **Datos de la profesional**: nombre y apellidos, NIF, número de colegiada,
  dirección. Salen en las facturas y en los informes. **El número de colegiada es
  obligatorio** en la factura de un servicio sanitario. Pulsar **Guardar datos**.
- **Consentimiento vigente**: una etiqueta con la versión del documento de
  consentimiento que se está haciendo firmar (por ejemplo `2026-01`). No es el
  documento en sí —el consentimiento firmado de cada paciente se guarda en su
  ficha (§4)—, solo sirve para saber quién firmó qué: al cambiar la versión, las
  fichas que habían firmado la anterior quedan marcadas para volver a firmar.
- **Logotipo de la consulta**: se estampa como marca de agua muy atenuada en las
  facturas e informes que se exporten. Opcional.

### 3.2 Tarifas

- **Tipos de terapia**: la lista de lo que ofrece la consulta. Vienen dos puestas,
  **Terapia individual** y **Terapia de pareja**, y se pueden añadir las que hagan
  falta con **Añadir**: se le pone nombre (por ejemplo, «Individual online») y se
  marca **De pareja** si necesita dos personas. Cada una lleva su propio precio,
  que es el que se aplica a las sesiones de los casos abiertos con esa terapia.
- **Retirar una terapia**: el interruptor de cada línea. Una terapia retirada deja
  de ofrecerse al abrir casos nuevos, pero **no se borra nada**: los casos que ya
  la usaban siguen igual y su historial de precios se conserva. Se puede volver a
  activar cuando se quiera.
- **Aviso para cancelar**: horas. Por debajo de ese margen, la sesión cancelada
  se cobra entera. Vienen 24 puestas.
- **Recordar al paciente**: horas antes de la sesión para enviarle el correo de
  recordatorio. Un 0 significa no enviar ninguno.

Pulsar **Guardar tarifas**.

Cambiar una tarifa **solo afecta a lo que se agende a partir de ese momento**.
Las sesiones ya agendadas conservan el importe que tenían.

### 3.3 La clave de recuperación

En la pestaña **Seguridad y copias** hay cuatro apartados: el registro de accesos
y las copias de seguridad (los dos explicados en §7), la clave de recuperación y
la verificación en dos pasos. Los dos últimos se dejan puestos ahora.

Esto es lo más importante de toda la guía.

1. En **Administración › Seguridad y copias**, bajar hasta **Clave de recuperación**.
2. Escribir la contraseña en **Confirma tu contraseña**.
3. Pulsar el botón de generar.
4. Aparece un código de ocho grupos, tipo `4KWQ-9M2T-…`. Pulsar **Guardar en un
   archivo…**, imprimirlo, y **guardar el papel fuera del ordenador**: una
   carpeta física, una caja fuerte, en casa.
5. Pulsar **Ya la he guardado** para que desaparezca de pantalla.

Es lo único que permite entrar si se olvida la contraseña. No sirve de nada
guardarlo en el mismo ordenador, ni en el correo. Generar una clave nueva
invalida el papel anterior.

### 3.4 Verificación en dos pasos (opcional, recomendable)

Añade un segundo candado: además de la contraseña, un código de seis dígitos que
va cambiando y que sale de una app en el móvil (Google Authenticator, Aegis,
1Password, la que sea).

1. En la misma pestaña, bajar hasta **Verificación en dos pasos**.
2. Escribir la contraseña y pulsar **Activar…**.
3. Aparece un código QR. Abrir la app de verificación en el móvil, darle a añadir
   cuenta y escanearlo. Si no se puede escanear, teclear a mano el texto que sale
   debajo del QR.
4. La app empieza a mostrar un código de seis dígitos. Escribirlo en la casilla y
   pulsar **Activar**.

A partir de ahí, cada vez que se entre se pedirá la contraseña y después ese
código. Para desactivarlo hacen falta la contraseña y un código válido.

**Si se pierde el móvil.** Se entra con la clave de recuperación en papel (la de
§3.3, ahora sí): al hacerlo, la verificación en dos pasos se apaga y hay que
volver a configurarla con el móvil nuevo. Por eso el papel sigue siendo
imprescindible aunque se use el segundo factor.

**La hora tiene que estar bien.** El código depende del reloj: si el del ordenador
o el del móvil va desajustado más de medio minuto, el código se rechaza. Con la
hora automática activada en ambos no hay problema.

### 3.5 Conectar Google

Sirve para tres cosas: meter las sesiones en el calendario, crear los enlaces
de Meet, y subir las copias de seguridad a Drive.

Se conecta desde **Administración › Conexiones** (o en la pantalla del primer
arranque, §2) cargando el archivo de credenciales `client_secret.json`. Se abre
el navegador, se acepta con la cuenta de la consulta, y ya queda.

**Qué ve Google y qué no.** En el calendario solo aparece una etiqueta del tipo
`Sesión · AR-3f9c1b`: nunca el nombre del paciente ni el motivo. El paciente no
se añade como invitado del evento. Las copias que suben a Drive van cifradas:
Google recibe bytes que no puede leer.

### 3.6 Informes de diagnóstico

En **Administración › Diagnóstico** está el registro de fallos técnicos que la
aplicación recoge sola: una copia que no se pudo hacer, Google que no responde,
un error inesperado. En cada arranque se manda un informe con lo nuevo al
correo de quien mantiene la aplicación, **sin que haya que pulsar nada**.

El informe **no lleva datos de pacientes**: solo el tipo de fallo, la traza
técnica y datos del equipo (versión, sistema, espacio en disco). Desde esa
misma pestaña se puede **desactivar el envío automático** y marcar cada
incidencia como revisada. El registro no se borra.

---

## 4. El día a día

Cinco secciones a la izquierda: **Agenda**, **Pacientes**, **Facturación**,
**Resumen mensual** y **Administración**.

![Listado de pacientes, con el filtro de casos abiertos y los botones de Abrir ficha y Dar de alta](imagenes/pacientes.png)

### Dar de alta a un paciente

**Pacientes** → **Dar de alta**. Se abre una ventana: nombre, apellidos, DNI o
NIE, fecha de nacimiento, teléfono y correo (el correo es opcional, pero sin él
no se le pueden enviar avisos de cita).

![Ventana de dar de alta a un paciente](imagenes/dar-de-alta.png)

### Abrir un caso

Una persona dada de alta todavía no tiene terapia. Hay que abrirle un caso: en su
ficha se elige el **tipo de terapia** en la lista de arriba y se pulsa **Abrir
caso**. Si la terapia elegida es de pareja, pide a la otra persona, que tiene que
estar dada de alta antes.

También se puede abrir en el mismo momento del alta, marcando **Abrirle un caso al
darlo de alta**.

Las sesiones y los informes cuelgan del caso, no de la persona. Una misma
persona puede tener a la vez un caso individual y uno de pareja, y cada uno
lleva su historia y su facturación por separado.

### Cerrar un caso

Cuando la terapia termina, en la tarjeta del caso de la ficha se pulsa **Cerrar
caso** y se indica la fecha de cierre. Un caso cerrado no admite citas nuevas,
pero su historia, sus informes y sus facturas se conservan. Si hay que retomarlo,
**Reabrir** lo vuelve a activar.

Cerrar los casos hace falta, además, para poder **suprimir** la ficha más
adelante (§10): una ficha con casos abiertos no se puede suprimir.

### Registrar el consentimiento

En Pacientes, con la persona elegida: **Registrar consentimiento firmado…**, y
se adjunta el documento escaneado. Queda guardado cifrado dentro de la ficha.

---

## 5. Agenda

![Vista de Agenda con las sesiones del periodo elegido](imagenes/agenda.png)

### Agendar una sesión

En **Agenda**, el botón **+ Nueva sesión** abre una ventana: elegir el caso, la
fecha, la hora y la duración. El importe no se pide aquí: sale de la tarifa del
tipo de terapia del caso.

![Ventana de Nueva sesión, con el caso, la fecha y la hora elegidos](imagenes/nueva-sesion.png)

Para online, **Crear enlace de Meet** lo genera automáticamente al agendar. Si se
prefiere otro (Zoom, el que sea), se desmarca esa casilla y se pega el enlace en
el campo que aparece debajo.

Pulsar **Agendar**.

### Avisar al paciente

Justo después de agendar sale una ventana **Enviar la cita** con el correo ya
redactado: destinatario, asunto y mensaje, todo modificable. **Enviar al
paciente** lo manda; **Ahora no** lo deja sin enviar. La sesión queda agendada
en los dos casos: esa ventana solo decide si se avisa.

Si el paciente no tiene correo en la ficha, se puede escribir ahí mismo.

### Los colores del cobro

En la columna **Cobro**:

- **Verde**: pagada.
- **Neutro**: sin pagar, pero todavía queda margen antes de la sesión.
- **Ámbar**: sin pagar y ya dentro de las horas de aviso. Es la que hay que
  mirar.

### Cerrar una sesión

Al elegir una sesión de la lista se habilita el panel de la derecha:

- **Marcar como pagada** (y **Anular el pago** si se marcó por error).
- **Realizada**: la sesión se dio.
- **No asistió**: no vino y no avisó. Se cobra.
- **Cancelar sesión**: cancelada con menos aviso del pactado. Se cobra entera.
- **Cancelar sin cargo**: cancelada en plazo, o por fuerza mayor. No se cobra.

---

## 6. Ficha, historia clínica, informes y pruebas

Desde **Pacientes** → **Abrir ficha**.

La ficha reúne los datos de la persona, sus casos abiertos, si tiene el
consentimiento firmado, sus informes y las pruebas psicométricas que se le
hayan pasado.

### La historia clínica

Vienen ya puestas las diez secciones de la plantilla, para rellenar debajo de
cada una. Se escribe como en cualquier procesador de texto: se selecciona un
trozo y se le da formato con los botones de la barra de arriba —**Título**,
**Subtítulo**, negrita, cursiva, **Viñeta** y **Cita**—. El botón **Ver cómo
queda** enseña el resultado tal cual saldrá al guardarlo y al exportarlo.

**A tener presente** es un campo aparte, arriba. Lo que se escriba ahí se ve
nada más abrir la ficha: es para riesgo, o para cualquier cosa que no deba
pasarse por alto. Nunca se rellena solo a partir del texto de la historia.

**Guardar historia** para grabar.

### Informes

En la ficha: elegir el caso, escribir un título y **Crear informe**. Se redacta
igual, con la barra de formato y su vista previa. **Exportar a PDF…** lo saca con
el logotipo de marca de agua, si se subió uno en Administración.

### Pruebas

Pestaña **Pruebas** de la ficha. Cuelgan del caso elegido arriba, igual que los
informes.

Para registrar una: nombre del test (por ejemplo *WAIS-IV* o *BDI-II*), fecha en
que se pasó, notas o interpretación si se quiere, y **Elegir archivo y guardar**.
El archivo con el resultado (PDF, o una foto/escaneo en JPG o PNG) se guarda
cifrado dentro de la ficha; en disco no queda nada legible.

Con una prueba elegida de la lista:

- **Previsualizar** — abre el archivo en una ventana aparte: las imágenes tal
  cual y los PDF como una imagen por página. El documento se descifra en memoria,
  no se escribe en el disco.
- **Guardar copia…** — descifra el archivo y lo deja donde se diga, para
  adjuntarlo a un informe o abrirlo con otro programa.
- **Eliminar** — borra la prueba y su archivo. Queda anotado en el registro de
  accesos, como cualquier otro movimiento sobre la historia clínica.

Las pruebas entran también en el expediente que se le entrega al paciente si
ejerce su derecho de acceso.

### Cuestionarios

Pestaña **Cuestionarios** de la ficha. También cuelgan del caso elegido arriba.

Un cuestionario es una lista de preguntas con opciones y una forma de puntuarlas
(sumar, invertir los ítems de control, clasificar por tramos). Se preparan una vez
en **Administración → Cuestionarios**, importándolos desde un archivo JSON —lo
normal es pedirle a una IA que lo genere siguiendo `docs/cuestionarios.md`— y
**publicándolos**. Solo los publicados aparecen aquí.

Para pasar uno: elegir el cuestionario en el desplegable, **Cumplimentar…**,
marcar cada respuesta y **Guardar**. La aplicación suma y enseña la puntuación y
el tramo al momento. Si quedan respuestas sin marcar y el cuestionario no lo
permite, se guarda como *incompleto*.

Con un cuestionario elegido de la lista: **Ver respuestas** lo reabre en solo
lectura, se pueden editar las **notas**, y **Eliminar** lo borra (queda anotado en
el registro de accesos). También entran en el expediente del derecho de acceso.

Bitácora no interpreta clínicamente: solo cuenta y clasifica según lo que diga
cada plantilla.

---

## 7. Copias de seguridad y recuperación

### Cómo funcionan

Se hace una copia **al cerrar la aplicación, una vez al día**. Va cifrada con la
misma contraseña, y si Google está conectado sube sola a Drive, a la carpeta
«Bitácora · copias de seguridad».

La copia diaria (`bitacora-….zip`) solo lleva la base de datos: es pequeña y se
conservan los últimos días. Los documentos adjuntos (consentimientos, informes,
pruebas) se guardan **aparte, un solo ejemplar de cada uno**, en la carpeta
`copias/adjuntos` de al lado —y en su equivalente en Drive—. Así la copia de
cada día no vuelve a arrastrar los mismos documentos.

En Administración se puede forzar una con **Hacer una copia ahora**, ver las que
hay en Drive, y decidir cuántos días se conservan.

> Para llevarse una copia en un USB hay que copiar la carpeta `copias` **entera**
> (el `.zip` y la carpeta `adjuntos`), no solo el archivo. Está dentro de la
> carpeta de datos —normalmente `Documentos\Bitacora\copias`—; la ruta exacta
> aparece en **Administración**, debajo del título.

### Recuperar en un ordenador nuevo

Al abrir Bitácora por primera vez, en vez de crear la consulta:

- **Buscar en Drive…** — pide el archivo de credenciales de Google, abre el
  navegador, lista las copias que haya en Drive y se elige una. Trae también los
  documentos adjuntos.
- **Desde una carpeta…** — se apunta a la carpeta `copias` copiada entera (la del
  USB). Reconstruye la base y los documentos.
- **Desde un archivo…** — si solo se tiene el `.zip`. Recupera la consulta, pero
  sin los documentos adjuntos; avisa de cuántos faltan y se pueden traer luego de
  Drive.

Después pide la contraseña de siempre, y todo vuelve: pacientes, historias,
facturas, y también **la conexión con Google**, que viaja dentro de la copia.

### Si se olvida la contraseña

En la pantalla de entrada, **He olvidado la contraseña**. Pide el usuario, el
código de recuperación que se imprimió, y una contraseña nueva. El código se
puede escribir con guiones o sin ellos, y da igual mayúsculas o minúsculas.

Sin ese código no hay ninguna otra vía. No existe un «te enviamos un correo»:
si lo hubiera, quien entrara en el correo entraría en las historias clínicas.

Si estaba activada la verificación en dos pasos, al recuperar el acceso así se
apaga: hay que volver a configurarla (§3.4).

---

## 8. Facturación

![Pantalla de Facturación, con el desplegable de caso y el listado de facturas emitidas](imagenes/facturacion.png)

**Facturación** → elegir el caso, a quién se factura y **la sesión concreta**
→ **Emitir**.

**Cada factura es de una sola sesión.** El desplegable de sesión solo ofrece
las que están **ya dadas y ya cobradas** y que no se hubieran facturado antes;
si un caso tiene varias sesiones pendientes, hay que emitir una factura por
cada una. Una sesión sin cobrar no aparece en la lista.

La factura sale **exenta de IVA** por el artículo 20.Uno.3º de la Ley del IVA,
que es lo que corresponde a la asistencia sanitaria.

**El concepto es siempre «Terapia online».** No dice la modalidad (individual o
de pareja): esa factura puede acabar en manos de terceros y el tipo de terapia
es un dato de salud. Solo cuando se cobra una sesión a la que el paciente no
asistió, o una cancelación fuera de plazo, se añade «(sesión no realizada)» para
que se entienda el cargo.

**Una factura emitida no se edita.** Si hay un error, se corrige con **Emitir
rectificativa**, que es lo que exige la normativa. **Exportar a PDF…** la saca
para enviarla.

---

## 9. El resumen para la gestoría

![Resumen mensual, con las citas por estado y el detalle de cobros del mes](imagenes/resumen-mensual.png)

**Resumen mensual** → elegir el mes. Sale lo que suele pedir la gestoría cada mes:
cuántas sesiones hubo por estado (realizadas, no asistió, canceladas…), el total
cobrado, y el detalle de cada cobro.

**Va por lo cobrado, no por lo facturado.** Si una sesión de agosto se cobró en
agosto pero no se factura hasta septiembre, cuenta en el resumen de agosto — el
mes en que entró el dinero, no el mes de la factura. No hace falta tener las
facturas al día para sacar el resumen.

El detalle de cada cobro lleva la fecha, el nombre, el NIF y la dirección de
quien paga, y el importe: los mismos datos que llevaría la factura, aunque esa
sesión todavía no se haya facturado. Es lo que la gestoría necesita para
declarar el ingreso.

**No aparece el tipo de terapia.** Ni en el recuento de citas ni en el detalle de
cobros: el documento va a un tercero (la gestoría) y cruzar a una persona con una
modalidad de terapia sería darle un dato de salud que no necesita para su trabajo.

**Exportar a PDF…** lo saca ya con los datos fiscales y el logotipo, listo para
enviarlo.

---

## 10. Cosas que conviene saber

**No mover la carpeta de datos a Drive, OneDrive ni Dropbox.** La aplicación lo
impide a propósito: la sincronización continua corrompe la base de datos. A la
nube van las copias, que para eso están.

**El registro de accesos** (Administración → Ver el registro…) deja constancia
de cada consulta y cada cambio en una historia clínica. Es una obligación legal
y solo se puede mirar, no borrar.

**Suprimir una ficha** no la borra: deja de tratarse y se borran teléfono y
correo de inmediato, pero los datos se conservan **cinco años**, que es el
mínimo que exige la Ley 41/2002. Ese plazo se cuenta desde el **cierre del
último caso** de la persona (por eso hay que cerrarlos antes de suprimir), no
desde el día de la supresión. Pasado el plazo, **Destruir las caducadas** en
Administración las elimina de verdad.

**Bloqueo por intentos.** Cinco contraseñas fallidas seguidas bloquean el
acceso un rato. Es a propósito. Los códigos de verificación fallidos cuentan
igual.
