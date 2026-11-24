---
name: convenio-conyuges-liquidar-sociedad-gananciales-civ-0247
description: "Convenio de los cónyuges para liquidar la sociedad de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio de los cónyuges para liquidar la sociedad de gananciales

> Formulario **CIV-0247** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio de los cónyuges para liquidar la sociedad de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio de los cónyuges para liquidar la sociedad de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-conyuges-liquidar-sociedad-gananciales-civ-0247`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] FECHA (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] MES
- [ ] Nº
- [ ] TIPO DE VEHÍCULO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

EXPONEN

1) Que en fecha [FECHA] contrajeron matrimonio en [LOCALIDAD], bajo el régimen económico-matrimonial de gananciales.

2) Que, interesando a ambos cónyuges la liquidación del citado régimen económico-matrimonial y separar sus bienes, por medio del presente liquidan el referido régimen de gananciales, con arreglo a las siguientes ESTIPULACIONES:

PRIMERO.- INVENTARIO DE BIENES.

En la sociedad de gananciales, y a esta fecha [FECHA], están vigentes los siguientes derechos y obligaciones:

1) EN COPROPIEDAD INDIVISA de ambos cónyuges, piso y parking en [LOCALIDAD], fincas registrales [Nº DE FINCA] y [Nº DE FINCA] del Registro de la Propiedad de [LOCALIDAD], adquirido constante matrimonio en el año

Pesa sobre el mismo hipoteca con la entidad bancaria [ENTIDAD BANCARIA], que debe extinguirse en el año [AÑO] con un importe mensual de [IMPORTE] euros.

Este inmueble constituye la vivienda familiar.

2) DE PROPIEDAD EXCLUSIVA DE LA ESPOSA Dª [NOMBRE Y APELLIDOS], casa en [LOCALIDAD], calle [CALLE], número [NÚMERO], finca registral número [NÚMERO] del Registro de la Propiedad de

La casa, de [Nº] metros cuadrados de superficie, fue edificada sobre solar propiedad de la familia de la esposa constante matrimonio, con dinero correspondiente a la sociedad de gananciales, por importe total de [IMPORTE] euros.

3) EN COPROPIEDAD INDIVISA DE AMBOS CÓNYUGES, vehículo [TIPO DE VEHÍCULO] matrícula [MATRÍCULA], adquirido constante matrimonio en el año [AÑO]

Lo valoran ambos cónyuges de consuno en la cantidad de [IMPORTE] euros.

4) DINERO en efectivo, por importe de [IMPORTE] euros, en cuentas corrientes y depósitos en las siguientes entidades bancarias [ENTIDAD BANCARIA]

SEGUNDO.- LIQUIDACIÓN DE LA SOCIEDAD CONYUGAL.

I. ADJUDICACIONES

De acuerdo al anterior inventario, ambos cónyuges CONVIENEN:

1) Mantener pro indiviso el inmueble descrito en el apartado 1 comprometiéndose ambos esposos a sufragar por mitad la hipoteca que pesa sobre el mismo, según lo pactado en convenio regulador.

El inmueble será vendido dentro de los cinco años siguientes a que los hijos comunes se independicen, otorgándose a la esposa un derecho de adquisición preferente para su compra a precio de mercado.

2) Adjudicar a Dª [NOMBRE Y APELLIDOS] el inmueble descritos en el apartado 2, reconociendo ésta una deuda para su esposo por importe de [IMPORTE] euros correspondiente a la construcción.

3) Adjudicar al marido el vehículo descrito en el apartado 3, reconociendo ésta para su esposa una deuda de [IMPORTE] euros.

4) Repartir por mitad el dinero de las cuentas corrientes y depósitos a ambos esposos, correspondiendo a cada uno de la cantidad de [IMPORTE] euros.

II. PACTOS

De acuerdo a las anteriores adjudicaciones, y de común acuerdo por los cónyuges,

A) Se reconoce por la esposa una deuda por importe de [IMPORTE] euros a favor del marido, la cual se hará efectiva en fecha [FECHA]

B) El marido se compromete a desalojar el domicilio familiar en el plazo pactado en el convenio regulador.

C) Ambos cónyuges se comprometen a elevar el presente documento a público, así como a otorgar los documentos públicos y privados necesarios para la ejecución del presente convenio.

Y para que así conste, firman ambos cónyuges en el lugar y fecha expresados en el encabezamiento de este convenio.

========================================================================
