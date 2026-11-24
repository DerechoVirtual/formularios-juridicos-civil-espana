---
name: decreto-admite-demanda-filiacion-presentada-madre-hijo-civ-2140
description: "Decreto que admite la demanda de filiación presentada por la madre del hijo menor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que admite la demanda de filiación presentada por la madre del hijo menor

> Formulario **CIV-2140** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto admitiendo a trámite la demanda sobre determinación legal de la filiación, interpuesta por la madre del hijo menor de edad.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que admite la demanda de filiación presentada por la madre del hijo menor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que admite la demanda de filiación presentada por la madre del hijo menor” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-admite-demanda-filiacion-presentada-madre-hijo-civ-2140`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] FOLIO
- [ ] GRUPO
- [ ] LUGAR
- [ ] TOMO

## Normas que cita el formulario

- art. 264.2.º LEC
- art. 133 CC
- art. 765 LEC
- art. 766 LEC
- art. 749.1 LEC
- art. 37 LEC
- art. 50.1 LEC
- art. 767.1 LEC
- art. 753 LEC
- art. 496 LEC
- art. 750 LEC

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

DECRETO DEL LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

Sr./a. Letrado de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.- Por la Procuradora Sr./a. [NOMBRE Y APELLIDOS], que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], se ha presentado demanda sobre determinación legal de la filiación de su hijo menor [NOMBRE Y APELLIDOS], nacido el [FECHA] e inscrito su nacimiento en el Registro Civil de [LOCALIDAD], al tomo [TOMO], folio [FOLIO].

SEGUNDO.- La demanda se formula frente a D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO]

TERCERO.- Se aportan como elementos de principio de prueba siete cartas manuscritas del demandado dirigidas a Dña. [NOMBRE Y APELLIDOS], dos juegos de fotografías de señaladas ocasiones, la copia de un contrato de arrendamiento de vivienda, dos certificaciones de una entidad bancaria, etc..

RAZONAMIENTOS JURÍDICOS

PRIMERO.- Examinada la anterior demanda, se estima, a la vista de los datos y documentos aportados, que la parte demandante reúne los requisitos de capacidad, representación y postulación procesales, necesarios para comparecer en juicio conforme a lo determinado en los arts. 6, 7, 23, 31 y 750.1 LEC.

SEGUNDO.- Asimismo, conforme a lo que la demanda acredita (art. 264.2.º LEC), tiene la demandante legitimación para promover la presente pretensión de determinación legal de filiación extramatrimonial sin posesión de estado, conforme al art. 133 CCiv, en relación con el art. 765 LEC, y la tiene el demandado D./Dña. [NOMBRE Y APELLIDOS], conforme al art. 766 LEC y el Ministerio Fiscal (art. 749.1 LEC).

TERCERO.- Vista la pretensión formulada en la demanda, y el partido a que extiende su competencia territorial este Tribunal, tiene jurisdicción y competencia objetiva para conocer de la misma, según los arts. 37, 38 y 45 LEC, y por tener en esta circunscripción su domicilio la parte demandada, se respeta el fuero general de las personas físicas de art. 50.1 LEC.

CUARTO.- Cumple asimismo la demanda la exigencia de admisibilidad dispuesta por el art. 767.1 LEC, propia de la que se deduce en pretensiones de filiación, consistente en un principio de prueba de los hechos en que se fundan aquéllas, puesto que los elementos aportados por la parte actora y que han sido reseñados en el ordinal tercero de los antecedentes de esta resolución, se estiman suficientes para abonar la seriedad del derecho deducido, sin prejuzgar el resultado definitivo del proceso.

QUINTO.- Lo expuesto indica la procedencia de admitir a trámite la demanda, que se sustanciará en juicio especial con arreglo a los trámites del juicio verbal, según lo dispuesto en el art. 753 LEC, confiriendo traslado de la misma al Ministerio Fiscal y a la parte demandada, emplazándoles, con los apercibimientos legales, para que contesten en el plazo de veinte días hábiles computados desde el siguiente al emplazamiento.

PARTE DISPOSITIVA

1.- Se admite a trámite la demanda sobre determinación legal de la filiación de [NOMBRE Y APELLIDOS], promovida por la Procurador/a Sr./a., en nombre y representación de Dña. [NOMBRE Y APELLIDOS], frente a D./Dña. [NOMBRE Y APELLIDOS] y el Ministerio Fiscal, que se sustanciará por los trámites del juicio verbal, con las modificaciones establecidas en los arts. 753, 767 y 768 LEC.

2.- Dése traslado de la demanda al Ministerio Fiscal y a la parte demandada, haciéndoles entrega de copias de la misma y de los documentos presentados, a fin de que puedan contestar a la demanda en el plazo de veinte días computados desde el siguiente al emplazamiento, bajo apercibimiento de que si no se comparece dentro de plazo se le declarará en situación de rebeldía procesal (art. 496 LEC), y que el demandado debe comparecer representado por Procurador de los Tribunales y asistido de Abogado (art. 750 LEC).

3.- Llévese a efecto el emplazamiento en el domicilio señalado por la parte actora, para lo que se empleará comunicación por correo con acuse de recibo.

4.- Devuélvase el poderdejando testimonio en autos.

Así lo acuerdo y firmo:

Firma del Letrado de la Administración de Justicia

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
