---
name: demanda-cese-convivencia-pareja-hecho-segun-derecho-civ-0236
description: "Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco

> Formulario **CIV-0236** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que uno de los miembros de una pareja de hecho inscrita, ambos de vecindad civil vasca, reclama al otro la compensación económica derivada del cese de la convivencia (art. 6 de la Ley 2/2003, del Parlamento Vasco, reguladora de las parejas de hecho), cuando no existen pactos y la dedicación al hogar y a los hijos comunes ha generado una situación de desigualdad patrimonial que implica un enriquecimiento injusto.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-cese-convivencia-pareja-hecho-segun-derecho-civ-0236`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] LETRA O Nº DE LA CAUSA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 18 Ley 2/2003
- art. 6 Ley 2/2003
- art. 6.2 Ley 2/2003
- art. 85.1 LOPJ
- art. 49 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…UE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].»: el original numeraba como cuarto este hecho sobre el proceso de negociación previo; se ha reordenado la numeración al no figurar en el texto un hecho tercero separado de la fundamentación de la compensación.

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

[OPCIONAL — si ha lugar: en el segundo párrafo del hecho segundo deben hacerse constar, en cada caso, las circunstancias concretas por las que se solicita la pensión y/o la compensación; adaptar los datos del modelo (hijos comunes, dedicación al hogar, actividad del demandado) a los hechos reales.]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], según acredito [ELEGIR: por certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño / mediante designación apud acta ante el/la Letrado/a de la Administración de Justicia de [SEDE]], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a del Ilustre Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito formulo demanda de juicio ordinario en ejercicio de los derechos derivados de la extinción de la relación de pareja estable frente al demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio en [DOMICILIO], fundando mi pretensión en los siguientes

HECHOS

PRIMERO.– Mi representado/a y el/la demandado/a D./Dña. [NOMBRE Y APELLIDOS], ambos de vecindad civil vasca, han mantenido una relación de pareja de hecho desde el año [AÑO], lo cual acredito por certificado de la inscripción en el Registro de Parejas de Hecho que acompaño como documento número [Nº].

SEGUNDO.– En fecha [FECHA] y por motivos personales, se produjo la extinción de la convivencia por la causa [LETRA O Nº DE LA CAUSA] del artículo 18 de la Ley 2/2003, del Parlamento Vasco [OPCIONAL — si ha lugar: según acredito mediante [comunicación fehaciente recibida por mi mandante / certificación del Registro Civil de matrimonio del demandado con un tercero / OTRO DOCUMENTO]].

La presente reclamación se funda en lo dispuesto en el art. 6 de la Ley 2/2003, del Parlamento Vasco, al no existir pactos específicos entre la pareja y en aplicación asimismo del principio de enriquecimiento injusto, por cuanto la convivencia ha disminuido la capacidad de mi representado/a de obtener ingresos, puesto que se ha dedicado al cuidado de los hijos e hijas comunes [OPCIONAL — si ha lugar: en la actualidad mayores de edad], a la vez que ha trabajado para el hogar común y para los hijos comunes, por lo que tiene derecho a recibir una compensación económica al haberse generado por este motivo una situación de desigualdad entre el patrimonio de ambos que implique un enriquecimiento injusto. En efecto, la convivencia con el/la demandado/a ha impedido a mi representado/a acceder al mercado laboral, por cuanto se ha dedicado plenamente al cuidado de los hijos comunes, a la vez que le ha supuesto una situación de desigualdad patrimonial que ha implicado un enriquecimiento injusto a favor del/de la demandado/a por cuanto que se ha dedicado al hogar y a los hijos comunes, lo que implica, como efecto del cese, el derecho de mi representado/a a obtener una compensación económica conforme a lo que dispone el art. 6.2 de la Ley 2/2003, del Parlamento Vasco.

En efecto, mi mandante, durante todo el tiempo de la convivencia, se hizo cargo de todas las tareas del hogar familiar, propiedad del/de la demandado/a, cuidando a los hijos comunes [OPCIONAL — si ha lugar: en la actualidad mayores de edad], sin percibir ningún tipo de retribución. Por su parte, el/la demandado/a siguió desempeñando durante todo este tiempo su trabajo como [PROFESIÓN], percibiendo una retribución mensual de [IMPORTE] euros (a efectos acreditativos, y sin perjuicio de la prueba que se propondrá en el momento procesal oportuno, aporto los siguientes documentos: libro de familia, certificación de nacimiento de los hijos comunes, nóminas del demandado, certificación del servicio público de empleo del actor donde figura como demandante de empleo y donde constan las ofertas rechazadas, etc.).

Por tanto, atendiendo a los criterios establecidos en la Ley 2/2003, del Parlamento Vasco, y a la interpretación jurisprudencial, debe fijarse una compensación a favor de mi representado/a por la extinción de la convivencia por importe de [IMPORTE] euros, que debe satisfacer el/la demandado/a.

TERCERO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO EN CUMPLIMIENTO DEL REQUISITO DE PROCEDIBILIDAD QUE EXIGE LA LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº] [ESPECIFICAR EL DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

A estos hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Es competente este Tribunal, de conformidad con lo previsto en el art. 85.1 LOPJ y los arts. 49 y 52 de la LEC.

Procedimiento

Deben seguirse los trámites del proceso ordinario conforme al art. 249.2 de la LEC, al ser la cuantía reclamada superior a 15.000 euros.

Legitimación activa y pasiva

La ostentan ambas partes por su relación de pareja de hecho, conforme a la Ley 2/2003, del Parlamento Vasco.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Extinción y pensión y/o compensación económica

El art. 6.2 de la Ley 2/2003, del Parlamento Vasco, establece la cláusula general para el caso en que no se hubieren pactado expresamente los efectos de la extinción, disponiendo en su apartado 2.2 que los efectos del cese darán lugar a «una compensación económica a favor del miembro de la pareja que, sin retribución o con retribución insuficiente, haya trabajado para el hogar común o para el otro miembro, en el caso que se haya generado por este motivo una situación de desigualdad entre el patrimonio de ambos que implique un enriquecimiento injusto».

Motivación de la pensión y/o compensación

En este caso, nos hallamos ante un supuesto de extinción de la pareja de hecho donde uno de los convivientes, mi representado/a, se ha dedicado exclusivamente y sin ninguna retribución al hogar y al cuidado de los hijos comunes, sin posibilidad de acceder al mercado laboral, por lo que procede fijar la compensación que establece el apartado 2.2 del artículo 6 de la Ley 2/2003, del Parlamento Vasco.

Costas

Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte demandada.

Por cuanto antecede,

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de [NOMBRE Y APELLIDOS DEL DEMANDANTE], en virtud de [ELEGIR: la copia electrónica del poder notarial de representación (digitalizada) general para pleitos, cuya devolución intereso previa unión a los autos de copia testimoniada / designación apud acta], que se entiendan conmigo las sucesivas diligencias de proceso ordinario y que, en su día y tras los trámites legales, se dicte sentencia por la que se estime la demanda y se condene al demandado a indemnizar a mi representado/a en la cantidad de [IMPORTE] euros, más los intereses correspondientes, en concepto de extinción de la relación de pareja de hecho, todo ello con expresa imposición de costas a la parte demandada.

OTROSÍ DIGO: Que fijo la cuantía del proceso en la cantidad de [IMPORTE] euros.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes [OPCIONAL — si ha lugar: y por acompañado el documento justificativo del abono de la tasa].

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma de Procurador: [NOMBRE Y APELLIDOS]
