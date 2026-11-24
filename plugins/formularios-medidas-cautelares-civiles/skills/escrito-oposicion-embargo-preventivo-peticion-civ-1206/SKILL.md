---
name: escrito-oposicion-embargo-preventivo-peticion-civ-1206
description: "Escrito de oposición al embargo preventivo con petición subsidiaria de caución sustitutoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición al embargo preventivo con petición subsidiaria de caución sustitutoria

> Formulario **CIV-1206** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del demandado a la medida cautelar de embargo preventivo de bienes acordada sin audiencia previa para asegurar la reclamación de comisiones impagadas e indemnización por clientela derivadas de un contrato de agencia, con petición subsidiaria de que se sustituya el embargo por una caución sustitutoria.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición al embargo preventivo con petición subsidiaria de caución sustitutoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición al embargo preventivo con petición subsidiaria de caución sustitutoria” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:escrito-oposicion-embargo-preventivo-peticion-civ-1206`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL DEL DEMANDADO (6 veces)
- [ ] Nº (5 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL DEL ACREEDOR
- [ ] DENOMINACIÓN SOCIAL DEL TERCERO PROVEEDOR
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL

## Normas que cita el formulario

- art. 723.1 LEC
- art. 739 LEC
- art. 746 LEC
- art. 741.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, en nombre y representación de [DENOMINACIÓN SOCIAL DEL DEMANDADO], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº]; asistida del Letrado/a suscrito D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], colegiado con n.º [Nº DE COLEGIADO] en el Ilustre Colegio de Abogados de [COLEGIO], y cuyo despacho profesional se abre en [DOMICILIO PROFESIONAL]; en autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO], seguidos a instancias de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que por medio del presente escrito, y en la representación que ostento, deduzco escrito de oposición en la pieza separada de medidas cautelares de los presentes autos, dentro de los veinte días hábiles siguientes a la notificación del auto que acordó el embargo preventivo de bienes de mi representada, con base en los siguientes

HECHOS

PRIMERO

Con expresa remisión a la contestación que se formula en los autos principales, resumimos que mi mandante sostiene que lo que el demandante D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] dice que se le adeuda por comisiones son diferencias entre lo que pretende que habría de haber cobrado y lo que efectivamente cobró.

Y es que el contrato con el actor no excluía las oscilaciones del importe porcentual de comisiones, conforme a la evolución del mercado, que la rebaja en fecha [FECHA] por [DENOMINACIÓN SOCIAL DEL DEMANDADO] (se acompaña documento n.º [Nº]).

SEGUNDO

Si bien la rebaja de comisiones fue protestada en misiva de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], sin embargo, siguió el actor prestando sus servicios con normalidad bajo el nuevo régimen remuneratorio, de tal manera que, al no existir incumplimiento justificador de la resolución, es un puro desistimiento que no da lugar a indemnización ninguna de esta parte y, además, al no respetar el plazo de preaviso, haría deudor al agente.

TERCERO

Se niega expresamente la informalidad del suministro al agente por esta parte, y se niega la veracidad de las informaciones de prensa que se adjuntan con la demanda.

CUARTO

Mi mandante no tenía más relación con [DENOMINACIÓN SOCIAL DEL TERCERO PROVEEDOR] que la mercantil contractual derivada de, entre otros clientes, distribuir en exclusiva sus productos, y es perfectamente ajena a la crisis económica de tal sociedad y sus conflictos. Al perder sus productos y su marca, lógicamente [DENOMINACIÓN SOCIAL DEL DEMANDADO] ya no podrá distribuirlos.

QUINTO

[DENOMINACIÓN SOCIAL DEL DEMANDADO], que atraviesa problemas serios de liquidez, ha alcanzado con la entidad [DENOMINACIÓN SOCIAL DEL ACREEDOR], su acreedora en autos de ejecución n.º [Nº DE PROCEDIMIENTO] del Tribunal de Instancia de [SEDE], un acuerdo transaccional que compromete el alzamiento del embargo sobre los bienes embargados ahora preventivamente (documento n.º [Nº]).

SEXTO

La medida que ha adoptado el Tribunal a instancias de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] supone un grave perjuicio para mi mandante, puesto que necesita imperiosamente financiación, lo que implica la utilización en garantía de su pequeño patrimonio. Es por ello que se solicitará subsidiariamente la fijación de contracautela, que se está consiguiendo en una entidad bancaria, a cambio de que se pueda hipotecar el local propiedad de [DENOMINACIÓN SOCIAL DEL DEMANDADO], libre del embargo.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Conformes con la territorial, según la funcional ex art. 723.1 LEC, puesto que hay sumisión tácita para el proceso principal.

II.- PROCEDIMIENTO

La oposición a la medida cautelar decretada sin previa audiencia del sujeto pasivo se puede formular en tiempo y forma conforme a los arts. 739 a 742 LEC.

III.- FONDO DE LA OPOSICIÓN

Siendo la causa de pedir cuantos hechos y razones se opongan a la procedencia, requisitos, alcance, tipo y demás circunstancias de la medida efectivamente acordada, sin limitación alguna —así como la oferta de caución sustitutoria—, se discierne:

Presupuestos: Aunque puede asumirse, en teoría, que, de ostentar un derecho subjetivo patrimonial contra mi mandante el actor, existe por el retraso en resolverse un peligro, por la situación de insuficiencia financiera que padece, no lo es por maniobras fraudulentas que no se pueden demostrar, ya que solo son elucubraciones interesadas. En todo caso, no hay en absoluto ese «fumus boni iuris» o apariencia de buen derecho, puesto que los documentos aportados por el actor a lo sumo abonan una discrepancia en cuanto al cómputo de comisiones, por la rebaja que el demandado no acepta, de lo que se sigue que no hay motivo para resolver por incumplimiento ni derecho indemnizatorio. Además, la indemnización es una cifra que el interesado autoliquida.

Caución sustitutoria: Subsidiariamente, se solicita, con arreglo a los arts. 746 y 747 LEC, la determinación de caución sustitutoria, que tiene el mismo fundamento cautelar que el embargo preventivo y debe ponderar la proporcionalidad entre el valor de aseguramiento para el solicitante de garantía y la restricción que supone el embargo a la actividad patrimonial del demandado o gravamen.

Se solicita la caución sustitutoria en cifra exclusivamente de la cuantía de comisiones reclamadas de [IMPORTE] euros, sin tomar en cuenta unas cifras ilíquidas y, en todo caso, mediante aval bancario y plazo de otorgamiento generoso.

Caución: Subsidiariamente, en último lugar, la cantidad por la que se embarga se estima excesiva, y la caución fijada se estima insuficiente. Lo primero, porque se suma toda la reclamación, líquida e ilíquida. Lo segundo, porque es muy inferior a la reclamación que se hace; supuesto de admitirse, la apariencia de buen derecho no es vigorosa; y, en fin, el perjuicio para mi mandante es tan grave que le priva de toda financiación con garantía real, sin poseer otra.

IV.- COSTAS

Con arreglo al art. 741.2 LEC, si se alzare el embargo preventivo, habrá que condenar en costas del incidente al que lo promovió.

En su virtud,

SUPLICO AL TRIBUNAL, que, teniendo por presentado este escrito con los documentos que se acompañan, se digne admitir una y otros y tenga a esta parte por opuesta al embargo preventivo decretado, mandando que la oposición se sustancie en vista, después de la que recaiga auto que proceda a alzar la medida cautelar decretada, y condene a la parte demandante a indemnizar los daños y perjuicios ocasionados, así como las costas procesales del incidente; o, subsidiariamente, se reduzca la cantidad que garantizará a la de [IMPORTE] euros y se resuelva acceder a que, en sustitución de dicho embargo preventivo reducido, se preste caución sustitutoria por [DENOMINACIÓN SOCIAL DEL DEMANDADO], en cantidad de los predichos [IMPORTE] euros, en forma de aval bancario.

Es de justicia que pido en [LOCALIDAD], a [FECHA].

OTROSÍ DIGO que, siendo el poder general para pleitos y necesitándolo para otros usos,

SUPLICO AL TRIBUNAL que, una vez tomada nota en autos, sea desglosado y devuelto a esta parte.

Reitero justicia en lugar y fecha ut supra.

Por ser de justicia que pido en [LOCALIDAD], a [FECHA].

Firma del Abogado/a: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS DEL PROCURADOR]

NOTAS DE USO

El contrato de agencia se rige por la Ley 12/1992, de 27 de mayo, sobre Contrato de Agencia. Los hechos de este modelo (rebaja de comisiones, desistimiento del agente, crisis del proveedor y acuerdo transaccional con otro acreedor) corresponden a un supuesto concreto y deben sustituirse por los del caso.
