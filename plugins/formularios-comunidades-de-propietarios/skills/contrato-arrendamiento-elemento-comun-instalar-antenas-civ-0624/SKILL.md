---
name: contrato-arrendamiento-elemento-comun-instalar-antenas-civ-0624
description: "Contrato de arrendamiento de un elemento común para instalar antenas de telefonía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de un elemento común para instalar antenas de telefonía

> Formulario **CIV-0624** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de un elemento común para instalar antenas de telefonía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de un elemento común para instalar antenas de telefonía” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:contrato-arrendamiento-elemento-comun-instalar-antenas-civ-0624`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (19 veces)
- [ ] Nº (7 veces)
- [ ] NOMBRE DE LA COMUNIDAD (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº REGISTRAL
- [ ] NÚMERO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

EXPONEN

I.- Que [DENOMINACIÓN SOCIAL] MÓVIL S.A., está procediendo a la implantación de una red de Estaciones Base un operador del servicio de telefonía móvil digital, por lo que está interesado en ocupar un espacio en la azotea de la finca que se indica, para la instalación en el mismo de los equipos que componen una Estación Base, para integrarla en la Red de Telefonía Móvil.

II.- Que LA COMUNIDAD es dueña en pleno dominio y sin limitación alguna, de los elementos comunes del inmueble situado en la localidad de [LOCALIDAD] c /, n° [Nº] y que figura inscrita en el Registro de la Propiedad de [LOCALIDAD], Libro n° [Nº] Tomo n° [Nº] Finca n° [Nº], Inscripción n° [Nº REGISTRAL]

III.- Que en consecuencia, ambas partes desean suscribir un acuerdo en virtud del cual [DENOMINACIÓN SOCIAL] MÓVIL S.A., arrienda la superficie definida en este documento para instalar, montar, explotar, mantener, conservar y reparar, por sí o por un tercero una Estación Base de Telefonía Móvil, con todos sus elementos y componentes, a cambio del pago a LA COMUNIDAD de una contraprestación económica.

De conformidad con lo expuesto, ambas partes convienen el presente contrato, con sujeción a las siguientes:

CLÁUSULAS

Objeto

La Comunidad de Propietarios [NOMBRE DE LA COMUNIDAD] arrienda un espacio de [Nº] m2 en la finca descrita a [DENOMINACIÓN SOCIAL] MÓVILES, S.A, que lo acepta, para la instalar, montar, explotar, mantener, conservar, reparar y modificar un equipo de telecomunicaciones, por si misma o por un tercero.

Asimismo la Comunidad de Propietarios de [NOMBRE DE LA COMUNIDAD] autoriza a [DENOMINACIÓN SOCIAL] MÓVILES, S.A a contratar por su cuenta y a sus expensas el suministro eléctrico y conexión telefónica necesarias para los equipos de telecomunicaciones. MÓVILES, S.A instalará en el edificio cables separados y contadores propios, para facilitar suministro eléctrico y telefónico a los equipos de telecomunicaciones.

En caso de que fuera necesario, [DENOMINACIÓN SOCIAL] MÓVILES, S.A podrá instalar un transformador en la finca, sin coste adicional en la renta.

Los servicios y suministros referidos serán de total responsabilidad de [DENOMINACIÓN SOCIAL] MÓVILES, S.A.

Renta

La renta pactada se establece en la cantidad de [IMPORTE] () EUROS, anuales, más el IVA correspondiente, que será abonada por meses vencidos, a partir del momento establecido en el párrafo siguiente.

El primer pago se realizará en los cinco días siguientes a la fecha en que se concluya la instalación de los equipos.

La contraprestación económica se incrementará o disminuirá anualmente de acuerdo con la variación porcentual experimentada por el índice Nacional de Precios al Consumo, que publique el organismo oficial correspondiente, quedando establecida como fecha de la primera revisión, el día de la suscripción del contrato.

El pago se realizará en la cuenta corriente señalada por la COMUNIDAD a tal efecto.

Fianza

La COMUNIDAD recibirá en concepto de fianza el importe equivalente a dos mensualidades que responderá del pago de la renta y posibles desperfectos que se ocasionaren en la finca.

Estando obligado a devolver dicho importe en el momento de la finalización o resolución del contrato de arrendamiento por cualquier causa, sin perjuicio de la función de garantía de la fianza.

Vigencia

El presente contrato tendrá una duración inicial de tres años, a partir de la fecha de la firma del mismo. Al final de este período, el contrato quedará automáticamente renovado, y se prorrogará por períodos sucesivos de cinco años, salvo que [DENOMINACIÓN SOCIAL] MÓVILES, S.A notifique a la Comunidad de Propietarios [NOMBRE DE LA COMUNIDAD] nº [NÚMERO] su intención de no renovarlo, con al menos seis meses de antelación a la terminación de cada período de cinco años, mediante carta certificada con acuse de recibo. Cada renovación lo será en los mismos términos y condiciones expresados en este documento.

Transcurridos veinte años de vigencia, ambas partes podrán ejercer su derecho a no renovar el contrato, comunicando su intención a la otra parte, con al menos seis meses de antelación a la fecha de vencimiento, mediante carta certificada.

Instalaciones

El cableado necesario para la instalación de los servicios, se realizará, preferentemente, por las canalizaciones propias de la comunidad y en su defecto, por el punto que acuerden las partes.

El sistema de antenas, con sus armazones correspondientes, se instalará sobre la azotea del edificio, en los puntos donde se logre la mejor prestación del servicio de telecomunicaciones, a criterio de [DENOMINACIÓN SOCIAL] MÓVILES, S.A.

Serán por cuenta de [DENOMINACIÓN SOCIAL] MÓVILES, S.A, todos los gastos de montaje, instalación, mantenimiento, reparación, modificación y retirada de la Estación Base.

La COMUNIDAD autoriza a [DENOMINACIÓN SOCIAL] MÓVILES, S.A, a realizar todas las modificaciones que fueran necesarias para la optimización de la Estación Base, tanto en la ubicación de los equipos como de las antenas, dentro del espacio arrendado.

MÓVILES, S.A se responsabilizará de la obtención de todas las licencias y autorizaciones que fueran precisas para el desarrollo de su actividad en el espacio contratado, así como del abono de todas las cantidades que se devenguen por este concepto. No obstante La COMUNIDAD se compromete a colaborar en todo lo que proceda, para la solicitud, tramitación y obtención de dichas autorizaciones.

Todos los elementos, componentes y partes de los equipos de telecomunicaciones, serán propiedad exclusiva de [DENOMINACIÓN SOCIAL] MÓVILES, S.A, por lo que una vez extinguido el contrato por cualquier causa, [DENOMINACIÓN SOCIAL] MÓVILES, S.A, conservará el dominio de los equipos de telecomunicaciones, siendo por su cuenta, los gastos de retirada.

La COMUNIDAD facilitará las actuaciones necesarias para proceder a dicha retirada, que será iniciada por el propietario de los equipos de telecomunicaciones o personas que éste designe dentro de los [Nº] días siguientes a la extinción del contrato.

MÓVILES, S.A se compromete una vez finalizado el contrato, a reponer el espacio ocupado a su situación original, salvo los desperfectos ocasionados por el uso normal del mismo.

Acceso

Mientras se mantenga la vigencia del contrato, La COMUNIDAD autoriza a [DENOMINACIÓN SOCIAL] MÓVILES, S.A y/o a las personas físicas o jurídicas que [DENOMINACIÓN SOCIAL] MÓVILES, S.A designe, el libre acceso a la finca para la preparación de los equipos de telecomunicaciones y depósito de materiales, maquinaria y herramientas, además de todo cuanto fuera necesario para llevar a cabo los trabajos que se requieran en la instalación, montaje, explotación, mantenimiento, conservación, reparación y modificación de los equipos de telecomunicaciones.

A estos efectos la COMUNIDAD facilitará a [DENOMINACIÓN SOCIAL] MÓVILES, S.A las llaves necesarias para acceder a la azotea. El horario habitual para revisiones y reparaciones será de 08:00 a 20:00 horas, a salvo de reparaciones de urgencias que podrán realizarse a cualquier hora del día.

Causas de resolución

Serán causas de resolución del presente contrato, las contenidas en el Título III de la Ley 29/1994, de 24 de Noviembre, de Arrendamientos Urbanos (falta de pago de la renta, falta de pago de la fianza o cuando tengan lugar actividades molestas, insalubres, nocivas, peligrosas o ilícitas).

Responsabilidad

MÓVILES, S.A será responsable de los daños ocasionados a la COMUNIDAD o a terceros, derivados de la instalación de sus equipos y del desarrollo de su actividad en el espacio arrendado. A estos efectos, [DENOMINACIÓN SOCIAL] MÓVILES, S.A. se obliga a tener contratado, durante todo el tiempo de vigencia del contrato, una póliza de seguro de responsabilidad civil, con entidad aseguradora de reconocida solvencia, que garantice suficientemente los riesgos mencionados, con un mínimo de [IMPORTE] euros.

Por su parte la COMUNIDAD, será responsable de los daños que produzca a los equipos de telecomunicaciones, siempre que se demuestre que la Comunidad de Propietarios es la causante, debiendo reparar los mismos y satisfacer la indemnización que se produzca

Interferencias

MÓVILES, S.A garantiza que no se producirá ningún tipo de interferencias con señales de radio y televisión derivadas de la instalación y/o funcionamiento de la estación base. No obstante lo anterior y en el improbable caso de que las interferencias se produjeran, [DENOMINACIÓN SOCIAL] MÓVILES, S.A se compromete a investigar la causa de las mismas; si tras esta investigación quedara fehacientemente demostrado que dichas interferencias han sido producidas por los equipos de telecomunicaciones instalados, [DENOMINACIÓN SOCIAL] MÓVILES, S.A dispondrá de un plazo de [Nº] días para su subsanación.

[ELEGIR UNA OPCIÓN: Sometimiento a tribunales / Sumisión a tribunales / Renuncia al fuero propio / Sin renuncia al fuero propio]

Sumisión a arbitraje

Para dirimir cualquier controversia o reclamación derivada del cumplimiento y aplicación de este contrato, las partes se someten, con renuncia a su fuero propio si fuera otro, al arbitraje de

Normativa aplicable

En todo lo no expresamente previsto en este contrato será de aplicación cuanto sobre el arrendamiento de bienes inmuebles destinados a uso distinto del de vivienda se establece en la ley de Arrendamientos Urbanos y el Código Civil.

Y en prueba de conformidad con cuanto antecede, firman ambas partes el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

Fdo.: Fdo.:

LA COMUNIDAD [DENOMINACIÓN SOCIAL] MÓVILES, S.A

========================================================================
