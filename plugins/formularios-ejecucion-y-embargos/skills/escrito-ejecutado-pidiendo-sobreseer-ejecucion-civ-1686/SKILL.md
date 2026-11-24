---
name: escrito-ejecutado-pidiendo-sobreseer-ejecucion-civ-1686
description: "Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños

> Formulario **CIV-1686** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutado solicitando del sobreseimiento de la ejecución provisional, la devolución de la cantidad percibida por la ejecutante y que se declare su derecho a ser resarcido de los daños y perjuicios ocasionados por la ejecución provisional.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutado-pidiendo-sobreseer-ejecucion-civ-1686`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] FECHA (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] IMPORTE EN LETRA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] SECCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 533.1 LEC
- art. 713.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de SEGUROS Y REASEGUROS, S.A., demandada en los autos de Juicio Ordinario n.º [NÚMERO]/[AÑO], en su pieza separada de Ejecución Provisional n.º [NÚMERO]/[AÑO] comparezco, y como mejor en Derecho proceda, DIGO:

PRIMERO.-Que el día [FECHA] ha sido notificada a esta parte la sentencia de fecha [FECHA], dictada por la Sección [SECCIÓN] de la Audiencia Provincial, con la que ha finalizado la tramitación del recurso de apelación interpuesto por nuestra representación contra la sentencia de ese Tribunal de fecha

SEGUNDO.-Como resulta del testimonio de la dicha sentencia de segunda instancia, cuyo testimonio se acompaña como documento n.º [NÚMERO], el recurso de apelación ha sido estimado íntegramente, habiendo sido revocada la sentencia de ese Tribunal, con absolución libre de mi mandante, e imposición de costas de la primera instancia.

TERCERO.-Como igualmente consta en autos, la demandante, D./Dña. [NOMBRE Y APELLIDOS], cuyas pretensiones han sido íntegramente desestimadas por la Audiencia Provincial, había solicitado la ejecución provisional de la sentencia recaída en primera instancia, lo que fue acordado por este Tribunal mediante auto de fecha [FECHA].

CUARTO.-Consecuencia de dicha ejecución nuestra representada se vio obligada a entregar a la actora, de la consignación de la condena en la cuenta del Tribunal, efectuada el [FECHA], la cantidad de [IMPORTE] euros, correspondientes a la cantidad a la que se había fijado de principal, más intereses calculados a la fecha del dictado de la sentencia revocada, según se resolvió en auto de [FECHA], que desestimó la oposición al embargo planteada por esta parte.

QUINTO.-Conforme a lo dispuesto por el art. 533.1 LEC, si el pronunciamiento provisionalmente ejecutado es de condena al pago de dinero y se ha revocado totalmente, debe sobreseerse la ejecución provisional, y la hasta ahora ejecutante, D./Dña. [NOMBRE Y APELLIDOS], deberá devolver a mi representada, hasta ahora ejecutada, la cantidad que, en su caso, hubiere percibido (en el caso de autos, [IMPORTE EN LETRA] xx [IMPORTE] euros), y reintegrarle las costas de instancia, incluidas las de la ejecución provisional, así como resarcirle de los daños y perjuicios que dicha ejecución le hubiera ocasionado.

Para la tasación de costas, se aportan minutas detalladas de honorarios del Letrado Sr./a. (documento n.º [NÚMERO]), y de los derechos y suplidos del Procurador/a. que comparece, junto con los recibos y justificantes de estos últimos (documento n.º [NÚMERO]), todos conceptos debidamente satisfechos por mi principal. Arroja total de [IMPORTE EN LETRA] yy [IMPORTE] euros.

SEXTO.-Mi mandante es mercantil que invierte su capital en activos financieros para atender a sus prestaciones, diferencia entre los frutos de sus inmovilizado e ingresos, y su exigible, que constituye su beneficio, por lo que, obligada a desprenderse de una cifra desde [FECHA], ha experimentado un lucro cesante que excede la mera retribución, como intereses legales, de la cifra de la que hubo de desprenderse injustamente, y cuya entrega se exigió por la actora de modo voluntario, cuando no es más que una facultad, que legalmente tiene apercibida esta posibilidad de deber de devolución.

A los efectos de determinar la indemnización procedente, y conforme a lo establecido en el art. 713.1 LEC, se acompaña, señalado como documento n.º [NÚMERO], dictamen pericial emitido por el Economista, Auditor Censor Jurado de Cuentas D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] de [LOCALIDAD], que individualiza y relaciona detalladamente todos los daños y perjuicios sufridos, valorando los mismos en la suma total de [IMPORTE EN LETRA] zz [IMPORTE] euros.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito con los documentos y el dictamen que lo acompañan, y justificante de haber efectuado el traslado a la representación procesal de la parte contraria, se digne admitir uno y otros, y en su virtud, se dicte por el Letrado de la Administración de Justicia decreto de sobreseimiento de la ejecución provisional, y ordene la devolución a nuestro mandante de la cantidad percibida por la ejecutante D./Dña. [NOMBRE Y APELLIDOS], de [IMPORTE EN LETRA] xx [IMPORTE] euros, así como el reembolso de las costas de instancia, que se cifran en [IMPORTE EN LETRA] yy [IMPORTE] euros, previa tasación, y declare el derecho de mi principal a ser resarcido de los daños y perjuicios ocasionados por la ejecución provisional, fijando la indemnización en la suma de [IMPORTE] zz [IMPORTE] euros, previo procedimiento de liquidación.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
