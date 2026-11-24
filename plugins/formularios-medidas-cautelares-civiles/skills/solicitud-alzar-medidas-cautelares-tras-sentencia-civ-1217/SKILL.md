---
name: solicitud-alzar-medidas-cautelares-tras-sentencia-civ-1217
description: "Solicitud de alzar medidas cautelares tras sentencia absolutoria firme y de indemnización de daños. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de alzar medidas cautelares tras sentencia absolutoria firme y de indemnización de daños

> Formulario **CIV-1217** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito del demandado, una vez firme la sentencia absolutoria, solicitando el alzamiento de las medidas cautelares adoptadas contra él (art. 745 LEC) y la apertura del incidente de liquidación de los daños y perjuicios que la medida le ha ocasionado (arts. 712 y siguientes LEC), con relación detallada de los conceptos reclamados y de los documentos que los acreditan (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de alzar medidas cautelares tras sentencia absolutoria firme y de indemnización de daños» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de alzar medidas cautelares tras sentencia absolutoria firme y de indemnización de daños” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-alzar-medidas-cautelares-tras-sentencia-civ-1217`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] FECHA (8 veces)
- [ ] Nº (8 veces)
- [ ] AÑO (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] CALLE
- [ ] COMPRADOR
- [ ] DÍA
- [ ] LA MEDIDA CAUTELAR
- [ ] MEDIDA CAUTELAR ADOPTADA
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PROFESIONAL
- [ ] SEDE

## Normas que cita el formulario

- art. 745 LEC
- art. 742 LEC
- art. 713 LEC
- art. 712 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, obrando en nombre y representación del demandado D./Dª [NOMBRE Y APELLIDOS], según consta acreditado en autos de juicio ordinario nº [Nº DE PROCEDIMIENTO], comparezco y, como mejor proceda en derecho, DIGO:

Que habiéndose dictado sentencia absolutoria en este proceso en fecha [FECHA], declarada firme por resolución de fecha [FECHA], por medio de este escrito y al amparo de lo que dispone el artículo 745 de la LEC, solicito el alzamiento de las medidas cautelares adoptadas en este proceso en auto de fecha [FECHA] y el resarcimiento de los daños y perjuicios ocasionados a mi representado, en base a los siguientes

HECHOS Y FUNDAMENTOS

Procedencia del alzamiento de las medidas

Que, habiéndose declarado firme la sentencia de fecha [FECHA] dictada en este proceso, por la que se absuelve a mi representado de la demanda formulada de contrario, intereso que se alcen las medidas cautelares adoptadas a la mayor brevedad, si no se ha adoptado de oficio dicha resolución por el Letrado de la Administración de Justicia, tal como dispone el artículo 745 de la LEC.

Solicitud de daños y perjuicios

La medida adoptada en la pieza de medidas cautelares ([MEDIDA CAUTELAR ADOPTADA: p. ej., embargo preventivo / anotación preventiva de demanda]) ha ocasionado unos daños y perjuicios a mi representado que se reclaman en este escrito, al amparo de lo dispuesto en el artículo 745 en relación con el artículo 742 de la LEC, y que son directamente imputables a la adopción de la medida.

En efecto, consta que la medida cautelar adoptada al tiempo de iniciarse el pleito principal fue [DESCRIPCIÓN DE LA MEDIDA: p. ej., la anotación preventiva de la demanda en el Registro de la Propiedad, en concreto en la finca sita en la calle [CALLE] de la localidad de [LOCALIDAD]], que se acordó por auto de fecha [FECHA]. Transcurridos más de [NÚMERO] años, la medida ha seguido pendiente, lo que ha imposibilitado a mi mandante [PERJUICIO CAUSADO: p. ej., la venta de dicha finca en una época en que el mercado inmobiliario estaba en un ciclo alcista, habiendo tenido que recurrir a financiación externa para continuar con su actividad empresarial].

Relación detallada de daños y documentos acreditativos

Los daños y perjuicios sufridos por la medida se fijan en [IMPORTE] euros, según se desprende de la liquidación que se acompaña individualizada como documento [Nº], relatándose detalladamente a continuación, de conformidad con lo dispuesto en el artículo 713 de la LEC:

1) En concepto de compensación por el menor valor del precio de la finca en el año [AÑO], la cantidad de [IMPORTE] euros. Dicha cantidad resulta de la diferencia entre el precio de [IMPORTE] euros en el cual mi mandante había concertado su venta en el año [AÑO], la cual se vio imposibilitada por la pendencia de [LA MEDIDA CAUTELAR] sobre la reseñada finca registral, y el precio actual de [IMPORTE] euros.

Para acreditar este concepto aporto como documento número [Nº] precontrato de venta de la finca suscrito en el año [AÑO] con [COMPRADOR], donde se fijaba el precio de venta de [IMPORTE] euros, condicionado a que se alzara la medida decretada en este proceso. Como documento número [Nº] aporto dictamen pericial elaborado por [PROFESIONAL] Sr./Sra. [NOMBRE Y APELLIDOS], en el cual se realiza un estudio de los precios de mercado actuales, concluyendo que la finca tiene un valor real de mercado de [IMPORTE] euros.

2) En concepto de intereses se reclama la cantidad de [IMPORTE] euros, correspondiente al interés legal de la cantidad arriba expresada, de la cual no pudo disponer mi mandante, viéndose obligado a concertar una póliza de crédito en fecha [FECHA], al tiempo en que se iba a realizar la venta, por importe de [IMPORTE] euros, debiendo abonar los correspondientes intereses de la misma.

Para acreditar este concepto aporto liquidación de intereses como documento [Nº] y copia de la póliza concertada por mi mandante en fecha [FECHA] como documento [Nº].

Por todo ello, los daños y perjuicios ocasionados se estiman en el importe de [IMPORTE] euros, según lo expuesto, a la que se acompañan los documentos antes relacionados, del [Nº] al [Nº], solicitando que se proceda a su liquidación conforme a lo establecido en los artículos 712 y siguientes de la LEC.

Por todo lo expuesto,

SOLICITO AL TRIBUNAL: Que admita este escrito con el justificante del traslado y, en méritos de las alegaciones que se vierten, se proceda al alzamiento de la medida cautelar de [MEDIDA CAUTELAR ADOPTADA] acordada por auto de fecha [FECHA]. Asimismo, se interesa que se abra el incidente contemplado en el artículo 712 de la LEC a los efectos de liquidar los daños y perjuicios ocasionados al demandado, que se estiman en el importe de [IMPORTE] euros según se desprende de la liquidación que se acompaña individualizada y por conceptos, a la que se acompañan los documentos e informes justificativos, solicitando que, previos los trámites legales, se fije la citada cantidad de [IMPORTE] euros como daños y perjuicios sufridos por mi representado, condenando al demandante a su pago.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Abogado: ______________________

Firma Procurador: ______________________
