---
name: contrato-privado-deudor-cede-credito-acreedor-saldar-civ-2596
description: "Contrato privado por el que el deudor cede un crédito a su acreedor para saldar la deuda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato privado por el que el deudor cede un crédito a su acreedor para saldar la deuda

> Formulario **CIV-2596** del plugin **Contratos civiles y consumo** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 25-11-2026.

## Qué es

Documento privado de cesión crédito entre un acreedor y su deudor, en el que este último, con el fin de cancelar su deuda, transmite al acreedor un crédito que ostenta a su favor frente a un tercero.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato privado por el que el deudor cede un crédito a su acreedor para saldar la deuda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato privado por el que el deudor cede un crédito a su acreedor para saldar la deuda” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-privado-deudor-cede-credito-acreedor-saldar-civ-2596`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles y consumo) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] COMPLETAR (6 veces)
- [ ] CALLE (4 veces)
- [ ] ENTIDAD BANCARIA (4 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (2 veces)
- [ ] CLASE
- [ ] ESTADO CIVIL
- [ ] LETRA
- [ ] NOMBRE DEL NOTARIO
- [ ] PISO

## Normas que cita el formulario

- art. 1526 Código Civil

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

- Al principio del formulario: Jurisprudencia de las notas: se han localizado la STS 17-12-1994 (ECLI:ES:TS:1994:19263, con el pasaje citado), la STS 5-3-1994 (ECLI:ES:TS:1994:14855), la STS 24-3-2000 (ECLI:ES:TS:2000:2383) y la STS 24-9-1993 (ECLI:ES:TS:1993:6221). El resto de la lista (27-2-1891 o 27-2-1981, que el formulario cita de las dos formas; 28-10-1957; 7-7-1958; 5-11-1974; 11-1-1983; 13-2-1988; 27-9-1991; 19-2-1993; 22-2-1994; 20-2-1995) no se ha comprobado (sin comprobar).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Documento privado de cesión crédito entre un acreedor y su deudor, en el que este último, con el fin de cancelar su deuda, transmite al acreedor un crédito que ostenta a su favor frente a un tercero.

Notas al pie del formulario original:
(1) Tanto estos, como los siguientes actos, negocios o contratos, son susceptibles de otorgamiento en documento público y en privado. Por ello, los alternamos.

(2) En cuanto a su concepto, naturaleza jurídica y finalidad, establece nuestro Tribunal Supremo que el contrato de cesión de créditos «representa un negocio bilateral en virtud del cual el acreedor-cedente transfiere por actos «inter vivos» la titularidad de su crédito a un tercero cesionario, con lo que el crédito se le hace circular arts 1526 y siguientes del Código Civil.», siendo preciso «reunir la efectiva condición de acreedor» [STS. 17.12.1994 y 24.3.2000] y siendo, en definitiva, el alcance de esta figura el de «obligar al deudor crediticio con un nuevo acreedor en virtud de un negocio bilateral que vincula a cedente y a cesionario STS 5.3.1994.

Para su validez y eficacia, la cesión de créditos no necesita ni el consentimiento ni el conocimiento del deudor cedido Ss. TS. 27.2.1891; 28.10.1957; 7.7.1958; 5.11.1974; 11.1.1983 13.2.1988 27.9.1991 19.2.1993, Rec. 1873/1990, 24.9.1993, Rec. 66/1991, 22.2.1994, 20.2.1995, Rec. 3559/1991 y 24.3.2000, Rec. 2987/1995, si bien el conocimiento por el deudor cedido sí influye en el cumplimiento, habida cuenta que si se le notifica sólo se libera de la obligación si paga al cesionario, y si no tiene conocimiento de la cesión y satisface la prestación al primitivo acreedor cedente, queda libre de su obligación y nada puede reclamar el nuevo acreedor cesionario.

En esta misma jurisprudencia se destacan los principales requisitos, consecuencias y peculiaridades de este contrato de cesión de créditos, a saber:

1.- La cesión supone una subrogación o sustitución de la persona del acreedor.
2.- La obligación permanece invariable e inalterable en su total contenido y características:

Confiere al subrogado el crédito con los derechos a él anexos [COMPLETAR]:el crédito se transmite en toda su integridad, extensión y contenido, incluidos los derechos accesorios, como la fianza, hipoteca, prenda o privilegio, sin más alteración que el cambio de personas.

3.- Oponibilidad de las excepciones que el deudor tenía frente al cedente.

«La transferencia o cesión de un crédito, aunque esté representado por el importe de una letra de cambio, no altera ni modifica su naturaleza y carácter, subrogándose el cesionario en el lugar del cedente, por lo que el cesionario civil tiene que soportar todas aquellas excepciones que le pudiera oponer directamente el deudor al crédito cedido» STS. 24.9.93, rec. 66/1991 .

COMENTARIOS DE JURISPRUDENCIA:

— La cesión de créditos puede hacerse válidamente sin conocimiento previo del deudor y aun contra su voluntad, sin que la notificación a éste tenga otro alcance que el de obligarle con el nuevo acreedor, no reputándose pago legítimo desde aquel momento el hecho a favor del cedente (Cfr. TS 1.ª SS 27 Feb. 1981, 28 Oct. 1957, 7 Jul. 1958, 5 Nov. 1974).

— El CC utiliza el mecanismo de la novación, cuando de la cesión de créditos se trata, bien lo sea activa o pasiva, esto es, de un crédito o una deuda, y así dice, en su art. 1203 CC, que las obligaciones pueden modificarse sustituyendo la persona del deudor o subrogando a un tercero en los derechos del acreedor, y aunque para la doctrina moderna sea un acto o negocio abstracto, es lo cierto que la cesión es el modo operativo de la transmisión de obligaciones, a cuya virtud el cedente desaparece de la relación jurídica transmitida, mientras el cesionario ocupa su puesto mediante la subrogación, si lo es de créditos, o la asunción, si lo es de deudas; con ello hay un cambio en los elementos personales de la relación jurídica, de tal forma que el subrogado o asumiente juntamente con el cedido pasan a constituir sus nuevos elementos de dicho orden, de la que, por tanto, desaparece el cedente, pero bien entendido que es lo único que cambia, pues en lo demás la obligación queda inalterable o invariable en su total contenido y características.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
