---
name: demanda-juicio-ordinario-accidente-trafico-contra-civ-0850
description: "Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros

> Formulario **CIV-0850** del plugin **Accidentes, seguros y responsabilidad civil** (`formularios-accidentes-y-responsabilidad-civil`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio ordinario, dirigida a la Sección Civil del Tribunal de Instancia, en reclamación de daños y perjuicios ocasionados con motivo de la circulación de vehículos de motor contra el Consorcio de Compensación de Seguros (en el modelo, por daños causados por un vehículo con estacionamiento habitual en España que carecía de seguro), por cantidad superior a 15.000 euros.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros” para mi caso». También puedes invocarla directamente con `/formularios-accidentes-y-responsabilidad-civil:demanda-juicio-ordinario-accidente-trafico-contra-civ-0850`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-accidentes-y-responsabilidad-civil:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Accidentes, seguros y responsabilidad civil) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (20 veces)
- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MATRÍCULA (4 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] MARCA (3 veces)
- [ ] MODELO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE, NÚMERO, CIUDAD (2 veces)
- [ ] FIRMA (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN
- [ ] DESCRIPCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EXPOSICIÓN DETALLADA DE LOS HECHOS
- [ ] FACTORES
- [ ] FECHAS
- [ ] HORA
- [ ] LESIONES
- [ ] LESIONES Y SECUELAS
- [ ] MEDIO DE ACREDITACIÓN
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PUNTOS
- [ ] Nº DE TELÉFONO
- [ ] PROVINCIA
- [ ] RAZONES
- [ ] SEDE
- [ ] TIPO DE SINIESTRO
- [ ] VÍA

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 15 Ley 52/1997
- art. 84.1.a Ley 40/2015
- art. 10 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1902 Código Civil
- art. 20.6 Ley 50/1980
- art. 253.1 LEC
- art. 23 LEC
- art. 24.2 LEC

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

- Junto a «…s esenciales (reforma operada por el Real Decreto-ley 3/2013, de 22 de febrero).»: este reconocimiento tuvo su origen en la tasa judicial; comprobar su vigencia y el régimen actual de tasas, de las que las personas físicas están exentas desde el Real Decreto-ley 1/2015.
- Junto a «…idente. TEXTO DEL ESCRITO A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS EXPLICATIVAS (no forman parte del escrito; suprimir antes de presentar)

El Consorcio de Compensación de Seguros, como organismo cuya actividad está inspirada en el principio de compensación, tiene por fin cubrir los riesgos en los seguros determinados en su Estatuto legal.

El Consorcio responde en materia de tráfico hasta los límites del aseguramiento obligatorio y en los casos siguientes:

a) Indemnizar a quienes hubieran sufrido daños en sus personas, por siniestros ocurridos en España, en aquellos casos en que el vehículo causante sea desconocido.

b) Indemnizar los daños a las personas y en los bienes ocasionados con un vehículo que tenga su estacionamiento habitual en España, así como los ocasionados dentro del territorio español a personas con residencia habitual en España o a bienes de su propiedad situados en España con un vehículo con estacionamiento habitual en un tercer país no firmante del acuerdo entre las oficinas nacionales de seguros de los Estados miembros del Espacio Económico Europeo y de otros Estados asociados, en ambos casos cuando dicho vehículo no esté asegurado.

c) Indemnizar los daños a las personas y en los bienes producidos por un vehículo con estacionamiento habitual en España que, estando asegurado, haya sido robado, entendiéndose como tal exclusivamente las conductas tipificadas como robo y robo de uso en los artículos 237 y 244 del Código Penal, respectivamente.

