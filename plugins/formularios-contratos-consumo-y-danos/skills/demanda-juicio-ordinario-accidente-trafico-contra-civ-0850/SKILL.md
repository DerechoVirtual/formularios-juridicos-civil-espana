---
name: demanda-juicio-ordinario-accidente-trafico-contra-civ-0850
description: "Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros

> Formulario **CIV-0850** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario, dirigida a la Sección Civil del Tribunal de Instancia, en reclamación de daños y perjuicios ocasionados con motivo de la circulación de vehículos de motor contra el Consorcio de Compensación de Seguros (en el modelo, por daños causados por un vehículo con estacionamiento habitual en España que carecía de seguro), por cantidad superior a 15.000 euros.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-accidente-trafico-contra-civ-0850`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

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

TEXTO DEL ESCRITO

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [CALLE, NÚMERO, CIUDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC) (elegir opción en función de cómo se haya otorgado el poder) (1)

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si el poder se otorga a través de la sede judicial electrónica): mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como documento n.º [Nº], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga mediante comparecencia apud acta): mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como documento n.º [Nº], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga ante Notario): mediante escritura de poder otorgada a mi favor ante el/la Notario/a [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como documento n.º [Nº], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [CALLE, NÚMERO, CIUDAD], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO EN RECLAMACIÓN DE DAÑOS Y PERJUICIOS OCASIONADOS CON MOTIVO DE LA CIRCULACIÓN DE VEHÍCULOS DE MOTOR, contra el Consorcio de Compensación de Seguros, Delegación de [PROVINCIA], con domicilio en [DOMICILIO], actuando en calidad de aseguradora del vehículo [DESCRIPCIÓN], marca [MARCA], modelo [MODELO], matrícula [MATRÍCULA]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [Nº DE TELÉFONO].

HECHOS

PRIMERO.- El día [FECHA], sobre las [HORA] horas, y cuando circulaba por [VÍA], se produjo [TIPO DE SINIESTRO] entre el vehículo marca [MARCA], modelo [MODELO], con matrícula [MATRÍCULA], conducido por D./Dña. [NOMBRE Y APELLIDOS], y el automóvil conducido por el demandante D./Dña. [NOMBRE Y APELLIDOS], marca [MARCA], modelo [MODELO], matrícula [MATRÍCULA] [EXPOSICIÓN DETALLADA DE LOS HECHOS].

SEGUNDO.- Como consecuencia de los hechos descritos se han ocasionado diversos daños materiales y corporales. En cuanto a los primeros, se reclama el coste de la reparación total del vehículo, que asciende a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), según se acredita con la correspondiente factura que se acompaña.

Por lo que respecta a los daños corporales, mi representado ha permanecido [Nº] días de baja, de los cuales [Nº] ha estado hospitalizado en la Clínica [DENOMINACIÓN], causándosele [LESIONES Y SECUELAS], según se acredita con el oportuno informe médico.

TERCERO.- El citado vehículo, con matrícula [MATRÍCULA], tenía su estacionamiento habitual en España y no estaba asegurado en el momento del accidente.

CUARTO.- El Consorcio de Compensación de Seguros fue requerido de pago el día [FECHA], según queda acreditado mediante [MEDIO DE ACREDITACIÓN] que se acompaña como documento número [Nº], habiendo transcurrido más de tres meses sin haber sido efectuada oferta motivada de indemnización.

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN.

Los Tribunales españoles conocerán de los juicios que se susciten en territorio español en materia de obligaciones extracontractuales cuando el hecho del que deriven haya ocurrido en territorio español, conforme establece el artículo 22 quinquies.b) de la Ley Orgánica del Poder Judicial.

II.- COMPETENCIA.

El artículo 15 de la Ley 52/1997, de 27 de noviembre, de Asistencia Jurídica al Estado e Instituciones Públicas, que se declara en vigor expresamente por el párrafo 2.º, apartado 3.º, de la disposición derogatoria única de la Ley de Enjuiciamiento Civil, confiere la competencia territorial para conocer de los procesos civiles en que sea parte el Estado y las Entidades estatales de Derecho Público a los Tribunales que tengan su sede en las capitales de provincia, en Ceuta o Melilla. Demandado el Consorcio de Compensación de Seguros, cuya naturaleza jurídica, según el artículo 1 de su Estatuto Legal, es de entidad pública empresarial de las previstas en el art. 84.1.a) de la Ley 40/2015, de 1 de octubre, de Régimen Jurídico del Sector Público, con personalidad jurídica propia y plena capacidad de obrar, resulta territorialmente competente el Tribunal al que nos dirigimos, por ser el de la capital de la provincia en cuyo territorio ocurrió el accidente.

III.- PROCEDIMIENTO.

Los arts. 248, 249.2 y 399 y siguientes LEC sobre la procedencia del juicio declarativo ordinario instado.

IV.- LEGITIMACIÓN.

Está legitimado activamente mi representado por ser quien ha sufrido los daños materiales y corporales consecuencia del siniestro (art. 10 LEC).

Está legitimado pasivamente el Consorcio de Compensación de Seguros por no tener D./Dña. [NOMBRE Y APELLIDOS] asegurado su vehículo en el momento del accidente.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FUNDAMENTOS JURÍDICO-MATERIALES.

1.- En esta demanda se ejercita la acción que nace de la culpa o negligencia del artículo 1902 del Código Civil para obtener la indemnización correspondiente por los daños y perjuicios ocasionados por accidente de circulación, ya que se da la producción de un daño, como consecuencia de una acción (u omisión) culposa, mediando la debida relación de causalidad, requisitos que se dan cumplidamente en este caso.

2.- El artículo 11.3 del texto refundido del Estatuto legal del Consorcio de Compensación de Seguros, aprobado por Real Decreto Legislativo 7/2004, de 29 de octubre, establece entre sus funciones aquellas que le encomienda el artículo 11 del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre. Entre estas funciones está la de indemnizar los daños ocasionados a las personas y en las cosas por un vehículo que tenga su estacionamiento habitual en España y no esté asegurado. El pago de dicha indemnización no puede quedar condicionado a la prueba por parte del perjudicado de que la persona responsable no puede pagar o no quiere hacerlo.

3.- El artículo 11.3 del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor señala que el perjudicado tendrá acción directa contra el Consorcio de Compensación de Seguros en los casos señalados en dicho artículo.

Para el ejercicio de acciones civiles contra el Consorcio no será necesaria la reclamación previa en vía administrativa, según establece el artículo 21 de su Estatuto Legal, aprobado por Real Decreto Legislativo 7/2004, de 29 de octubre.

Se ha requerido previamente al Consorcio, habiendo transcurrido más de tres meses sin haber sido atendido dicho requerimiento (artículo 20 de su Estatuto Legal).

4.- Cuantificación de los daños.

4.1.- Daños corporales: el anexo del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor fija el sistema para la valoración de los daños y perjuicios causados a las personas en accidente de circulación. Para el año [AÑO], las cuantías de las indemnizaciones por muerte, lesiones permanentes e incapacidad permanente son:

[OPCIONAL — si ha lugar]

A) Indemnización por incapacidad temporal.

Días de baja durante estancia hospitalaria: indemnización diaria [IMPORTE] euros ([IMPORTE] €). Son [IMPORTE] euros ([IMPORTE] €).

Días de baja sin estancia hospitalaria: indemnización diaria [IMPORTE] euros ([IMPORTE] €). Son [IMPORTE] euros ([IMPORTE] €).

Factores de corrección: [SE INDICARÁN, EN SU CASO, LOS FACTORES DE CORRECCIÓN Y EL PORCENTAJE APLICABLE]

Total por incapacidad: [IMPORTE] euros ([IMPORTE] €).

[OPCIONAL — si ha lugar]

B) Indemnización por lesión permanente.

Concreción de las lesiones permanentes: [LESIONES]

Puntos asignados: [Nº DE PUNTOS]

Valor de los puntos en [IMPORTE] euros: [IMPORTE]

Factores de corrección: [FACTORES]

Total por lesiones: [IMPORTE] euros ([IMPORTE] €).

[OPCIONAL — si ha lugar]

C) Además se satisfarán en todo caso los gastos de asistencia médica y hospitalaria. (En su caso, en las indemnizaciones por muerte se satisfarán también los gastos de entierro y funeral.)

Total por gastos de asistencia: [IMPORTE] euros ([IMPORTE] €).

4.2.- Daños materiales: la indemnización viene fijada por los efectivamente sufridos.

Los gastos de reparación del vehículo ascienden a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €).

VII.- MORA.

El artículo 9 del texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre, establece que para que el asegurador, en este caso el Consorcio, no incurra en mora en el cumplimiento de su prestación, ha de formular oferta motivada de indemnización de daños y perjuicios debidos por el asegurador, conforme al art. 7 del propio texto refundido, con arreglo a la reforma de la Ley 21/2007, de 11 de julio.

Al no haber procedido el Consorcio a efectuar dicha oferta motivada, ni haber instado la declaración de suficiencia de una consignación judicial en el plazo de tres meses desde la fecha en que se le reclamó la satisfacción de la indemnización, y no concurriendo ninguna causa que justifique esa falta, procede la imposición de un interés moratorio sobre la indemnización debida, igual al interés legal del dinero vigente en el momento del devengo, incrementado en el 50%.

El término inicial del cómputo de intereses es el de la fecha en que fue requerido de pago, conforme a lo establecido en el art. 20.6 de la Ley 50/1980, de Contrato de Seguro, momento que resulta aquí plenamente aplicable puesto que [RAZONES].

VIII.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda, a los efectos de lo dispuesto en el artículo 253.1 de la LEC, es la de [IMPORTE] euros, en aplicación de la regla 1.ª del artículo 251, según el cual, si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad.

De ahí procede la preceptividad de la representación por Procurador/a y la defensa por Abogado, conforme a los arts. 23 y 31 LEC.

IX.- COSTAS.

El artículo 394.1 de la Ley de Enjuiciamiento Civil establece que se impondrán al litigante cuyas pretensiones hayan sido totalmente rechazadas, por lo que deben serle impuestas al demandado condenado en la sentencia.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con los documentos y las copias que se acompañan, se sirva admitirlo, tener por comparecido y parte al/a la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS] en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por interpuesta demanda de juicio ordinario en reclamación de daños y perjuicios ocasionados con motivo de la circulación de vehículos de motor contra el Consorcio de Compensación de Seguros; y, seguido que sea el procedimiento por sus trámites, se dicte sentencia por la que se le condene al pago de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de indemnización de daños y perjuicios, más una indemnización por mora consistente en un interés anual igual al interés legal del dinero vigente en el momento del devengo, incrementado en un 50%, desde la fecha en que fue reclamado de pago y hasta su efectivo cumplimiento, imponiéndose al demandado las costas de este procedimiento.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA]	Firma del Procurador/a: [FIRMA]

(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta automatizada orientada al dato de dicho Registro, algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.
