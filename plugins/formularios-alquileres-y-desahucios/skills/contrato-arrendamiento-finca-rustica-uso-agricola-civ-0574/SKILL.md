---
name: contrato-arrendamiento-finca-rustica-uso-agricola-civ-0574
description: "Contrato de arrendamiento de finca rústica para uso agrícola. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de finca rústica para uso agrícola

> Formulario **CIV-0574** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento de una finca rústica, en el que se detallan las circunstancias y estipulaciones necesarias para llevar a cabo el arrendamiento, así como los derechos y obligaciones tanto del arrendador como del arrendatario.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de finca rústica para uso agrícola» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de finca rústica para uso agrícola” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-finca-rustica-uso-agricola-civ-0574`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] IMPORTE
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] MUNICIPIO
- [ ] NOMBRE DE LA FINCA
- [ ] Nº DE DÍAS
- [ ] REFERENCIA CATASTRAL
- [ ] SUPERFICIE
- [ ] TOMO

## Normas que cita el formulario

- art. 12 Ley 49/2003
- art. 13 Ley 49/2003
- art. 24 Ley 49/2003
- art. 1542 Ley 49/2003

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del ARRENDADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del ARRENDATARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ARRENDAMIENTO RÚSTICO y, a tal fin,

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es dueño de la finca que a continuación se indica, como consecuencia de título de compraventa, constando inscrita en el Registro de la Propiedad de [LOCALIDAD], al Tomo [TOMO], se la conoce con el nombre de [NOMBRE DE LA FINCA], en el término municipal de [MUNICIPIO], carretera de [LOCALIDAD], linda al norte con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], al sur con D./Dña. [NOMBRE Y APELLIDOS], al este con D./Dña. [NOMBRE Y APELLIDOS] y al oeste con D./Dña. [NOMBRE Y APELLIDOS], tiene una superficie de [SUPERFICIE] Hectáreas, y su destino principal es la siembra de productos cereales, estando libre de cargas, arrendamientos, gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto.

Referencia catastral: [REFERENCIA CATASTRAL].

II.- Que el Sr./Sra. D./Dña. [NOMBRE Y APELLIDOS], solicita se le arriende el mencionado inmueble, a lo que accede el arrendador y lo llevan a efecto de conformidad con las siguientes,

CLÁUSULAS

Primera.- Que D./Dña. [NOMBRE Y APELLIDOS], es dueño de la finca descrita en el apartado I) del presente documento y está interesado en arrendar y arrienda a D./Dña. [NOMBRE Y APELLIDOS], quien a su vez acepta el arriendo de la finca de referencia en este contrato.

Segunda.- El arrendatario tiene derecho a determinar el tipo de cultivo, sin perjuicio de su obligación de devolver la finca, al terminar el arriendo, en el estado en que la recibió y de lo dispuesto sobre mejoras en la Ley 49/2003 de 26 de noviembre, de Arrendamientos Rústicos, pudiendo contratar siempre a su cargo, con completa indemnidad para la otra parte, a las personas que considere necesarias para ayudarle en la explotación.

Tercera.- El presente arrendamiento se conviene y concierta por plazo mínimo de cinco años, en conformidad con el artículo 12 de la Ley 49/2003, de 26 de noviembre, de Arrendamientos Rústicos, y el arrendador podrá recuperar la finca al término del plazo contractual, notificándolo fehacientemente al arrendatario con un año de antelación.

Cuarta.- El precio o renta inicial de este contrato se fija en [IMPORTE] euros ( € [IMPORTE EN LETRA]) anuales, pagaderos por años vencidos, dentro de los [Nº DE DÍAS] primeros días del mes de [MES], fijándose como domicilio para el pago el domicilio del arrendador, y se actualizará para cada anualidad por referencia a la variación anual del Índice de Garantía de Competitividad, de conformidad con el artículo 13 de la Ley 49/2003, de 26 de noviembre, de arrendamientos rústicos. El arrendador se compromete a entregar al arrendatario un recibo acreditativo del pago.

Todas las cantidades que hubiese de pagar el arrendador y que por disposición legal sean repercutibles al arrendatario podrán ser exigidas por aquél desde el momento en que las haya satisfecho, expresando el concepto, importe y disposición que autorice la repercusión. El impago de tales cantidades equivaldrá al impago de la renta. El derecho a repercutir prescribirá al año de haberse efectuado el pago por el arrendador.

Quinta.- Si el arrendador no recobra la finca conforme a lo establecido en la estipulación tercera de este contrato, salvo que el arrendatario ponga la posesión de la finca arrendada a disposición del arrendador al término del plazo, se entenderá el contrato tácitamente prorrogado por un período de cinco años. Tales prórrogas se sucederán indefinidamente en tanto no se produzca la denuncia del contrato.

El arrendatario por su parte podrá dar por extinguido el contrato al término de cada año agrícola, notificándoselo al arrendador con un año de antelación.

Sexta.- El arrendatario no podrá ceder o subarrendar la finca o explotación sin el consentimiento expreso del arrendador. Dicho consentimiento no será necesario cuando la cesión o subarriendo se efectúe a favor del cónyuge o de uno de los descendientes del arrendatario. No obstante, el subrogante y el subrogado notificarán fehacientemente al arrendador la cesión o el subarriendo, en el plazo de 60 días hábiles a partir de su celebración.

La cesión y el subarriendo habrán de referirse a la totalidad de la finca o explotación y se otorgarán por todo el tiempo que reste del plazo del arrendamiento por una renta que no podrá ser superior a la pactada entre el arrendador y el arrendatario.

Séptima.- El arrendatario se compromete a suscribir una póliza de seguros contra riesgos catastróficos corriendo a su cargo el pago de las primas que derive, y que deberá cubrir al menos el doble de la cantidad que se ha pactado en este arrendamiento.

Octava.- En caso de incumplimiento, el arrendador podrá instar el desahucio por falta de pago y serán de cargo del arrendatario todos los gastos y costas judiciales y extrajudiciales que origine su incumplimiento, incluso honorarios de Letrado y Procurador aunque la intervención de éstos no fuere preceptiva.

Novena.- El arrendamiento terminará, además de por el motivo previsto en el punto anterior, por alguna de las causas previstas en los artículos 24 y 25 de la Ley 49/2003, de 26 de noviembre, de Arrendamientos Rústicos.

Décima.- En todo lo no dispuesto en el presente contrato se estará a lo dispuesto en el Código Civil, en sus arts.1542 y siguientes, y en la Ley 49/2003 de 26 de noviembre, de Arrendamientos Rústicos.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un solo efecto.

En [LUGAR], a [FECHA].

ARRENDADOR

ARRENDATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
