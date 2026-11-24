---
name: contestacion-empresa-solicitud-arbitraje-reconvencion-civ-1778
description: "Contestación de la empresa a la solicitud de arbitraje con reconvención contra el reclamante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación de la empresa a la solicitud de arbitraje con reconvención contra el reclamante

> Formulario **CIV-1778** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación de la empresa a la solicitud de arbitraje con reconvención contra el reclamante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación de la empresa a la solicitud de arbitraje con reconvención contra el reclamante” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:contestacion-empresa-solicitud-arbitraje-reconvencion-civ-1778`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE FAX
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

A LA JUNTA ARBITRAL DE CONSUMO DE [LOCALIDAD]

D./Dª. [NOMBRE Y APELLIDOS], con D.N.I., legal representante de la empresa, lo cual acredito mediante el documento adjunto acompañado como número 1, con domicilio en calle [CALLE] de [LOCALIDAD] (correo electrónico [CORREO ELECTRÓNICO] o fax [Nº DE FAX]), el cual se designa a efectos de notificaciones, en nombre de la empresa que representa EXPONE:

1) Que en fecha [FECHA] he recibido reclamación formulada por [ÓRGANO O PERSONA] en solicitud de la cantidad de [IMPORTE] euros

2) Que mi representada está adherida al sistema arbitral de consumo.

3) Y que, estando en total disconformidad con la reclamación formulada, en el plazo establecido en el 36.2 del Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo, da contestación a dicha solicitud, y al amparo del art. 40 del citado RD 713/2024, formula RECONVENCIÓN, mediante este escrito se funda en los siguientes:

HECHOS Y FUNDAMENTOS

Se niegan los hechos y fundamentos alegados por el reclamante.

La facturación realizada se ajusta a lo pactado en el contrato y a las normas aplicables, resultando que los consumos se midieron por aparatos homologados y con todos los requisitos de fiabilidad (se acompañan certificados del personal técnico de la empresa en relación a las homologaciones y lecturas de los aparatos en relación al consumo correspondientes a las líneas del reclamante, así como de las tarifas aplicables por mi representada).

El reclamante únicamente alega un pico de consumo excesivo en los dos meses impugnados y en comparación al consumo de otros meses; ello no obstante, ninguna prueba aporta que no realizara efectivamente ese consumo en esos dos meses, ni tampoco niega haber realizado ninguna de las llamadas registradas en sus facturas, de lo que se deduce la falta de fundamento de su reclamación, por lo que solicitamos su desestimación.

Al amparo de lo dispuesto en el art. 40 del RD 713/2024, formulamos reconvención frente al reclamante, solicitando que sea condenado a indemnizar a mi representada en la cantidad de [IMPORTE] euros, correspondientes a los consumos no pagados correspondientes a los meses de [MES] a

El reclamante está en adeudar dicha cantidad puesto que, aunque lo silencia en su reclamación, lo cierto es que mi representada siguió cumpliendo sus obligaciones contractuales, prestando el servicio en los términos pactados, en tanto que el reclamante dejó de abonar injustificadamente los recibos de consumo telefónico correspondientes al periodo referido que ascienden a la cantidad de [IMPORTE] euros. A efectos acreditativos, acompaño como documentos [Nº DE DOCUMENTO] los recibos expedidos correspondientes a dicho periodo y los certificados bancarios de devolución de dichos recibos girados a la cuenta del cliente, no habiendo sido en ningún momento abonados.

Por tanto, se formula reconvención por la cantidad de [IMPORTE] euros en concepto de recibos impagados en el periodo referido, cantidad ésta que deberá incrementarse con los intereses correspondientes.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA JUNTA ARBITRAL que tenga por formulada esta contestación, así como reconvención frente al reclamante y, tras los trámites legales y de conformidad a lo expuesto en este escrito, dicte laudo desestimando íntegramente la reclamación presentada de contrario y, estimando la reconvención formulada, condene al reclamante a indemnizar a mi representada en la cantidad de [IMPORTE] euros con más los intereses correspondientes.

Firmado:

========================================================================
