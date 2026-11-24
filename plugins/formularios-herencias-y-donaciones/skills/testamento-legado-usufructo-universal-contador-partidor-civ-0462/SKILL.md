---
name: testamento-legado-usufructo-universal-contador-partidor-civ-0462
description: "Testamento con legado, usufructo universal y contador partidor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Testamento con legado, usufructo universal y contador partidor

> Formulario **CIV-0462** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Modelo de testamento notarial abierto de una persona casada con hijos, que lega el usufructo universal al cónyuge (cautela socini), instituye herederos a los hijos con sustitución, y admite bloques alternativos de legado ordinario, de cosa ganancial o de parte alícuota, limitación de responsabilidad por legados, nombramiento de tutor o curador y de contador-partidor.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Testamento con legado, usufructo universal y contador partidor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Testamento con legado, usufructo universal y contador partidor” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:testamento-legado-usufructo-universal-contador-partidor-civ-0462`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] RELACIÓN DE PARENTESCO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IDENTIFICACIÓN DEL OBJETO DEL LEGADO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HEREDERO GRAVADO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CIF
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN DE LA FUNDACIÓN
- [ ] DNI/NIE
- [ ] DÍA
- [ ] EL/LA
- [ ] ESTADO CIVIL
- [ ] HORA
- [ ] MES
- [ ] MINUTOS
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL TESTADOR
- [ ] NOMBRES Y APELLIDOS
- [ ] NÚMEROS
- [ ] PARTE
- [ ] PORCENTAJE
- [ ] PROFESIÓN
- [ ] SERIE

## Normas que cita el formulario

- art. 236.4 Código Civil
- art. 238 Código Civil

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

- Junto a «…ión [DENOMINACIÓN DE LA FUNDACIÓN], con C.I.F. [CIF] y domicilio en [DOMICILIO].»: la sustitución ejemplar fue modificada por la Ley 8/2021, de 2 de junio, de apoyo a las personas con discapacidad; comprobar la redacción vigente del artículo 776 del Código Civil y su encaje con los apoyos que precise el hijo antes de utilizar esta cláusula.
- Junto a «…bra como tales, por orden de prelación, a los siguientes: [NOMBRES Y APELLIDOS].»: tras la Ley 8/2021, la tutela queda reservada a los menores no sujetos a patria potestad y las medidas de apoyo a personas con discapacidad (curatela, guarda de hecho, defensor judicial) se rigen por los artículos 249 y siguientes del Código Civil; comprobar el artículo equivalente a los citados 236.4 y 238 antes de utilizar esta cláusula.

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

TESTAMENTO CON LEGADO

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECE D./Dª [NOMBRE Y APELLIDOS DEL TESTADOR], mayor de edad, [ESTADO CIVIL], [PROFESIÓN], vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO] y D.N.I. número [DNI/NIE], y

DICE

Que es hijo/a de los consortes D./Dª [NOMBRE Y APELLIDOS], fallecido/a, y D./Dª [NOMBRE Y APELLIDOS], que vive; estando [ELEGIR: casado / casada] en únicas nupcias con D.ª/D. [NOMBRE Y APELLIDOS DEL CÓNYUGE], de cuyo matrimonio tiene [NÚMERO] hijos, llamados [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS].

Que ordena su última voluntad a tenor de las siguientes

ESTIPULACIONES

Usufructo universal

Lega a su cónyuge el usufructo universal y vitalicio de su herencia, relevándole de la obligación de prestar fianza y hacer inventario. Si alguno de sus descendientes legitimarios no estuviese conforme con esta disposición, quedará reducido a su legítima estricta, acreciendo su parte en los tercios de mejora y libre disposición a los que lo estuvieren; y si ninguno fuese conforme, lega a su cónyuge el tercio de libre disposición en pleno dominio, además de su cuota legal usufructuaria.

Ordena a sus herederos respetar esta disposición testamentaria y determina que aquel que la impugnare reciba en tal caso, del testador, sólo lo que por legítima estricta le conceda la Ley, acreciendo lo que perdiera en los tercios de mejora y libre disposición en favor de los que acaten su voluntad expresada.

Institución de herederos

Instituye por sus únicos universales herederos por partes iguales a sus antes mencionados hijos, y a los demás hijos que puedan tener en el futuro, con sustitución vulgar, en caso de premoriencia o incapacidad de los mismos, en favor de sus respectivos descendientes.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sustitución vulgar.

Sustituye vulgarmente a sus hijos, D. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS], para los casos de premoriencia o incapacidad de los mismos, por sus respectivos descendientes.

— Sustitución ejemplar.

Sustituye ejemplarmente a sus hijos, D. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS], quedando sujeta la sustitución ejemplar a la condición de que los sustitutos D. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS] atiendan al sustento, habitación, vestido y asistencia médica del sustituido, su hermano [NOMBRE Y APELLIDOS], durante toda la vida de éste.

En caso de no cumplirse tal condición, sustituye ejemplarmente a su hijo D. [NOMBRE Y APELLIDOS] por la Fundación [DENOMINACIÓN DE LA FUNDACIÓN], con C.I.F. [CIF] y domicilio en [DOMICILIO].

Preterición

Manifiesta que quiere que este testamento valga íntegramente aun en caso de preterición, aunque sea errónea y total, sin perjuicio de la legítima más reducida y estricta que le corresponda al preterido o preteridos.

Legado

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Legado ordinario.

Que lega a su [RELACIÓN DE PARENTESCO], D. [NOMBRE Y APELLIDOS], [IDENTIFICACIÓN DEL OBJETO DEL LEGADO], con cargo a la porción hereditaria de [NOMBRE Y APELLIDOS DEL HEREDERO GRAVADO].

— Legado de cosa ganancial.

Que lega a su [RELACIÓN DE PARENTESCO], D. [NOMBRE Y APELLIDOS], [IDENTIFICACIÓN DEL OBJETO DEL LEGADO], con cargo a la porción hereditaria de [NOMBRE Y APELLIDOS DEL HEREDERO GRAVADO]. Hace este legado con conocimiento de que la finca tiene carácter ganancial y con la voluntad de que, entre las herencias del testador y de su cónyuge, el legatario perciba la totalidad de la finca.

— Legado de parte alícuota.

Que lega a su [RELACIÓN DE PARENTESCO], D. [NOMBRE Y APELLIDOS], una [PARTE] parte indivisa del activo hereditario líquido, que el heredero podrá pagar [ELEGIR: en dinero / en bienes de la herencia].

Limitación de responsabilidad por el legado

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Limitación total.

El heredero sólo responderá de la entrega de los legados hasta donde alcance el valor líquido del patrimonio hereditario, debiéndose reducir aquéllos en cuanto al exceso.

— Limitación parcial.

El heredero sólo responderá de la entrega de los legados hasta el [PORCENTAJE] % del valor líquido del patrimonio hereditario, debiéndose reducir aquéllos en cuanto al exceso.

Nombramiento de tutor o curador

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Tutor único.

Nombra tutor y, en su caso, curador de sus hijos a D./Dª [NOMBRE Y APELLIDOS].

— Tutor múltiple.

Nombra tutores de su hijo D. [NOMBRE Y APELLIDOS] a sus dos hijos D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], para que ejerzan las facultades de la tutela conjuntamente conforme al artículo 236.4 del Código Civil. En el supuesto de que por cualquier causa cese uno de los tutores nombrados, de conformidad con el artículo 238 del Código Civil y al efecto de que siempre sean dos las personas que desempeñen el cargo de tutor de forma conjunta, nombra como tales, por orden de prelación, a los siguientes: [NOMBRES Y APELLIDOS].

Nombramiento de contador partidor

Para el solo caso de que hubiere menores o personas con discapacidad que precisen apoyo al tiempo de la partición, nombra Contador-Partidor a D./Dª [NOMBRE Y APELLIDOS], con las más amplias facultades legales y en especial con la facultad de liquidar junto con el cónyuge viudo la sociedad conyugal, entregar legados y conmutar el usufructo del cónyuge viudo de acuerdo con éste, señalando como plazo para el ejercicio de su cargo el legal establecido.

RESERVAS Y ADVERTENCIAS LEGALES

Así lo dice y otorga, siendo las [HORA] horas y [MINUTOS] minutos.

Leo en alta voz el contenido de este testamento, por elección de su otorgante, advertida por mí de su derecho a leerlo por sí, y de explicarle yo, el Notario, su contenido, del que me manifiesta su conformidad, por ser fiel y exacta expresión de su voluntad, y se ratifica y firma conmigo.

De conocer a [EL/LA] compareciente y, en general, de haberse observado las formalidades legales en un solo acto y de todo lo demás consignado en este instrumento público, que queda extendido en [NÚMERO] folios de la clase [CLASE], serie [SERIE], números [NÚMEROS], el presente y el siguiente en orden, doy fe.
