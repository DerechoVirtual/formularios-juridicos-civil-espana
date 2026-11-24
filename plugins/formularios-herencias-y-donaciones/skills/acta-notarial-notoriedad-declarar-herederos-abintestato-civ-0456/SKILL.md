---
name: acta-notarial-notoriedad-declarar-herederos-abintestato-civ-0456
description: "Acta notarial de notoriedad para declarar herederos abintestato. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta notarial de notoriedad para declarar herederos abintestato

> Formulario **CIV-0456** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta notarial de notoriedad para declarar herederos abintestato» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta notarial de notoriedad para declarar herederos abintestato” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:acta-notarial-notoriedad-declarar-herederos-abintestato-civ-0456`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] Nº (5 veces)
- [ ] AÑO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MES (4 veces)
- [ ] DÍA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] SERIE (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] FECHA
- [ ] NIF/DNI
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 930 Código Civil
- art. 6 Ley Orgánica 3/2018

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

- Junto a «… garantía de los derechos digitales (LOPDGDD), y Reglamento (UE) 2016/679 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

ACTA DE NOTORIEDAD DE DECLARACIÓN DE HEREDEROS ABINTESTATO.

NÚMERO (protocolo).

Se inicia esta acta, en [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, Notario del Ilustre Colegio de [COLEGIO].

INTERVIENE

En su propio nombre y derecho, me aseguro de su identidad por su D.N.I, la juzgo con capacidad e interés legítimo suficiente para esta ACTA.

EXPOSICIÓN

Requerimiento

El Sr./Sra. me requiere para declaración notarial de herederos ab intestato, según los siguientes hechos, que manifiesta:

Don [NOMBRE Y APELLIDOS], falleció en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], con vecindad civil [VECINDAD CIVIL] sin haber otorgado disposición de última voluntad alguna.

El/la causante mencionado en el apartado anterior falleció en estado de casado/a y de su único matrimonio contraído con Doña/Don [NOMBRE Y APELLIDOS], tuvo y le sobreviven los siguientes descendientes: sus hijos Don [NOMBRE Y APELLIDOS], Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS]

Me asevera bajo pena de falsedad en documento público la certeza de los hechos expuestos, propone como pruebas para su demostración la documental y la testifical a practicar por mí, sin perjuicio de otras que yo estimare necesarias o convenientes; y me requiere para que compruebe y declare la notoriedad de los hechos narrados y, por tanto, herederos abintestato del causante a sus indicados descendientes.

Prueba

Como prueba documental me exhibe el Libro de Familia de los cónyuges Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], y certificados literales de matrimonio de el/la causante y su citada/o cónyuge, también literales de nacimiento de sus hijos Don [NOMBRE Y APELLIDOS], Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], y del Registro General de Actos de Última Voluntad, certificados que devuelvo.

Testimonio por fotocopia de las páginas del Libro de Familia, que concuerda con su original, incorporo a esta matriz para que forme parte de ella a todos los efectos, así como de los certificados literales del registro Civil citados.

Certificaciones literales de defunción y del Registro General de Actos de Ultima Voluntad que acreditan su aserto y Documento Nacional de Identidad del causante (o certificado de empadronamiento u otro documento que acredite el último domicilio del causante) me entrega la persona requirente y yo, el Notario, dejo unidos a esta matriz a todos los efectos mediante testimonio por fotocopia que concuerda con su original.

PRUEBA TESTIFICAL. DILIGENCIA: Siendo las [Nº] horas del día [DÍA] de [MES] de [AÑO], comparecen ante mí Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con D.N.I. número [NÚMERO]; y Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecina de [LOCALIDAD], domiciliado/a en [DOMICILIO], con D.N.I. número [NIF/DNI]

En calidad de testigos en su propio nombre y derecho. Les identifico por sus documentos nacionales de identidad y, en relación con esta acta, previamente advertidos por mí el Notario de que pueden incurrir en la pena de falsedad en documento público si desvirtúan la verdad, libre y espontáneamente aseveran que de ciencia propia les consta la certeza y veracidad de los hechos cuya declaración de notoriedad se pretende en virtud de esta acta.

Sin nada más que hacer constar doy por concluida esta diligencia que por su acuerdo y renuncia leo a los comparecientes la encuentran conforme y firman conmigo el Notario, que doy fe de su contenido extendido en

Juicio de notoriedad y declaración de herederos

Yo, el Notario, en base a las pruebas practicadas, declaro: justificada la notoriedad pretendida de los hechos narrados y, en consecuencia, conforme a los artículos 209 y 210 del Reglamento Notarial, al resultar evidente por aplicación directa de los artículos 930, 932, 943 y 944 del Código Civilformalmente HEREDEROS de Don a sus hijos Don [NOMBRE Y APELLIDOS], Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], sin perjuicio de la cuota legal usufructuaria que conforme al artículo 834 del mismo cuerpo legal corresponde al cónyuge viudo Doña [NOMBRE Y APELLIDOS]

Y sin nada más que hacer constar, doy por concluida esta acta de notoriedad, tramitada conforme a las vigentes disposiciones procesales y notariales extendida en [Nº] folios de serie [SERIE], números [Nº] el día [FECHA] de [MES] de 20 [AÑO] bajo el número [NÚMERO] de mi Protocolo Ordinario de Instrumentos Públicos.

Aprobación y autorización

Así lo dicen y otorgan, después de hechas las reservas y advertencias legales pertinentes.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD), y Reglamento (UE) 2016/679 (RGPD) (B.O.E. de 14 de diciembre de 1999), los comparecientes prestan su expreso consentimiento para que sus datos de carácter personal queden incorporados a los ficheros automatizados de esta Notaría, conservándose en la misma con carácter confidencial y reservado y sin perjuicio de las remisiones autorizadas por la Ley.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura, es responsable del fichero, de su seguridad y confidencialidad el Notario titular de esta notaría.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

Permito al compareciente la lectura de esta escritura, porque así lo solicita después de advertida de la opción del artículo 193 del Reglamento Notarial.

Enterada, según dice, por la lectura que ha practicado y por mis explicaciones verbales, la señora compareciente hace constar libremente su consentimiento al contenido de la escritura. Y la firma.

Y yo el Notario, del contenido de este instrumento público, extendido [Nº] folios de papel timbrado de la clase [CLASE], serie [SERIE], números [Nº]

Firmas

========================================================================
