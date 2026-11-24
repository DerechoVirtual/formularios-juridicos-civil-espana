---
name: contrato-arrendamiento-local-uso-distinto-vivienda-civ-0500
description: "Contrato de arrendamiento de local para uso distinto del de vivienda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de local para uso distinto del de vivienda

> Formulario **CIV-0500** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de local para uso distinto del de vivienda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de local para uso distinto del de vivienda” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-local-uso-distinto-vivienda-civ-0500`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] DIRECCIÓN ELECTRÓNICA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] AÑO
- [ ] CARÁCTER DE LA TITULARIDAD
- [ ] CONDICIONES DE ADMISIÓN O EXCLUSIÓN
- [ ] CONDICIONES DE INSPECCIÓN
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DURACIÓN
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NORMATIVA APLICABLE
- [ ] PERIODICIDAD
- [ ] PLAZO
- [ ] PROVINCIA
- [ ] RÉGIMEN DE LAS OBRAS REALIZADAS
- [ ] RÉGIMEN DE LOS SERVICIOS
- [ ] SISTEMA DE ACTUALIZACIÓN
- [ ] TIPO DE CONTRATO
- [ ] TIPO DE MEDIACIÓN
- [ ] USO DEL LOCAL
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 35 LAU
- art. 32.3 LAU
- art. 36 LAU

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

ARRENDAMIENTO DE LOCALES PARA USO DISTINTO DEL DE VIVIENDA

En la ciudad de [LOCALIDAD] a [DÍA] de [MES] de [AÑO]

REUNIDOS

ARRENDADOR

NOMBRE Y APELLIDOS, mayor de edad, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], que deja designado a efectos de notificaciones y avisos en relación con el presente contrato. D.N.I. número y letra

ARRENDATARIO

NOMBRE Y APELLIDOS, mayor de edad, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], que deja designado a efectos de notificaciones y avisos en relación con el presente contrato. D.N.I. número y letra

INTERVIENEN

En su propio nombre y derecho/en nombre y representación de [NOMBRE DEL REPRESENTADO/A]

como mandatario verbal de [NOMBRE Y APELLIDOS] y a reserva de su ratificación, que se hará constar por nota firmada y fechada a continuación del presente documento.

Recíprocamente se reconocen, en los conceptos de su respectiva intervención, la capacidad necesaria para otorgar el presente contrato de [TIPO DE CONTRATO], y

EXPONEN

I. que es titular con carácter [CARÁCTER DE LA TITULARIDAD], del local [DESCRIPCIÓN DEL BIEN].

II. Sobre tales bases,

ESTIPULACIONES

Clase de arrendamiento. local y accesorios. uso y actividades a desarrollar

D/Dª [NOMBRE Y APELLIDOS]. cede en arrendamiento, concertado para finalidad distinta de la de vivienda [USO DEL LOCAL]) a D/Dª [NOMBRE Y APELLIDOS] que acepta en esos términos, el local descrito a la base I antecedente.

Duración

La relación se concierta por término de [DURACIÓN] a partir de [FECHA]

Condiciones de admisión o exclusión [CONDICIONES DE ADMISIÓN O EXCLUSIÓN]

Actualización

Arrendador y arrendatario, de común acuerdo fijan la renta en [IMPORTE], pagaderas en la moneda que sea de curso legal en España al tiempo del pago, por [PERIODICIDAD], mediante [ÓRGANO].

La renta se actualizará [SISTEMA DE ACTUALIZACIÓN].

Sin perjuicio de lo dispuesto en el art. 35 LAU, la falta de pago de la renta actualizada, a su vencimiento, dará derecho al arrendador a ejecutar lo que se estipula (en su caso) en la cláusula Undécima.

Destino

El arrendatario no podrá, sin previo permiso por escrito del arrendador, desarrollar en el local arrendado actividad distinta de la que se indica en la cláusula tercera.

Cesiones y subarriendos

Ejemplo de cláusula restrictiva: No podrá el arrendatario ceder su derecho ni subarrendar, total o parcialmente. Las hipótesis contempladas en el art. 32.3 LAU se considerarán cesión inconsentida. Lo mismo se entenderá respecto de la sociedad unipersonal, anónima o de responsabilidad limitada constituida por el arrendatario. La ocupación por el que hubiera sido único socio, en el local inicialmente arrendado a la sociedad unipersonal, después disuelta, tendrá la misma consideración.

Régimen de obras, autorizaciones, gastos, destino de lo realizado. Compensaciones. Obtención de licencias, servicios accesorios

Se faculta al arrendatario para realizar en el plazo de [PLAZO] para obrar lo necesario al uso pactado para el local, colocar anuncios y rótulos alusivos a su actividad en la proyección del local sobre la fachada, sin ruidos o luces que puedan molestar a los demás vecinos del inmueble. Transcurrido ese plazo, cualquier obra necesitará consentimiento escrito del arrendador y, en todo caso, las que afecten a la seguridad del inmueble o modifiquen su configuración. Los gastos causados por las obras, la obtención y abono de las licencias y permisos administrativos pertinentes, que condicionan, en todo caso, el ejercicio de la facultad concedida al arrendatario, corren de cargo del [ELEGIR: arrendador / arrendatario].

Las obras realizadas [RÉGIMEN DE LAS OBRAS REALIZADAS].

El arrendador podrá inspeccionar el local arrendado, [CONDICIONES DE INSPECCIÓN].

Sin perjuicio de lo que se dispone en la cláusula Décima la infracción de lo estipulado en los párrafos anteriores de la presente, facultará al arrendador para exigir, a costa del arrendatario, la reposición de las cosas a su estado anterior a las obras no autorizadas.

Servicios

El mantenimiento de los servicios [RÉGIMEN DE LOS SERVICIOS]

Sobre los gastos de la presente formalización y los ulteriores de escritura pública e inscripción registral

Los gastos que se ocasionen por los conceptos del epígrafe serán de cuenta de [ELEGIR: arrendador / arrendatario / ambas]

Fianza

En cumplimiento de lo dispuesto en el art. 36 LAU, el arrendatario entrega en este acto al arrendador la suma de [IMPORTE], equivalente a dos mensualidades de renta, para que éste proceda a la constitución de la fianza mediante su depósito en la Administración o Entidad pública correspondiente (Caben pactos con efectos entre las partes, sobre legitimación, obligación y responsabilidad al pago. Pero lo más aconsejable es lo que se propone fuera del paréntesis).

Causas de resolución

El incumplimiento de las obligaciones establecidas en el presente contrato, dará derecho a la parte que esté al corriente en el cumplimiento de las suyas a resolver la relación y (alternativa o cumulativamente) ejecutar las garantías que se establecen en la cláusula Undécima siguiente.

Garantías adicionales

(Pueden convenirse las admitidas en derecho, incluso las consistentes en depósitos de dinero a disposición, llegado el caso, del beneficiario de la garantía. Todas están exentas del régimen del art. 36, aunque no está de más hacer mención expresa de esa circunstancia. Debe preverse causas y formas de cancelación de las garantías que se constituyan)

Sumisión a mediación y/o arbitraje; jurisdicción competente y ley aplicable

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación [TIPO DE MEDIACIÓN] de ……………………, antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y [NORMATIVA APLICABLE] fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de……………………, a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Juez de Primera Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Título III de la Ley de Arrendamientos Urbanos de 24 de Noviembre de 1.994 y, supletoriamente, por lo dispuesto en el Código Civil.

Notificaciones

A efectos de notificaciones o emplazamientos judiciales, y en general, toda comunicación o requerimiento que hayan de oír las partes en relación con el presente contrato, se tomará como domicilio del arrendador el señalado al inicio del presente contrato, es decir, calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], y como domicilio del arrendatario, el de la calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de

De conformidad a lo dispuesto en el artículo 4.6 de la Ley de Arrendamientos Urbanos, las partes designan las siguientes direcciones electrónicas para realizar las notificaciones:

- Por el arrendador [DIRECCIÓN ELECTRÓNICA]

- Por el arrendatario [DIRECCIÓN ELECTRÓNICA]

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.
