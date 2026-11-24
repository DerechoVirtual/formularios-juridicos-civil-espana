---
name: solicitud-division-judicial-herencia-liquidacion-civ-0401
description: "Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales

> Formulario **CIV-0401** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:solicitud-division-judicial-herencia-liquidacion-civ-0401`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] MES (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] DERECHO CIVIL APLICABLE
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] SEDE
- [ ] SUCURSAL
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 808 LEC
- art. 53.1 LEC
- art. 73.3 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Dª [NOMBRE Y APELLIDOS], y de D. [NOMBRE Y APELLIDOS], según acredito mediante designación apud acta otorgada ante el Letrado de la Administración de Justicia de la Oficina de [SUCURSAL] que acompaño (o, en su caso, copia auténtica de la copia electrónica del poder notarial de representación informática (o digitalizada) que debidamente bastanteada acompaño, solicitando su devolución por precisarla para otros usos una vez testimoniada en autos), y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que en la indicada representación y mediante el presente escrito, siguiendo instrucciones de mis mandantes, formulo DEMANDA ACUMULANDOS LAS ACCIONES DE DIVISIÓN JUDICIAL DE HERENCIA de D. [NOMBRE Y APELLIDOS], respectivamente esposo y padre de mis representados, CON LA DE PETICIÓN DE LIQUIDACIÓN DE LA SOCIEDAD DE GANANCIALES constituida entre mi representada y citado causante, acción que dirijo contra D. [NOMBRE Y APELLIDOS], hijo del causante y mi representada, con domicilio en [LOCALIDAD], basando esta demanda en los siguientes

HECHOS

Que el causante, esposo y padre de mis mandantes, D. [NOMBRE Y APELLIDOS], con vecindad civil [VECINDAD CIVIL] por haber nacido y residido toda su vida en [LOCALIDAD], territorio de Derecho Civil [DERECHO CIVIL APLICABLE], falleció el pasado día [FECHA] del mes [MES] del año en curso, a la edad de [Nº] años en su domicilio sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], según acredito mediante certificación literal de defunción del Registro Civil de la localidad de [LOCALIDAD] que acompaño como documento núm. uno.

Que D. contrajo matrimonio en [LOCALIDAD] con mi representada Doña [NOMBRE Y APELLIDOS], el día [FECHA] del mes de [MES] del año [AÑO], según acredito mediante certificación literal de matrimonio del Registro Civil de la localidad de [LOCALIDAD] que acompaño como documento núm. dos. El régimen económico matrimonial era el de sociedad de gananciales, quedando disuelto por el fallecimiento del causante.

Fruto del citado matrimonio nacieron dos hijos: Don [NOMBRE Y APELLIDOS], actual demandante, y Don [NOMBRE Y APELLIDOS], contra quien se dirige esta demanda, cuyos datos y señas obran en el encabezamiento, En prueba de lo manifestado acompaño las correspondientes certificaciones literales de nacimiento acreditativas de la filiación, como documentos números tres, cuatro, cinco y seis, respectivamente.

Como se ha indicado, el causante falleció el día [FECHA], habiendo otorgado testamento en fecha [FECHA], legando a su esposa la parte de libre disposición además de la cuota legal usufructuaria, e instituyendo herederos a sus hijos en sus demás bienes, tal como se acredita por copia auténtica del testamento y certificación del Registro de Actos de Última Voluntad (o, en su caso, el causante falleció sin otorgar testamento, por lo que se iniciaron los trámites para la declaración de herederos ab intestato, siendo declarados como tales los hijos del causante y su cónyuge, tal como se acredita por acta notarial que se acompaña como documento número [Nº DE DOCUMENTO])

Con la finalidad de liquidar la sociedad de gananciales disuelta por el fallecimiento del causante y de dividir la herencia, mis representados convocaron al demandado a la notaría de D. [NOMBRE Y APELLIDOS] en fecha [FECHA], quien no compareció, ni ha contestado a los intentos de llegar a una solución amistosa, expresando tan solo su disconformidad bajo la alegación de deber traerse a la herencia "las cuantiosas donaciones que se han producido a favor de mi hermano" según consta en la carta remitida por conducto notarial en fecha

Ante la imposibilidad de llegar a un acuerdo con el demandado, mis representados se ven en la obligación de ejercitar la presente acción a fin de disolver la sociedad de gananciales y adjudicar la herencia.

En cuanto a la liquidación de la sociedad de gananciales, y de conformidad con lo dispuesto el artículo 808 y siguientes de la LEC, insto la liquidación del régimen económico de gananciales del matrimonio constituido por el causante y mi representada, acompañando al presente escrito propuesta de inventario del régimen de gananciales por el que se rige el citado matrimonio y documentos justificativos de sus diferentes partidas (documentos número [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO]).

Las partidas que se recogen en el inventario determinan un caudal líquido de [IMPORTE] euros, solicitándose la adjudicación de la mitad del haber ganancial a mi representada Dª [NOMBRE Y APELLIDOS] y la otra mitad a la herencia yacente del cónyuge fallecido D. [NOMBRE Y APELLIDOS], conforme a la propuesta de liquidación que también se acompaña como documento número

Practicada la liquidación del régimen económico matrimonial, y una vez incluido en el caudal hereditario la parte correspondiente a la mitad del haber ganancial, dicho caudal hereditario está conformado por los bienes muebles, inmuebles, participaciones, títulos valores, créditos y activos que a continuación se exponen:

Asimismo se tiene constancia de la existencia de determinadas deudas que asolan el patrimonio relicto, nacidas de los créditos de terceros que a continuación se exponen:

Por todo ello, pretendemos que se proceda a la liquidación del régimen de gananciales, con adjudicación de la mitad a mi representada Dª [NOMBRE Y APELLIDOS], y la otra mitad pro indiviso a la herencia del causante D. [NOMBRE Y APELLIDOS]; así como que se practique la división de la herencia proponiendo como inventario el reseñado en este escrito de demanda, y fijado el inventario se convoque a junta de herederos, se nombre contador y peritos tasadores y se lleven a efecto las operaciones divisorias

A los anteriores hechos, se estiman de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Legitimación activa

Se encuentran legitimados mis mandantes para el ejercicio de las acciones acumuladas de liquidación de la sociedad de gananciales y solicitud de división judicial del caudal hereditario del finado, en cuanto cónyuge y heredero del causante, de conformidad con lo prevenido en los artículos 782 y 806 y siguientes de la vigente Ley de Enjuiciamiento Civil.

Jurisdicción

En cuanto a la jurisdicción es de aplicación lo dispuesto en el artículo 117 de la Constitución Española, artículo 21 de la Ley Orgánica del Poder Judicial de 1 de julio de 1.985 y artículos 5 y 36 de la Ley de Enjuiciamiento Civil.

Competencia objetiva

En cuanto a la competencia objetiva es de aplicación lo dispuesto en el artículo 85 de la Ley Orgánica del Poder Judicial y artículo 45 de la Ley de Enjuiciamiento Civil, correspondiendo la competencia objetiva para la sustanciación del proceso introducido por la presente demanda, en primera instancia, a los órganos jurisdiccionales de esta clase o grado.

Competencia territorial

En cuanto a la competencia territorial es de aplicaciónel art. 53.1 LEC que, en su inciso primero, en cuya virtud será tribunal competente territorialmente, cuando se ejerciten varias acciones frente a una o varias personas, el del lugar correspondiente al de la acción que sea fundamento de las demás, siendo de aplicación lo dispuesto en el artículo 52.4 de la Ley de Enjuiciamiento Civil por cuanto que la liquidación de los gananciales trae causa de la disolución por fallecimiento (ATS 16 noviembre 2010, rec. 514/2010, en el que se determina el fuero que decanta la competencia territorial en juicios sobre cuestiones hereditarias a favor prioritariamente del órgano judicial de la demarcación en que el finado tuvo su último domicilio y, si fueren varios los que en el territorio ostentaren jurisdicción, a favor de aquel al que por reparto se turne el asunto.

Acciones que se ejercitan. Se ejercitan de forma acumulada la acción de liquidación del régimen de gananciales y la de división judicial de la herencia, al amparo de lo dispuesto en el artículo 73.3 LEC.

En cuanto a la necesidad de llevar a cabo la previa liquidación de la comunidad de gananciales (STS 15 de junio de 2006, rec. 4167/1999).

En cuanto a la procedencia de la acumulación de acciones, es mayoritaria la postura de las Audiencias Provinciales, pudiendo citarse entre otras: AAP Madrid (Sección 14) 20 octubre 2009, rec. 525/2009; SAP Guipúzcoa (Sección 1) 11 mayo 2009, rec. 2120/2009; SAP Almería (Sección 1), sentencia núm. 153/2008, de 10 septiembre; AAP Huelva (Sección 2) 20 febrero 2008, rec. 26/2008; Madrid, Sección 11ª, 26 septiembre. 2008, rec. 169/2008; AAP Madrid, Sección 21ª, 29 noviembre 2011, rec. 490/2011 con cita de los AAP Audiencias Provinciales de Castellón -Sección 1ª- de 29 de abril de 2005, rec. 29/2005, Cádiz -Sección 5ª- de 26 de noviembre de 2007, rec. 564/2007, Madrid, Sección 14ª, de 26 de enero de 2011, rec. 718/2010, y Granada -Sección 3ª -de 24 de septiembre de 2010, y de las SSAP Burgos -Sección 3ª- de 15 de julio de 2005, rec. 235/2005 y Alicante -Sección 6ª- de 9 de mayo de 2007.

Procedimiento

El procedimiento a través del que debe tramitarse la pretensión incorporada a la presente demanda es el prevenido en los artículos 782 a 788 de la Ley de Enjuiciamiento Civil, sin perjuicio de la prevención establecida en el artículo 789 del citado cuerpo legal. De acuerdo a la interpretación realizada en resulta procedente la tramitación acumulada de la liquidación de la sociedad conyugal y la división de la herencia que nos ocupa, al tratarse de trámites comunes, según la jurisprudencia arriba citada.

Fundamentos de Derecho material

Artículos 1344 y siguientes del Código Civil y artículos 1.965, 1.051, 1.052 del Código civil.

En su virtud,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; me tenga por comparecido y parte en la representación que ostento y tengo acreditada en la forma dicha de don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS], ordenando se entiendan conmigo las actuaciones judiciales y demás notificaciones que recaigan, y teniendo por ejercitadas de forma acumulada las acciones de disolución y liquidación del régimen económico-matrimonial y división de herencia del causante D. [NOMBRE Y APELLIDOS], y, tras los trámites legales, se declare la extinción del régimen de gananciales existente, con adjudicación de la mitad a mi representada Dª [NOMBRE Y APELLIDOS], y la otra mitad pro indiviso a la herencia del causante D. [NOMBRE Y APELLIDOS]; así como que se proceda a la división de la herencia proponiendo como inventario el reseñado en este escrito de demanda, y fijado el inventario se convoque a junta de herederos, se nombre contador y peritos tasadores y se lleven a efecto las operaciones divisorias

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmas de Abogado y Procurador
