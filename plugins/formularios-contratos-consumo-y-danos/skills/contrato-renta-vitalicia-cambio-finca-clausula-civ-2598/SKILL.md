---
name: contrato-renta-vitalicia-cambio-finca-clausula-civ-2598
description: "Contrato de renta vitalicia a cambio de una finca con cláusula resolutoria y cláusula penal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de renta vitalicia a cambio de una finca con cláusula resolutoria y cláusula penal

> Formulario **CIV-2598** del plugin **Contratos civiles y consumo** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 25-11-2026.

## Qué es

Modelo de contrato en el que una de las partes es titular en pleno dominio de una determinada finca y se la transmite a la otra parte a cambio de una renta vitalicia. En este contrato se establece una cláusula penal en caso de incumplimiento por parte del adquirente, y las causas de resolución de esta relación contractual, así como a quien corresponde acarrear con los gastos que se deriven del presente contrato.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de renta vitalicia a cambio de una finca con cláusula resolutoria y cláusula penal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de renta vitalicia a cambio de una finca con cláusula resolutoria y cláusula penal” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-renta-vitalicia-cambio-finca-clausula-civ-2598`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles y consumo) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] COMPLETAR (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE
- [ ] PROFESIÓN

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Comprobadas STS 9-2-1990, 5-6-1991, 18-1-1996 y 11-7-1997 (esta sin poder confirmar el n.º de recurso). Las SSTS de 1930, 1956, 1959, 1960, 1962 y 1963 y las RR. DGRN de 16-10-1989 y 26-4-1991 no constan en la herramienta (sin comprobar).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de contrato en el que una de las partes es titular en pleno dominio de una determinada finca y se la transmite a la otra parte a cambio de una renta vitalicia. En este contrato se establece una cláusula penal en caso de incumplimiento por parte del adquirente, y las causas de resolución de esta relación contractual, así como a quien corresponde acarrear con los gastos que se deriven del presente contrato.

Notas al pie del formulario original:
(1) Mención de obligada observancia, tanto en documentos públicos como en privados, en los términos previstos en los artículos 38 y siguientes del Real Decreto Legislativo 1/2004, de 5 de marzo, por el que se aprueba el texto refundido del Catastro Inmobiliario.

En el caso de documentos notariales, habría que hacer constar que se incorpora para su unión a la matriz, por testimonio, y su constancia en las copias que se expidan, el documento relativo a la referencia catastral; véase artículo 47 del Real Decreto Legislativo 1/2004.

(2) Sobre la materia destacamos los siguientes aspectos de nuestra jurisprudencia:

En cuanto a su concepto: el contrato de renta vitalicia es un contrato consensual, oneroso, sinalagmático, y aleatorio en virtud del cual el deudor se obliga a pagar una pensión durante la vida de una o varias personas determinadas (acreedores) a cambio de la adquisición del dominio o cualquier otro derecho real o personal sobre determinados bienes muebles o inmuebles desde el momento en que surge la obligación de pagar la pensión.

El de renta vitalicia es un «contrato aleatorio» (art. 1802 del Código Civil), lo que significa que depende del azar tanto el tiempo de su eficacia (durante la vida del pensionista) como el número de rentas a pagar, y por tanto si la pensionista fallece pronto no puede decirse que haya en esta circunstancia enriquecimiento injusto para el deudor de la renta." [STS. 9.2.1990, 5.6.1991 y 18.1.1996]. No obstante la doctrina manifiesta que debe darse en el momento de la estipulación del contrato la llamada equivalencia del riesgo entre las partes, es decir que ambas partes deben tener igual posibilidad de pérdida o ganancia a la conclusión del contrato. Manifestación de este principio es el artículo 1804 del CC, que, aparte de establecer la nulidad del contrato de renta vitalicia constituida sobre la vida de una persona muerta (la vida de la persona que se tiene en cuenta al constituir la renta es la esencia de la aleatoriedad del contrato), establece también la nulidad del contrato de renta vitalicia que recae sobre la vida de una persona que sufre una enfermedad que le cause la muerte dentro de los veinte días siguientes a la conclusión del contrato.

La STS de 11.7.1997, rec. 2051/1993, destaca del contrato de renta vitalicia su carácter oneroso, (así como aleatorio) siendo las obligaciones que derivan de él de carácter personal y no real ]en el mismo sentido STS 8 mayo 1992]: para el pagador "tiene la esencial de pagar la renta durante la vida que se determine, que la normal es la del propio rentista" (...), y para el rentista "tiene la esencial de la entrega y transmisión dominical de un capital en bienes muebles o inmuebles, como dice literalmente dicho artículo 1802 pero que se interpreta en un sentido amplio que comprende no sólo la transmisión del derecho de propiedad de cosa mueble o inmueble, sino también la de cualquier otro derecho real que no sea el de propiedad o incluso un derecho personal; entenderlo así se corresponde a una interpretación progresiva del articulado de un más que centenario código, adaptándolo a la siempre cambiante realidad social (artículo 3.1 CC) y entenderlo de otra forma sería admitir el contrato como utópico, en base al principio de autonomía de la voluntad (artículo 1255 CC) y aplicar por analogía las mismas normas del contrato de renta vitalicia.

La STS 2.3.1956 establece que "la transmisión del dominio es requisito indispensable para que exista el contrato de renta vitalicia".

"Los artículos 1802 y siguientes al regular el denominado contrato de renta vitalicia desligan las titularidades transmitidas de las vicisitudes de las obligaciones asumidas por el adquirente hasta el extremo de excluir la recuperación del predio enajenado en caso de impago de las pensiones". RDGRN de 26.4.1991, recogiendo también la jurisprudencia sobre la materia.

Las partes son libres para fijar el objeto de la pensión, pero ha de ser fija y determinada y puede ser objeto de cláusulas de revisión o revalorización, o incluso de aplicación de la cláusula rebus sic stantibus [Ss. TS. 16.12.1930; 31.10.1960; 23.11. 1962].

El artículo 1805 del Código Civil prohíbe el reembolso del capital y volver a entrar en la posesión del predio enajenado al pensionista en el caso de que el deudor no cumpla con las pensiones vencidas, sólo teniendo derecho a reclamar judicialmente el pago de las rentas atrasadas y el aseguramiento de las futuras. No obstante este artículo ha sido interpretado por la jurisprudencia dando prioridad al principio de autonomía de la voluntad entre las partes contratantes recogido en el artículo 1255 del CC, de tal forma que puede pactarse que el incumplimiento de un número determinado de pensiones dará lugar a la resolución del contrato y la consiguiente recuperación por el enajenante (pensionista) de las fincas vendidas. Por tanto el artículo 1805 admite pacto en contrario y la previsión de cláusula resolutoria expresa para el caso de impago de la pensión [STS 13.5.1959; 14.10.1960, 15.1.1963].

Es más se concibe al artículo 1805 no como una prohibición de pacto resolutorio, sino una prohibición legal de carácter dispositivo para el caso de silencio contractual al respecto. RR. DGRN de 16.10.1989 y 26.4.1991], recogiendo jurisprudencia sobre la materia. Por tanto cabe pactar la resolución del contrato de renta vitalicia en caso de incumplimiento en el pago de las pensiones, revertiendo el bien transmitido al pensionista-transmitente, o dicho de otra manera cabe llevar a cabo pacto comisorio.


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
