---
name: poder-notarial-general-pleitos-especial-otras-civ-0861
description: "Poder notarial general para pleitos y especial para otras facultades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Poder notarial general para pleitos y especial para otras facultades

> Formulario **CIV-0861** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial de poder otorgado por una sociedad mercantil a favor de abogados y procuradores, con facultades generales para pleitos y facultades especiales (recursos extraordinarios, transacción, arbitraje, allanamiento, concurso, cobro de cantidades, actas notariales, sustitución, etc.), incluida la facultad de solicitar el concurso de la propia sociedad.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Poder notarial general para pleitos y especial para otras facultades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Poder notarial general para pleitos y especial para otras facultades” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:poder-notarial-general-pleitos-especial-otras-civ-0861`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] AÑO
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES
- [ ] DNI/NIF
- [ ] DOMICILIO
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FIRMA - NOMBRE DEL NOTARIO
- [ ] FIRMA - NOMBRE Y APELLIDOS
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL COMPARECIENTE
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] NÚMEROS
- [ ] REGISTRO Y DATOS DE INSCRIPCIÓN
- [ ] SERIE
- [ ] TÍTULO DE LA REPRESENTACIÓN: CARGO O PODER

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…os de acuerdos, aceptar cargos y designar vocales de organismos de conciliación.»: el original aludía a suspensión de pagos, quiebra y síndicos, figuras ya derogadas; se ha adaptado a la terminología del texto refundido de la Ley Concursal (RDLeg 1/2020). Revisar la redacción conforme a dicho texto.
- Junto a «…ndo de las facultades anteriormente consignadas y cuantas demás sean necesarias.»: el original citaba el art. 6.2.1.º de la Ley 22/2003, de 9 de julio, Concursal, derogada por el texto refundido de la Ley Concursal (RDLeg 1/2020); comprobar el artículo equivalente en dicho texto refundido (requisitos del poder especial para solicitar el concurso).

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

NÚMERO [Nº DE PROTOCOLO]

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL], con residencia en [LOCALIDAD],

COMPARECE

[NOMBRE Y APELLIDOS DEL COMPARECIENTE], mayor de edad, estado civil [ESTADO CIVIL], domiciliado/a en [DOMICILIO], con DNI/NIF [DNI/NIF].

INTERVIENE en nombre y representación de la mercantil denominada [DENOMINACIÓN SOCIAL].

INSCRITA en [DATOS REGISTRALES].

NÚMERO DE IDENTIFICACIÓN FISCAL: [NIF].

Usa de las facultades que legal y reglamentariamente le corresponden en virtud de [TÍTULO DE LA REPRESENTACIÓN: CARGO O PODER].

INSCRITA en el [REGISTRO Y DATOS DE INSCRIPCIÓN].

Juzgo al compareciente, al que identifico por el documento reseñado, con capacidad suficiente para otorgar esta escritura de PODER GENERAL PARA PLEITOS Y ESPECIAL PARA OTRAS FACULTADES, a cuyo fin,

DICE:

Que confiere poder, tan amplio y bastante como en Derecho sea necesario y de forma solidaria, a favor de los Letrados: don/doña [NOMBRE Y APELLIDOS], don/doña [NOMBRE Y APELLIDOS], don/doña [NOMBRE Y APELLIDOS], don/doña [NOMBRE Y APELLIDOS], don/doña [NOMBRE Y APELLIDOS] y don/doña [NOMBRE Y APELLIDOS], y Procuradores de los Tribunales de [LOCALIDAD]: don/doña [NOMBRE Y APELLIDOS], don/doña [NOMBRE Y APELLIDOS] y don/doña [NOMBRE Y APELLIDOS], para que, en la representación antedicha, ejerciten las siguientes facultades:

FACULTADES GENERALES PARA PLEITOS

Comparecer ante cualesquiera Audiencias y demás Tribunales, ordinarios o especiales, de cualquier grado o jurisdicción, y ante cualquier otra autoridad, Magistratura, Fiscalía, Organismos Sindicales, Delegación, Junta, Jurado, Tribunal de Competencia o de Cuentas del Estado, Autoridad Eclesiástica, Centro, Notaría, Registro Público, Administración de Hacienda o Agencia Tributaria, oficina o funcionario del Estado, Administración Central, Comunidad Autónoma, Provincia, Municipio o cualesquiera otras entidades locales, organismos autónomos y demás entes públicos, incluso internacionales, en particular de la Unión Europea, y demás Entidades creadas y por crear, en cualquiera de sus ramas, dependencias y servicios; y en ellos, instar, seguir y terminar, como actor, demandado, tercero, coadyuvante, requirente o en cualquier otro concepto, toda clase de expedientes, juicios y procedimientos, civiles, criminales, administrativos, sociales, contencioso-administrativos, económico-administrativos, de trabajo, gubernativos, notariales, hipotecarios, de Hacienda, de jurisdicción voluntaria y de cualquier otra clase.

En todos estos casos, entablar, contestar y seguir por todos sus trámites e instancias, hasta su conclusión, toda clase de acciones, demandas, denuncias, querellas, acusaciones, excepciones y defensas y ejercitar otras cualesquiera pretensiones, pedir suspensiones de juicios o procedimientos, ejercitándose en cuantos casos fuera menester la ratificación personal; firmar y presentar escritos y asistir a toda clase de actuaciones; solicitar y recibir notificaciones, citaciones y emplazamientos.

Dirigir, recibir y contestar requerimientos y notificaciones. Interponer recursos de alzada y cualquier otro acto previo al proceso.

Tachar testigos; suministrar y tachar pruebas, renunciar a ellas y a traslados de autos. Absolver posiciones y confesar en juicio y en todo tipo de interrogatorios previstos por la ley.

Instar autorizaciones judiciales, declaraciones de herederos, expedientes de dominio, acumulaciones, liquidaciones y tasaciones de costas; promover conflictos de jurisdicción, cuestiones de competencia, diligencias preliminares, preparatorias o previas, y otras cuestiones incidentales, siguiéndolas hasta que se dicte auto o resolución pertinente. Ser parte en juicios de testamentaría o abintestato hasta su resolución, pudiendo presentar o dar conformidad a proyectos de partición. Consentir las resoluciones favorables.

Interponer y seguir toda clase de recursos, incluso los gubernativos y contencioso-administrativos y los de reposición, alzada, reforma, súplica, apelación, injusticia notoria, suplicación, queja, nulidad e incompetencia, anulación, aclaración, revisión; interponer y seguir recurso de amparo ante el Tribunal Constitucional, así como los extraordinarios de casación o interés casacional y los extraordinarios por infracción procesal, y demás procedentes en Derecho y, en general, practicar cuanto permitan las respectivas leyes de procedimiento sin limitación.

Instar, prestar, alzar o cancelar embargos, secuestros, depósitos, ejecuciones, desahucios y anotaciones preventivas, así como pedir administraciones, intervenciones o cualquier otra medida de conservación, seguridad, prevención o garantía, y modificarlas o extinguirlas; designar peritos. Intervenir en subastas judiciales y extrajudiciales, ceder remates a terceros o aceptar las cesiones que otros hicieren a favor del poderdante; pedir desahucios y lanzamientos; tomar posesión de los bienes muebles o inmuebles que deban hacerlo como consecuencia de los juicios en que intervengan. Prestar cauciones; hacer depósitos y consignaciones judiciales, así como percibir del Tribunal de Instancia las cantidades consignadas como precio del remate.

FACULTADES ESPECIALES

Interponer los recursos extraordinarios de casación y revisión. Desistir de cualquier recurso, incluso los de casación y revisión. Promover la recusación de señores Magistrados.

Celebrar actos de conciliación, con avenencia o sin ella, en cuanto impliquen actos dispositivos. Transigir, someter a arbitraje las cuestiones controvertidas u otras surgidas después. Otorgar ratificaciones personales en nombre de la parte poderdante. Renunciar o reconocer derechos; allanarse; renunciar a la acción de derecho discutida o a la acción procesal, o desistir de ellas; aceptar y rechazar las proposiciones del deudor, así como realizar manifestaciones que puedan comportar sobreseimiento del proceso por satisfacción extraprocesal o carencia sobrevenida de objeto.

Promover y personarse en los procedimientos concursales, y seguirlos hasta su conclusión y, especialmente, intervenir con voz y voto en junta de acreedores y para la aprobación del convenio de que se trate, nombrar administradores concursales, interventores y miembros de tribunales colegiados. Reconocer y graduar créditos, cobrar éstos e impugnar los actos de acuerdos, aceptar cargos y designar vocales de organismos de conciliación.

Percibir cantidades, indemnizatorias o no, resultantes de decisiones judiciales favorables a la parte poderdante, ya figuren en nombre del poderdante o del apoderado. Los apoderados quedan facultados para que en nombre de los poderdantes puedan cobrar o percibir de los organismos jurisdiccionales o entidades bancarias correspondientes cuantas órdenes de pago o mandamientos de devolución se expidan a sus respectivos nombres en los procesos que se sigan y por las cuantías que resulten devueltas o abonadas.

Instar la autorización de actas notariales, de presencia, requerimiento, notificación, referencia, protocolización, declaración de herederos abintestato u otras de notoriedad, remisión de documentos, exhibición, depósito voluntario o cualesquiera otras, incluida la intervención en las subastas notariales.

Vigente la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, a los efectos específicos de la comparecencia y posible arreglo, renuncia, transacción o allanamiento previstos en su artículo 414.2, poder efectuar éstos, con independencia del tipo de procedimiento de que se trate y de sus circunstancias concretas de identificación procesal.

Sustituir el presente poder a favor de señores Procuradores o Letrados y solicitar las copias que se precisen de este poder.

Percibir del Fondo de Garantía Salarial, de la Tesorería General de la Seguridad Social o de cualquier otra entidad pagadora que en el futuro se cree o sustituya a dichos organismos, todas las cantidades que pudieran corresponder por cualquier concepto a la parte poderdante como consecuencia de la relación laboral que mantienen o mantuvo con la empresa donde prestaba o presta sus servicios; y facultar a las indicadas entidades pagadoras para subrogarse en los derechos de la parte poderdante, para el ejercicio de todo tipo de acciones que resultaran procedentes en Derecho.

Y cualquier otra facultad, no enumerada anteriormente, de las comprendidas en los artículos 25 y 414.2 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil.

[OPCIONAL — incluir si procede]

Y, específicamente, les faculta con carácter especial, a los efectos previstos en el artículo 6.2.1.º de la Ley Concursal, para promover y solicitar el concurso de «[DENOMINACIÓN SOCIAL], S.A.», continuando el procedimiento por todos sus trámites, presentando cuantos escritos resulten precisos y, en suma, realizando cuanto sea factible, usando de las facultades anteriormente consignadas y cuantas demás sean necesarias.

AUTORIZACIÓN

Así lo dice y otorga el compareciente don/doña [NOMBRE Y APELLIDOS], a quien hago las reservas y advertencias legales.

Por no hacer uso del derecho que tiene a hacerlo por sí, del que advierto, leo la presente a don/doña [NOMBRE Y APELLIDOS], compareciente; la encuentra conforme y, prestando su consentimiento al contenido de ésta, firma conmigo, el Notario, todo lo contenido en este instrumento público, extendido en [Nº] folios de papel timbrado de uso exclusivo notarial, serie [SERIE] y números [NÚMEROS].

DOY FE.

Notario: [FIRMA - NOMBRE DEL NOTARIO]

Otorgante: [FIRMA - NOMBRE Y APELLIDOS]