d) Indemnizar los daños a las personas y en los bienes cuando, en supuestos incluidos dentro del ámbito del aseguramiento de suscripción obligatoria o en los párrafos precedentes, surgiera controversia entre el Consorcio de Compensación de Seguros y la entidad aseguradora acerca de quién debe indemnizar al perjudicado. No obstante lo anterior, si ulteriormente se resuelve o acuerda que corresponde indemnizar a la entidad aseguradora, ésta reembolsará al Consorcio de Compensación de Seguros la cantidad indemnizada más los intereses legales, incrementados estos últimos en un 25 por 100 desde la fecha en que abonó la indemnización. Se entiende que existe controversia cuando la entidad aseguradora presente ante el Consorcio requerimiento motivado en relación al siniestro, o el perjudicado presente reclamación ante el Consorcio a la que acompañe justificación de que la entidad aseguradora rehúsa hacerse cargo del siniestro, y el Consorcio estimase que no le corresponde el pago.

e) Indemnizar los daños a las personas y en los bienes cuando la entidad española aseguradora del vehículo con estacionamiento habitual en España hubiera sido declarada judicialmente en concurso o, habiendo sido disuelta y encontrándose en situación de insolvencia, estuviese sujeta a un procedimiento de liquidación intervenida o ésta hubiera sido asumida por el propio Consorcio de Compensación de Seguros.

f) Reembolsar las indemnizaciones satisfechas a los perjudicados residentes en otros Estados del Espacio Económico Europeo por los organismos de indemnización en los siguientes supuestos: cuando el vehículo causante del accidente tenga su estacionamiento habitual en España, en el caso de que no pueda identificarse a la entidad aseguradora; cuando el accidente haya ocurrido en España, en el caso de que no pueda identificarse el vehículo causante; y cuando el accidente haya ocurrido en España, en el caso de vehículos con estacionamiento habitual en terceros países adheridos al sistema de Certificado Internacional del Seguro del Automóvil, expedido por una oficina nacional conforme a la recomendación número 5 adoptada el 25 de enero de 1949 por el Subcomité de Transportes por Carretera del Comité de Transportes Interiores de la Comisión Económica para Europa de la ONU (Carta Verde).

En los supuestos previstos en las letras b) y c) quedarán excluidos de la indemnización por el Consorcio los daños a las personas y en los bienes sufridos por quienes ocuparen voluntariamente el vehículo causante del siniestro, conociendo que el mismo no estaba asegurado o que había sido robado, siempre que el Consorcio probase que aquéllos conocían tales circunstancias. Se aplicará, además, en el supuesto de daños en los bienes, la franquicia que legalmente se determine.

Los perjudicados con residencia en España pueden presentar ante OFESAUTO, en su condición de organismo de indemnización español, reclamación por los perjuicios sufridos en los supuestos del artículo 20 y con los requisitos del artículo 27 del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor.

El actor ha de comparecer con abogado y procurador si su pretensión supera los 2.000 euros y debe acompañar a la demanda todos los documentos que utilice como prueba y que estén a su disposición o pueda conseguir y los informes periciales de que intente valerse.

La norma recoge la posibilidad de acción directa contra el Consorcio: artículo 20 del Real Decreto 1507/2008, de 12 de septiembre, y artículo 11.3 del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor.

La Ley 18/2011, de 5 de julio, regula el expediente judicial electrónico, el documento judicial electrónico, las copias y archivos de documentos electrónicos y el registro electrónico.

La asistencia jurídica gratuita reconoce, para litigar por la indemnización por daños personales y morales, a quienes, a causa de un accidente, acrediten secuelas permanentes que les impidan totalmente la realización de su actividad profesional o laboral y requieran ayuda de terceros en sus actividades diarias esenciales (reforma operada por el Real Decreto-ley 3/2013, de 22 de febrero).

La Ley 35/2015 modifica el baremo de indemnizaciones por accidentes de tráfico. La indemnización por lesiones temporales contempla el perjuicio personal básico, el perjuicio personal particular (la indemnización diaria está en función de la pérdida temporal de calidad de vida, que puede ser muy grave, grave o moderada, e incluye el perjuicio personal básico) y el daño patrimonial, que a su vez incluye el daño emergente (gastos de asistencia sanitaria y diversos gastos resarcibles que comprenden el incremento de los costes de movilidad, desplazamientos de familiares, etc.) y el lucro cesante, que está en función de los ingresos netos del perjudicado deducidas las prestaciones públicas por la causa del accidente.


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
