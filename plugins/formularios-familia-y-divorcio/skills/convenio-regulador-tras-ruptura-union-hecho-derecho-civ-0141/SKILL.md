---
name: convenio-regulador-tras-ruptura-union-hecho-derecho-civ-0141
description: "Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán)

> Formulario **CIV-0141** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Acuerdo alcanzado sobre convenio regulador después del cese de la convivencia estable en pareja conforme a Derecho civil especial de Cataluña

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-tras-ruptura-union-hecho-derecho-civ-0141`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] IMPORTE (4 veces)
- [ ] CALLE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] AÑOS (PERIODO)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE HIJOS

## Normas que cita el formulario

- art. 233 Código Civil
- art. 234 Código Civil

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

Doña [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], con domicilio en la calle [CALLE], de [LOCALIDAD] y con D.N.I. n.º [NÚMERO].

Y DE OTRA,

Don [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], con domicilio en la calle [CALLE], de [LOCALIDAD] y con D.N.I. n.º [NÚMERO].

Actúan ambas partes en nombre e interés propio y se reconocen recíprocamente la capacidad legal necesaria para el presente otorgamiento y, de sus libres y espontáneas voluntades

EXPONEN

I.- Que Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] han convivido como pareja estable entre los años [AÑOS (PERIODO)], manteniendo una relación cuasi conyugal equiparable a un matrimonio.

II.- Que fruto de esta relación afectiva, tienen [Nº DE HIJOS] hijos, nacidos el día [FECHA], respectivamente.

III.- Que ambas partes han decidido poner fin a su vida en común y con la finalidad de regular los efectos derivados del cese de su convivencia otorgan el presente Convenio Regulador de conformidad a los siguientes,

PACTOS

Primero.- Cese de la convivencia

Ambas partes acuerdan su separación dando totalmente por finalizada la relación de hecho mantenido hasta ahora.

Segundo.- Vivienda y ajuar doméstico

En cuanto a la atribución de la vivienda que constituía hasta ahora el domicilio de ambos, se atribuye el uso de la misma a Doña [NOMBRE Y APELLIDOS] por ser de su propiedad.

Don [NOMBRE Y APELLIDOS] fijará su domicilio donde estime conveniente, comunicándose ambas partes mutuamente cualquier cambio de domicilio.

En cuanto a los muebles y demás enseres que se encuentran en la vivienda, quedarán atribuidos a Doña [NOMBRE Y APELLIDOS], habiendo ya retirado Don [NOMBRE Y APELLIDOS] sus bienes privativos.

Tercero.- Plan de parentalidad

Las partes acuerdan el siguiente Plan de parentalidad para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación de los hijos comunes, conforme a lo establecido en el art. 233-9 del Código Civil de Cataluña: (véase modelo de Plan de parentalidad)

Cuarto.- Alimentos para los hijos menores

Teniendo en cuenta sus necesidades ordinarias y extraordinarias se fija en [IMPORTE] euros ( [IMPORTE] €) mensuales la cantidad a satisfacer en concepto de contribución del padre a los alimentos para sus hijos. Dicha cantidad será ingresada mensualmente, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta corriente que la madre designe.

Esta cantidad será revisada anualmente en proporción a las variaciones del Índice de Precios al Consumo General que publique el Instituto Nacional de Estadística o cualquier otro organismo público que en el futuro pudiera cumplir análoga misión.

[OPCIONAL — incluir si procede]

(Seleccionar en caso de fijarse garantías para el pago

Se fijan las siguientes garantías para su pago:

Quinto.- Régimen de relaciones personales con los abuelos

Por lo que respecta al régimen de relaciones personales con los abuelos, se fija lo siguiente:

Sexto.- Prestación alimentaria y compensación económica

. En atención a lo establecido en el art. 234-10.1 a) del Código Civil de Cataluña se establece a cargo de Don [NOMBRE Y APELLIDOS] una prestación alimentaria mensual en favor de Doña [NOMBRE Y APELLIDOS] de [IMPORTE] euros que tendrá una duración de tres años a partir de la firma de este documento, de conformidad con lo establecido en el art. 234-11.3 del citado Código, y se actualizará anualmente de acuerdo con la variación del IPC. Las cantidades que resultan de este pacto se harán efectivas por mensualidades anticipadas antes del día 5 de cada mes, mediante el ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)].

Del mismo modo, de acuerdo con lo que dispone el art. 234-9 del Código Civil de Cataluña, Don [NOMBRE Y APELLIDOS] pagará a Doña [NOMBRE Y APELLIDOS] una compensación de [IMPORTE] euros por los años de convivencia y por la contribución de ésta en casa y por los años que ha trabajado en el negocio familiar.

. Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] acuerdan no efectuarse reclamación alguna por estos conceptos.

Séptimo.- División del patrimonio común

. No procede acordar nada sobre esta cuestión dado que no existen bienes en pro indiviso.

En caso de que existan bienes en comunidad ordinaria, puede incluirse una cláusula acordando la liquidación de la comunidad ordinaria de bienes ostentada ("Los saldos existentes en las dos cuentas corrientes de las que son cotitulares indistintos ambos miembros de la pareja estable, acuerdan repartírselos por mitades"), o indicarse que se quiere permanecer en la indivisión ("El único patrimonio común de la pareja estable lo constituye [DESCRIPCIÓN DEL BIEN], acordando las partes por el momento mantener la copropiedad del mismo")

Octavo.- Vigencia del convenio regulador

Ambas partes se comprometen a cumplir estos pactos desde este acto; se obligan a formular de común acuerdo demanda de adopción de los efectos derivados del cese de la convivencia, ante el Tribunal competente, y a ratificar la petición y este convenio.

Noveno.- Indemnizaciones y costas del juicio

Todas las estipulaciones del presente convenio constituyen un conjunto negocial indivisible, por lo que sólo se entienden consentidas en cuanto sean todas ellas aprobadas en su integridad, sin supresión, adición ni alteración alguna.

Mediante el cumplimiento de estas prestaciones ambas partes se obligan a nada más pedir ni exigir.

En cuanto a las costas, cada parte abonará los honorarios de su respectivo Letrado, si bien acuerdan que los honorarios de Procurador que se devenguen por el juicio sean pagados por Don [NOMBRE Y APELLIDOS].

Décimo.- Compromiso general

Ambas partes se comprometen a cumplir bien y fielmente el presente convenio, a guardarse recíproco respeto, así como evitar cualquier actitud o maledicencia que pueda afectar al merecido respeto público de que ambos son acreedores.

Asimismo, las partes se comprometen a interpretar este convenio tomando siempre en consideración el interés y protección de los menores, y a evitar cualquier actitud que afecte el cariño y respeto de los hijos hacia ambos padres.

El presente convenio surte efectos entre las partes desde el día de hoy, y para que así conste, lo firman por duplicado en el lugar y fecha "ut supra".

Firmado	Firmado
D. Dña. [NOMBRE Y APELLIDOS]

========================================================================
