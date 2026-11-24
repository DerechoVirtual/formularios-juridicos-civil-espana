---
name: contestacion-empresa-arbitraje-alegando-reclamante-no-civ-1779
description: "Contestación de la empresa al arbitraje alegando que el reclamante no es consumidor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación de la empresa al arbitraje alegando que el reclamante no es consumidor

> Formulario **CIV-1779** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación de la empresa al arbitraje alegando que el reclamante no es consumidor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación de la empresa al arbitraje alegando que el reclamante no es consumidor” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:contestacion-empresa-arbitraje-alegando-reclamante-no-civ-1779`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] FECHA
- [ ] IMPORTE
- [ ] NOMBRE Y APELLIDOS
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

D./Dª. [NOMBRE Y APELLIDOS], con D.N.I. [DNI/NIE], legal representante de la empresa [DENOMINACIÓN SOCIAL], lo cual acredito mediante el documento adjunto acompañado como número 1, con domicilio en calle [CALLE] de [LOCALIDAD] (correo electrónico [CORREO ELECTRÓNICO] o fax [Nº DE FAX]), el cual se designa a efectos de notificaciones, en nombre de la empresa que representa EXPONE:

1) Que en fecha [FECHA] he recibido reclamación formulada por [ÓRGANO O PERSONA] en solicitud de la cantidad de [IMPORTE] euros

2) Que mi representada está adherida al sistema arbitral de consumo.

3) Y que, estando en total disconformidad con la reclamación formulada, en el plazo establecido en el 36.2 del Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo, da contestación a dicha solicitud, mediante este escrito se funda en los siguientes:

HECHOS Y FUNDAMENTOS

Con carácter previo, nos oponemos a la solicitud por cuanto el reclamante no tiene la condición de consumidor, requisito necesario para que pueda instar el arbitraje de consumo previsto en el art. 57 del TR de la Ley de Consumidores y Usuarios y en los artículos 1.2 y 31 del RD 713/2024.

El artículo 3.1 del TR de la Ley de 2007 define al consumidor como la persona física o jurídica que actúa en un ámbito ajeno a su actividad empresarial o profesional.

En la presente reclamación, el solicitante es una persona que está actuando en el ámbito de su actividad empresarial o profesional, por cuanto, tal como se observa en el contrato aportado por el mismo, contrató ocho líneas telefónicas para la realización su actividad empresarial o profesional, lo cual no es compatible con la condición de consumidor, según viene siendo interpretado por el Tribunal Supremo, entre otras, en SS. 23 de septiembre de 2004 y de 15 de diciembre de 2005.

En consecuencia, no ostentando la condición de consumidor el reclamante y, por tanto, no encontrándose en el ámbito de aplicación del Sistema Arbitral de Consumo, conforme disponen los citados artículos 57 del TR y 1.2 y 31 del RD 713/2024, procede decretar la inadmisión de la solicitud sin entrar a conocer del fondo del asunto.

De forma subsidiaria, y para el caso que se admitiera la solicitud, rechazamos los hechos y fundamentos alegados por el reclamante.

La facturación realizada se ajusta a lo pactado en el contrato y a las normas aplicables, resultando que los consumos se midieron por aparatos homologados y con todos los requisitos de fiabilidad (se acompañan certificados del personal técnico de la empresa en relación a las homologaciones y lecturas de los aparatos en relación al consumo correspondientes a las líneas del reclamante, así como de las tarifas aplicables por mi representada).

El reclamante únicamente alega un pico de consumo excesivo en los dos meses impugnados y en comparación al consumo de otros meses; ello no obstante, ninguna prueba aporta que no realizara efectivamente ese consumo en esos dos meses, ni tampoco niega haber realizado ninguna de las llamadas registradas en sus facturas, de lo que se deduce la falta de fundamento de su reclamación, por lo que solicitamos su desestimación.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA JUNTA ARBITRAL que tenga por formulada esta contestación y, tras los trámites legales y de conformidad a lo expuesto en este escrito, inadmita la solicitud del reclamante por no ostentar la condición de consumidor o, subsidiariamente, dicte laudo desestimando íntegramente la reclamación presentada de contrario.

Firmado:

========================================================================
