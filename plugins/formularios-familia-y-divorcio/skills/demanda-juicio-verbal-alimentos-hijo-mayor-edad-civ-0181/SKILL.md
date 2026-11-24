---
name: demanda-juicio-verbal-alimentos-hijo-mayor-edad-civ-0181
description: "Demanda de juicio verbal de alimentos del hijo mayor de edad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de alimentos del hijo mayor de edad

> Formulario **CIV-0181** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Procurador, representación y asistencia Letrada Interposición de demanda de Juicio Verbal HECHOS: Justificación Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial FUNDAMENTOS DE DERECHO Solicito Otrosí Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de alimentos del hijo mayor de edad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de alimentos del hijo mayor de edad” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-verbal-alimentos-hijo-mayor-edad-civ-0181`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] CALLE (2 veces)
- [ ] NOMBRE DEL CENTRO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] ESTUDIOS
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NACIONALIDAD
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE DOCUMENTO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 50 LEC
- art. 85.1 LOPJ
- art. 250.1.8 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 253 LEC
- art. 251.7 LEC

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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello (o bien: “según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº ”), comparezco en este Tribunal con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo demanda de JUICIO VERBAL contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., en reclamación de alimentos. La presente demanda se basa en los siguientes

HECHOS:

PRIMERO.- Que mi representado, de [Nº] años de edad y soltero, se encuentra todavía en proceso de formación, cursando estudios de [ESTUDIOS] en [NOMBRE DEL CENTRO], sin que haya accedido todavía al mercado laboral.

SEGUNDO.- Que mi representado no dispone de medios propios para subsistir, pues carece de patrimonio y no obtiene ningún tipo de ingresos.

TERCERO.- Que los parientes más próximos de mi representado son sus padres, D. [NOMBRE Y APELLIDOS] y Dª [NOMBRE Y APELLIDOS] encontrándose su padre/madre, de nacionalidad [NACIONALIDAD], y con domicilio oficial en su país de origen, en paradero desconocido desde hace años, por lo que resulta inviable la reclamación de alimentos contra el/la mismo/a; y su abuelo/a paterna/materna, D./Dª [NOMBRE Y APELLIDOS], que padece una discapacidad reconocida administrativamente del [Nº] por ciento. En la actualidad vive con dicho/a abuelo/a, en cuyos cuidados colabora de modo importante.

CUARTO.- Que D./Dª [NOMBRE Y APELLIDOS] se encuentra en una holgada situación económica, gracias a los elevados ingresos que obtiene como [PROFESIÓN] Además dispone de varios inmuebles de su propiedad.

QUINTO.- En consecuencia, se reclama al/a la padre/madre de mi representado, una pensión de alimentos de [IMPORTE] euros mensuales, a satisfacer, con carácter anticipado, en los cinco primeros días de cada mes, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], de la que es titular mi representado, actualizable anualmente de acuerdo con las variaciones experimentadas por el IPC que señale el Instituto Nacional de Estadística u organismo que lo sustituya.

Como justificación de los anteriores hechos, se acompañan los siguientes DOCUMENTOS:

1) Certificado de nacimiento de mi representado, donde consta su filiación paterna y materna, así como su fecha de nacimiento.

2) Justificante de matrícula en [NOMBRE DEL CENTRO] de mi representado, junto con el certificado de las calificaciones obtenidas en el primer curso expedido por [ÓRGANO O PERSONA]

3) Certificado de empadronamiento de mi representado en el domicilio de su abuelo/a, antes citado/a.

4) Copia del certificado de discapacidad del abuelo/a de mi representado.

5) Certificaciones expedidas por los Registros de la Propiedad de [LOCALIDAD] y [LOCALIDAD] (oficinas núms. y [Nº], respectivamente) en las que consta la propiedad del/la demandado/a sobre dos pisos ubicados en las citadas localidades.

Resultan aplicables a los citados hechos los siguientes

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN

Es competente la jurisdicción civil, de acuerdo con lo establecido en el art. 22 ter/quáter de la Ley Orgánica del Poder Judicial.

II. Competencia

Son competentes los Tribunales de [LOCALIDAD], lugar en que tiene su domicilio la demandada, de acuerdo con el artículo 50 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

III. Procedimiento

La presente demanda debe sustanciarse por los trámites del juicio verbal, en virtud de lo dispuesto en el artículo 250.1.8º LEC.

IV. Capacidad

Ambas partes tienen capacidad para serlo, conforme a lo dispuesto en los artículos 6 y ss. LEC.

V. Legitimación

Están legitimados activa y pasivamente, el/la demandante y el/la demandada. El primero, como acreedor de alimentos debidos y, el segundo, como obligado a prestarlos, de acuerdo con los arts. 142 y ss. CC.

VI. Representación y defensa

El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 LEC.

VII. Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII. Derecho sustantivo

Los arts. 142 y ss del Código civil, que regulan la obligación legal de alimentos; en especial los arts. 143.I.2º, 144.I.3º y 145.II del Código civil.

IX. Costas

Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en el art. 394 LEC.

Por lo expuesto

SOLICITO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta demanda, que habrá de sustanciarse por los trámites del juicio verbal, en nombre de D./Dª [NOMBRE Y APELLIDOS], en ejercicio de la acción de reclamación de alimentos, contra D./Dª [NOMBRE Y APELLIDOS]; y, previos los trámites legales que procedan, dicte sentencia en la que, estimando íntegramente la demanda, condene a la demandada a prestar los alimentos a mi representado en cuantía estimada de [IMPORTE] euros mensuales, salvo fijación de otra por el juzgador, para atender las necesidades de sustento, habitación, vestido, asistencia médica y educación. Y se condene al/a la demandado/a al pago de las costas del presente procedimiento.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 LEC en [IMPORTE] euros.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
