---
name: demanda-juicio-ordinario-impugna-particion-no-incluir-civ-0481
description: "Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario

> Formulario **CIV-0481** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario de coherederos para completar o adicionar la partición de una herencia ya aprobada judicialmente por no haberse incluido en el inventario determinados bienes, derechos o créditos (art. 1079 CC), con liquidación previa, en su caso, de la sociedad de gananciales no liquidada del causante, y subsidiaria designación de contador-partidor en ejecución de sentencia.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-ordinario-impugna-particion-no-incluir-civ-0481`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (52 veces)
- [ ] IMPORTE (28 veces)
- [ ] LOCALIDAD (17 veces)
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE (16 veces)
- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] FECHA (10 veces)
- [ ] DOMICILIO (9 veces)
- [ ] AÑO (8 veces)
- [ ] SEDE (7 veces)
- [ ] Nº (5 veces)
- [ ] Nº DE PROCEDIMIENTO (5 veces)
- [ ] BIEN OMITIDO (4 veces)
- [ ] BIENES ADJUDICADOS Y VALOR (3 veces)
- [ ] DENOMINACIÓN DEL NEGOCIO (3 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] ENTIDAD PERICIAL (3 veces)
- [ ] MES (3 veces)
- [ ] MUNICIPIO (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] Nº DE DOCUMENTOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] PARAJE (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] BIEN
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO LABORAL
- [ ] DÍA
- [ ] ENTIDAD VALORADORA
- [ ] NOMBRE Y APELLIDOS DE LA EXCÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PRIMER DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SEGUNDO DEMANDADO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE EXPEDIENTE
- [ ] Nº DE PARCELA
- [ ] Nº DE POLÍGONO
- [ ] Nº DE PROTOCOLO
- [ ] … y 1 datos más que aparecen una vez en el modelo

## Normas que cita el formulario

- art. 24.1 LEC
- art. 24.2 LEC
- art. 155.3 LEC
- art. 399.1 LEC
- art. 782 LEC
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 23 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 1079 CC
- art. 1396 CC
- art. 1392.1.º CC
- art. 1397.1.º CC
- art. 1404 CC
- art. 806 LEC
- art. 787.2 LEC
- art. 794.4 LEC
- art. 787.5 LEC
- art. 103.4.ª CC
- art. 810.5 LEC
- art. 784 LEC
- art. 394.1 LEC
- art. 335.2 LEC

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…l de la herencia cuyo inventario se debate supera con claridad los 15.000 euros.»: comprobar el umbral de cuantía vigente en los arts. 249 y 250 LEC.
- Junto a «… resolución en proceso de declaración plenario, juicio ordinario por la cuantía.»: el original citaba los arts. 792 y siguientes LEC para la división de herencia, mientras que en el hecho tercero cita los arts. 782 y siguientes; comprobar la numeración correcta.
- Junto a «…OCALIDAD], a [DÍA] de [MES] de [AÑO]. Firma del Abogado/a Firma del Procurador/a»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], y D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], representación que acredito mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— comparecencia electrónica a través de la sede judicial electrónica, con poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación acompaño certificación de dicho Registro como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme;
— comparecencia personal apud acta ante el Tribunal de Instancia de [LOCALIDAD], posteriormente inscrito el poder en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación acompaño certificación de dicho Registro como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme;
— escritura de poder otorgada a mi favor ante el Notario/Notaria D./Dña. [NOMBRE DEL NOTARIO], con notaría sita en [LOCALIDAD], inscrita en el Registro Electrónico de Apoderamientos Judiciales, lo cual justifico mediante certificación de dicho Registro, aportada como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme;

(Existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC. Todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales para su acreditación; basta, en principio, la consulta automatizada del Registro por el Letrado de la Administración de Justicia, y la certificación de la inscripción es la vía subsidiaria del art. 24.2 LEC.)

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], calle [DOMICILIO], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO contra D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER DEMANDADO], con domicilio en [DOMICILIO] (primero) [OPCIONAL: y [DOMICILIO LABORAL] (segundo, domicilio laboral)], con correo electrónico [CORREO ELECTRÓNICO] y número de teléfono móvil [TELÉFONO], y contra D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO DEMANDADO] [CIRCUNSTANCIAS DE IDENTIFICACIÓN Y LOCALIZACIÓN DEL CODEMANDADO EN LA FORMA INDICADA ANTERIORMENTE], en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los hechos y fundamentos de Derecho que se desarrollarán a continuación.

(El art. 155.3 LEC permite expresar varios domicilios del demandado: el que figure en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; aquel donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación inscrita en registro oficial, el del presidente, miembro o gestor de la junta correspondiente. Cuando se señalen varios, se indicará el orden a seguir para la notificación. El mismo precepto obliga al demandante a aportar cuantos datos sean de utilidad para localizar al demandado: NIF o NIE, teléfono, correo electrónico o similares.)

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.–

Mis representadas son hijas de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], quien falleció en [LOCALIDAD], el [FECHA].

Se acompañan certificados de defunción y nacimiento como documentos números [Nº DE DOCUMENTOS].

SEGUNDO.–

D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] otorgó último testamento abierto, ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], con el número [Nº DE PROTOCOLO] de su protocolo, en el que instituye herederos universales por terceras partes iguales a sus hijos, D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS].

Se acompaña copia del citado testamento como documento n.º [Nº DE DOCUMENTO].

TERCERO.–

D./Dña. [NOMBRE Y APELLIDOS] instó procedimiento de división de la herencia de su padre D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], tramitado conforme a lo dispuesto en los arts. 782 y siguientes LEC ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], bajo n.º [Nº DE PROCEDIMIENTO] / [AÑO].

En dicho procedimiento se sustanció en su día el trámite de formación del inventario, celebrándose la vista prevenida en la ley por haberse planteado controversia por mi mandante D./Dña. [NOMBRE Y APELLIDOS], personada en tales autos, acerca de los bienes que habían de integrarlo, y seguidamente fue dictada sentencia de fecha [FECHA], que devino firme, resolviendo la controversia en cuestión.

Con posterioridad se procedió al avalúo de los bienes inventariados y a la elaboración del cuaderno particional por el contador-partidor designado al efecto, el/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], cuyas operaciones divisorias no fueron objeto de oposición en plazo legal, por lo que el Letrado de la Administración de Justicia dictó decreto que aprobaba la partición.

Se acompaña testimonio de las actuaciones de referencia como documento n.º [Nº DE DOCUMENTO].

CUARTO.–

El cuaderno particional aprobado es del siguiente contenido:

A) Valor de los inmuebles sitos en [LOCALIDAD]:
a) Viviendas: [DIRECCIÓN] | [IMPORTE] euros (una línea por cada vivienda).
b) Solares: [DIRECCIÓN] | [IMPORTE] euros (una línea por cada solar).

B) Cálculo del importe de las obras de mejora y de ampliación (si las hubiera):
[BIEN] | Obras de mejora y ampliación: [IMPORTE] euros | Valor neto: [IMPORTE] euros.

C) Valor real del caudal relicto partible de los causantes de la herencia una vez deducido el importe de las obras de mejora y de ampliación:
a) Bienes inmuebles sitos en [LOCALIDAD]: [DIRECCIÓN] | [IMPORTE] euros (una línea por cada bien).
b) Fincas rústicas sitas en [LOCALIDAD], según la identificación y el valor dado por [ENTIDAD VALORADORA]: [IMPORTE] euros.
Valor total del caudal relicto: [IMPORTE] euros.

D) Importe de cada lote o hijuela de los herederos del causante: [IMPORTE] euros.

E) Adjudicaciones en pago a cada heredero para cubrir su haber:
— A D./Dña. [NOMBRE Y APELLIDOS]: [BIENES ADJUDICADOS Y VALOR]. Total adjudicado: [IMPORTE] euros. [Le sobran / Le faltan] [IMPORTE] euros, [que recibirá en metálico de D./Dña. [NOMBRE Y APELLIDOS] / que ha de abonar a D./Dña. [NOMBRE Y APELLIDOS]].
— A D./Dña. [NOMBRE Y APELLIDOS]: [BIENES ADJUDICADOS Y VALOR]. Total adjudicado: [IMPORTE] euros. [Le sobran / Le faltan] [IMPORTE] euros, [que recibirá en metálico de D./Dña. [NOMBRE Y APELLIDOS] / que ha de abonar a D./Dña. [NOMBRE Y APELLIDOS]].
— A D./Dña. [NOMBRE Y APELLIDOS]: [BIENES ADJUDICADOS Y VALOR]. Total adjudicado: [IMPORTE] euros. [Le sobran / Le faltan] [IMPORTE] euros, [que recibirá en metálico de D./Dña. [NOMBRE Y APELLIDOS] / que ha de abonar a D./Dña. [NOMBRE Y APELLIDOS]].

Se aporta, como documento n.º [Nº DE DOCUMENTO], la protocolización de tal cuaderno particional efectuada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el [FECHA], en ejecución del auto/decreto de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], de fecha [FECHA].

QUINTO.–

El causante D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] murió divorciado de D./Dña. [NOMBRE Y APELLIDOS DE LA EXCÓNYUGE], conforme a sentencia firme de la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], de fecha [FECHA], dictada en autos [Nº DE PROCEDIMIENTO] / [AÑO].

Según resulta de dicha resolución, cuya copia testimoniada se acompaña como documento n.º [Nº DE DOCUMENTO], a la esposa D./Dña. [NOMBRE Y APELLIDOS], además del uso y disfrute de la vivienda conyugal, de la calle [DOMICILIO], y la guarda y custodia de D./Dña. [NOMBRE Y APELLIDOS], entonces menor de edad, se le atribuyó, con el carácter de ganancial, la explotación del negocio denominado [DENOMINACIÓN DEL NEGOCIO], de la calle [DOMICILIO] de [LOCALIDAD], textualmente «hasta que se produzca la liquidación del régimen económico conyugal de sociedad de gananciales».

Desde el mes de [MES] de [AÑO] hasta el momento, Doña [NOMBRE Y APELLIDOS] jamás ha rendido cuentas del negocio en cuestión.

Acreditado, por tanto, que Doña [NOMBRE Y APELLIDOS] debía rendir cuentas, el cuaderno particional aprobado por el Letrado de la Administración de Justicia debía incluir el importe de los beneficios del negocio durante el período de tiempo transcurrido, y en atención al dictamen elaborado por [ENTIDAD PERICIAL], sobre la base de los datos obtenidos en las diligencias preliminares n.º [Nº DE PROCEDIMIENTO] / [AÑO] que adoptó ese Tribunal, sobre facturación derivada de las autoliquidaciones del IVA, supone una suma de [IMPORTE] euros. Así aparece evaluado en el documento n.º [Nº DE DOCUMENTO].

Esa comunidad de ganancias debe liquidarse con adjudicaciones por mitad, ingresando la de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] en su herencia.

SEXTO.–

Por otra parte, se ha averiguado, como consecuencia de las mismas indagaciones derivadas de las diligencias preliminares n.º [Nº DE PROCEDIMIENTO] / [AÑO] de ese Tribunal, que D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] había abonado, antes de morir, el mes de [MES] de [AÑO], las cuotas impagadas al Régimen Especial de Trabajadores Autónomos, en el expediente de apremio n.º [Nº DE EXPEDIENTE] y acumulados, a cuenta de D./Dña. [NOMBRE Y APELLIDOS], codemandado, por importe de [IMPORTE] euros, lo cual tampoco se tuvo en cuenta al inventariar como deuda de la herencia, excluyendo el crédito contra el heredero D./Dña. [NOMBRE Y APELLIDOS].

Se acompaña el certificado de la Unidad de Recaudación Ejecutiva de [LOCALIDAD] como documento n.º [Nº DE DOCUMENTO].

SÉPTIMO.–

En fin, está identificado un inmueble distinto de los ya incluidos en el cuaderno particional, no inmatriculado, que es el [DESCRIPCIÓN DEL INMUEBLE: p. ej. monte maderable] al lugar de [PARAJE], término municipal de [MUNICIPIO], que figura catastrado a nombre de D./Dña. [NOMBRE Y APELLIDOS], como parcela n.º [Nº DE PARCELA], del polígono [Nº DE POLÍGONO], del catastro de rústica del municipio de [MUNICIPIO], con arreglo a cuya pertenencia en pleno dominio a D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] resulta del documento n.º [Nº DE DOCUMENTO] y de la prueba de fuente personal que se articulará en su momento procesal idóneo.

La valoración de suelo y vuelo de dicho predio en cifra de [IMPORTE] euros se apoya en el dictamen pericial del Ingeniero Agrónomo D./Dña. [NOMBRE Y APELLIDOS], que se acompaña como documento n.º [Nº DE DOCUMENTO].

OCTAVO.–

Después de los reiterados esfuerzos sin éxito por alcanzar un acuerdo para integrar debidamente el inventario de los bienes relictos de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], mediante sendas cartas de fecha [FECHA], certificadas con acuse de recibo, mis representadas exigieron a D./Dña. [NOMBRE Y APELLIDOS] la liquidación de las ganancias del negocio familiar reseñado, orientando las cifras que tenían aquéllas dictaminadas, así como a D./Dña. [NOMBRE Y APELLIDOS] la nueva determinación de hijuelas en una partición que incluyera todos los bienes de la herencia.

No ha mediado respuesta alguna, por lo que no ha quedado más recurso que acudir a los tribunales, aportándose las cartas con sus acuses de recibo como documentos números [Nº DE DOCUMENTOS].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– PRESUPUESTOS SUBJETIVOS

I.1. JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia donde murió D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE].

I.2. CAPACIDAD Y LEGITIMACIÓN

Mis mandantes son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, así como lo son la demandada D./Dña. [NOMBRE Y APELLIDOS] y su hermano D./Dña. [NOMBRE Y APELLIDOS], por lo que todos tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa directa a mis mandantes, ya que son herederas testamentarias que fueron parte material en la división hereditaria, como hijas del causante, y están legitimados pasivamente de forma directa los codemandados: el otro heredero en la partición y la obligada a soportar la aportación a la masa hereditaria de los beneficios que se reclaman.

I.3. POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de representación de Procurador/a de los Tribunales con poder para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

II.– PRESUPUESTOS OBJETIVOS

II.1. PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, puesto que el valor real de la herencia cuyo inventario se debate supera con claridad los 15.000 euros.

II.2. CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de [IMPORTE] euros, que se obtienen, en aplicación de la regla 12.ª del art. 251 LEC, referida a pleitos sobre una herencia, adicionando al avalúo del cuaderno particional aprobado por el Letrado de la Administración de Justicia del Tribunal de Instancia n.º [Nº] de [SEDE] el valor de los bienes cuya inclusión en la masa patrimonial se pretende, a cuyo efecto se acompaña certificación de los expertos inmobiliarios de la firma [DENOMINACIÓN SOCIAL] (documento n.º [Nº DE DOCUMENTO]).

II.3. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

II.4. REQUISITOS FORMALES

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

III.– FONDO DEL ASUNTO

Las demandantes, mis patrocinadas, ejercitan la acción de complemento de la partición de la herencia de su padre D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], a la que se refiere el art. 1079 CCiv, conforme al que «la omisión de alguno o algunos objetos o valores de la herencia no da lugar a que se rescinda la partición por lesión, sino a que se complete o adicione con los objetos o valores omitidos».

Como presupuesto parcial de la misma se ejerce acción de liquidación de la comunidad postganancial habida entre D./Dña. [NOMBRE Y APELLIDOS] y el difunto D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE].

Al tenor del art. 1396 CCiv, disuelta la sociedad de gananciales, como ocurre con la disolución del matrimonio conforme al art. 1392.1.º CCiv por divorcio, se procederá a su liquidación, que comenzará por un inventario del activo y pasivo de la sociedad, debiéndose comprender en el activo los bienes gananciales existentes en el momento de la disolución (art. 1397.1.º CCiv).

Conforme al art. 1404 CCiv, hechas las deducciones en el caudal inventariado que prefijan los artículos anteriores, el remanente constituirá el haber de la sociedad de gananciales, que se dividirá por mitad entre los cónyuges o sus respectivos herederos.

PROCEDIBILIDAD

En efecto, para la liquidación de la comunidad conyugal de bienes se precave el procedimiento de los arts. 806 y siguientes LEC, y para la de la comunidad hereditaria, a través del trámite de división de herencia de los arts. 782 y siguientes LEC, pero nada puede excluir el directo examen y resolución en proceso de declaración plenario, juicio ordinario por la cuantía.

No se trata aquí de un nuevo incidente de inclusión y exclusión de bienes del inventario, sino de la posibilidad de incluir en la partición determinados bienes no incluidos inicialmente en el inventario, bien porque se ignoraba su existencia, bien porque se ignoraba su ganancialidad, para lo que resulta presupuesto previo liquidar una sociedad de gananciales, que de hecho parecía disuelta y liquidada, pero que de derecho supone un crédito frente a la excónyuge del causante, D./Dña. [NOMBRE Y APELLIDOS], demandada, a fin de que la misma se adjudique en propiedad el negocio familiar que viene explotando.

El art. 1079 CCiv concede amparo para incluir bienes omitidos, lo cual debe entenderse que igualmente procede con créditos, como el correlativo a la deuda del demandado D./Dña. [NOMBRE Y APELLIDOS] respecto de su padre D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE].

Tanto la manifestación de conformidad de los interesados con las operaciones divisorias practicadas como el transcurso del plazo de diez días sin hacer oposición supone que el Letrado de la Administración de Justicia dicte decreto que aprobará la partición y mandará protocolizarla (art. 787.2 LEC). Ello es lo que aconteció en el caso presente, a instancias de D./Dña. [NOMBRE Y APELLIDOS] en la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº].

Los bienes inventariables son los de contenido económico que formen parte del patrimonio del causante. La labor de averiguación de la titularidad no se impone al Letrado de la Administración de Justicia ni al tribunal, ni es factible imponérsela, siendo los herederos, parientes y demás interesados quienes pueden debatir, por su directo conocimiento, la inclusión o exclusión de bienes en la herencia. En el debate se puede llegar a un consenso, o bien puede suponer una efectiva controversia entre los presentes, previendo el art. 794.4 LEC un incidente de inclusión o exclusión de bienes, mediante la citación de los interesados a una vista, «continuando la tramitación con arreglo a lo previsto para el juicio verbal» (art. 794.4, párrafo 1.º, LEC).

Este incidente era praxis alegal, destinada a limitar una futura contienda sobre el contenido del inventario, y concentrar ésta, si se produjera, en las operaciones particionales del contador, despejando el tema de determinación del relicto antes de que el contador iniciara su tarea. Moderna jurisprudencia (desde la STS de 5 de julio de 1994, rec. 1772/1991) lo rechazó por anómalo, con doctrina sólida en el plano de los principios y de sujeción a la ley, pero escasamente práctica. En el supuesto de autos, con relación al [BIEN OMITIDO] en [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], personada en el procedimiento de división de herencia, ahora codemandante, instó su inclusión en el inventario, siéndole rechazada por sentencia de [FECHA]. Ahora bien, «la sentencia que se pronuncie sobre la inclusión o exclusión de bienes en el inventario dejará a salvo los derechos de terceros» (art. 794.4, párrafo 2.º, LEC), lo que debe interpretarse como ausencia de cosa juzgada y viable reproducción de la controversia por cualquier persona (aunque haya sido citada a la formación de inventario, e incluso haya sido parte, y pese a que cabalmente no sería «tercero») en un proceso declarativo ordinario.

De cualquiera de las maneras, el decreto que aprobó la partición en cuyo cuaderno particional se pretenden adiciones al inventario, para proceder a nuevas adjudicaciones, no es obstáculo a este proceso actual, con arreglo al art. 787.5 LEC.

NUEVA PARTICIÓN

La codemandada D./Dña. [NOMBRE Y APELLIDOS] estaba obligada a rendir cuentas de los rendimientos obtenidos por la explotación del negocio de [DENOMINACIÓN DEL NEGOCIO] durante los [NÚMERO] años transcurridos, toda vez que, como muy bien se expresa en la sentencia de divorcio que se presenta, al no haberse liquidado la sociedad de gananciales y, en consecuencia, no tener adjudicado en propiedad dicho negocio, tal y como prevé el art. 103.4.ª CCiv, que, aunque referido a las medidas provisionales, es plenamente aplicable también a las definitivas, nada eximía a la esposa de su obligación de rendir cuentas a D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], en tanto no se procediese a la liquidación del régimen económico matrimonial.

No es esta parte quien debe esforzarse en demostrar que el negocio ha producido beneficios, sino que la demandada está obligada a rendir cuenta detallada de la administración de dicho negocio y a acreditar cumplidamente el importe de los rendimientos del negocio, siendo así que, de las declaraciones de IVA correspondientes a los ejercicios a computar, obtenidas en las diligencias preliminares adoptadas por ese Tribunal, resultan unos ingresos que se evalúan en el dictamen pericial de [ENTIDAD PERICIAL].

No constando otros bienes o deudas de la comunidad conyugal, se pide la adjudicación del negocio, previa liquidación formal, a D./Dña. [NOMBRE Y APELLIDOS], restando como mitad del producto remanente a la herencia de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] los [IMPORTE] euros reclamados.

Así debe ingresar en el activo partible, como debe hacerlo el [BIEN OMITIDO] de [LOCALIDAD]. En este punto se cuenta con la prueba documental que no se tenía antes, que abona la certeza de la propiedad de dicho bien, por mucho que conste a nombre de [TITULAR CATASTRAL] en el Catastro. La finca está poseída por D./Dña. [NOMBRE Y APELLIDOS], sin que por ello deba demandarse para reivindicarla a persona alguna.

Y sumado su valor dictaminado por el Ingeniero Agrónomo [NOMBRE Y APELLIDOS] respecto del bien, y el de lo derivado de la deuda de D./Dña. [NOMBRE Y APELLIDOS], y agregando el crédito de la herencia por las cuotas de Seguridad Social abonadas a D./Dña. [NOMBRE Y APELLIDOS] al importe de su hijuela, la división, conservando las adjudicaciones de inmuebles del primitivo cuaderno particional aprobado judicialmente, supone que D./Dña. [NOMBRE Y APELLIDOS] deba por recibido en más, a la actora D./Dña. [NOMBRE Y APELLIDOS], la suma de [IMPORTE] euros, y a D./Dña. [NOMBRE Y APELLIDOS] la de [IMPORTE] euros.

Subsidiariamente, de la admisión de todas las operaciones divisorias que corrijan el cuaderno particional según las pretensiones liquidatorias de esta parte, puede sencillamente dejarse para ejecución de sentencia, nombrándose entonces un contador-partidor, conforme al art. 810.5 LEC, en relación con el art. 784 LEC.

IV.– COSTAS

Conforme al principio del vencimiento objetivo del art. 394.1 LEC, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo de la parte demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud, tener por interpuesta, en la representación que ostento, la presente demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], quienes deberán ser emplazados a fin de que puedan contestar, si a su derecho les conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que, estimando la acción de liquidación de comunidad matrimonial de bienes y complemento del cuaderno particional aprobado por decreto de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], de fecha [FECHA], en autos de división de herencia n.º [Nº DE PROCEDIMIENTO] / [AÑO], se declare:

— La liquidación de la sociedad de gananciales entre el difunto D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] y D./Dña. [NOMBRE Y APELLIDOS], con adjudicación a la esposa del negocio [DENOMINACIÓN DEL NEGOCIO] de la calle [DOMICILIO] en [LOCALIDAD], y al caudal relicto de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] la cantidad de [IMPORTE] euros.

— La inclusión en el inventario del cuaderno particional de la predicha cantidad de [IMPORTE] euros, y del [BIEN OMITIDO] en el sitio de [PARAJE], término municipal de [MUNICIPIO], por importe de [IMPORTE] euros.

— La imputación a la herencia partible del crédito frente al heredero demandado D./Dña. [NOMBRE Y APELLIDOS], por importe de [IMPORTE] euros.

— Dejando inalterable el resto del cuaderno particional aprobado.

Y condene a que D./Dña. [NOMBRE Y APELLIDOS] satisfaga a cada una de las demandantes la cantidad de [IMPORTE] euros, incrementada en los intereses al tipo legal del dinero desde el [FECHA].

Y condene a que, previa adjudicación por mitad a cada una de las demandantes del [BIEN OMITIDO], D./Dña. [NOMBRE Y APELLIDOS] satisfaga a D./Dña. [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, y a D./Dña. [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, incrementada en los intereses al tipo legal del dinero desde el [FECHA]; o subsidiariamente, y firme que sea la presente, se proceda en ejecución de sentencia a designar contador-partidor que, desde las bases de las previas declaraciones, reordene el cuaderno particional, confeccionando otro, con las compensaciones oportunas, para fijar las cuotas adjudicadas a los coherederos.

Todo ello con expresa imposición de las costas procesales a la parte demandada que se oponga.

OTROSÍ PRIMERO DIGO: que, siendo general para pleitos el poder que presenta el/la Procurador/a que suscribe, y precisándolo para otros usos,

OTROSÍ SEGUNDO DIGO: que se aportan los documentos números [Nº DE DOCUMENTOS] en condición de dictámenes periciales, el uno de evaluación de cuentas por [ENTIDAD PERICIAL], con sede en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO], y el otro de tasación de finca rústica del Ingeniero Agrónomo D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO], ambos con juramento o promesa del art. 335.2 LEC, articulándose en su momento procesal oportuno la solicitud de presencia de los peritos en el acto del juicio, si fuera menester.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por hechas las afirmaciones anteriores, se acuerde tener por presentado dictamen pericial y se proceda al desglose de la copia auténtica del poder para pleitos y su devolución a esta parte.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
