---
name: convenio-regulador-ruptura-pareja-hecho-hijos-menores-civ-0355
description: "Convenio regulador de la ruptura de pareja de hecho con hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de la ruptura de pareja de hecho con hijos menores

> Formulario **CIV-0355** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de la ruptura de pareja de hecho con hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de la ruptura de pareja de hecho con hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-ruptura-pareja-hecho-hijos-menores-civ-0355`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] CALLE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] AÑOS DE CONVIVENCIA
- [ ] IMPORTE
- [ ] LUGAR

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

Convenio regulador de los efectos derivados de la ruptura de una pareja de hecho con hijos menores y reconocimiento de la atribución de la guarda y custodia en exclusiva a la madre.

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

Doña [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], con domicilio en la calle [CALLE] y con D.N.I. n.º [NÚMERO].

Y DE OTRA,

Don [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], con domicilio en la calle [CALLE] y con D.N.I. n.º [NÚMERO].

Actúan ambas partes en nombre e interés propio y se reconocen recíprocamente la capacidad legal necesaria para el presente otorgamiento y, de sus libres y espontáneas voluntades

EXPONEN

I.- Que Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] han convivido en relación afectiva semejante al de las parejas casadas entre los años [AÑOS DE CONVIVENCIA], manteniendo una relación cuasi conyugal equiparable a un matrimonio.

II.- Que fruto de esta relación, tienen los siguientes hijos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

nacido el día [FECHA]

III.- Que ambas partes han decidido poner fin a su vida en común y con la finalidad de regular los efectos derivados del cese de su convivencia otorgan el presente Convenio Regulador de conformidad a los siguientes,

PACTOS

Primero.- Ambas partes acuerdan su separación dando totalmente por finalizada la relación de hecho mantenido hasta ahora.

Segundo.- En cuanto a la atribución de la vivienda que constituía hasta ahora el domicilio de ambos, se atribuye el uso de la misma a Doña [NOMBRE Y APELLIDOS] por ser de su propiedad.

Don [NOMBRE Y APELLIDOS] fijará su domicilio donde estime conveniente, comunicándose ambas partes mutuamente cualquier cambio de domicilio.

En cuanto a los muebles y demás enseres que se encuentran en la vivienda, quedarán atribuidos a Doña [NOMBRE Y APELLIDOS], habiendo ya retirado Don [NOMBRE Y APELLIDOS] sus bienes privativos.

Tercero.- Ambas partes pactan que, sin perjuicio de que tanto la titularidad como el ejercicio de la patria potestad siga siendo compartidos por ambos progenitores, los dos hijos queden bajo la guarda y custodia de la madre, con la que convivirán.

Se atribuye al padre un régimen de visitas amplio y flexible de forma que pueda estar con sus hijos sin ningún tipo de limitación y previo acuerdo entre ambas partes. Ello no obstante y para el caso de que no existiese acuerdo entre las partes, pactan ya desde ahora con carácter subsidiario el siguiente régimen de visitas a favor del padre:

a) Fines de semana alternos desde el viernes a la salida del colegio hasta el domingo a las 20.00 h. que lo reintegrará al domicilio de la madre.
b) La mitad de las vacaciones escolares de Navidad, Semana Santa y verano, correspondiéndole a la madre elegir la mitad que le corresponde en los años impares y al padre en los años pares.

Cuarto.- Se fija la cantidad de [IMPORTE] euros ( €) mensuales en concepto de contribución del padre a los alimentos para sus hijos. Dicha cantidad será ingresada mensualmente, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta corriente que la madre designe.

Esta cantidad será revisada anualmente en proporción a las variaciones del Índice de Precios al Consumo General que publique el Instituto Nacional de Estadística o cualquier otro organismo público que en el futuro pudiera cumplir análoga misión.

Quinto.- Todas las estipulaciones del presente convenio constituyen un conjunto negocial indivisible, por lo que sólo se entienden consentidas en cuanto sean todas ellas aprobadas en su integridad, sin supresión, adición ni alteración alguna.

Mediante el cumplimiento de estas prestaciones ambas partes se obligan a nada más pedir ni exigir.

Sexto.- Ambas partes se comprometen a cumplir bien y fielmente el presente convenio, a guardarse recíproco respeto, así como evitar cualquier actitud o maledicencia que pueda afectar al merecido respeto público de que ambos son acreedores.

Asimismo, las partes se comprometen a interpretar este convenio tomando siempre en consideración el interés y protección de los menores, y a evitar cualquier actitud que afecte el cariño y respeto de los hijos hacia ambos padres.

El presente convenio surte efectos entre las partes desde el día de hoy, y para que así conste, lo firman por duplicado en el lugar y fecha "ut supra".

Firma

Firma

D. Dña. [NOMBRE Y APELLIDOS]

========================================================================
