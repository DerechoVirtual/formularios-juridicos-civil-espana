---
name: demanda-resolucion-arrendamiento-rustico-reclamacion-civ-0599
description: "Demanda de resolución de arrendamiento rústico y reclamación de daños por obras no autorizadas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de resolución de arrendamiento rústico y reclamación de daños por obras no autorizadas

> Formulario **CIV-0599** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio declarativo ordinario en ejercicio de las acciones acumuladas de resolución contractual de arrendamiento de finca rústica y acción de reclamación por daños ocasionados a la finca objeto del pleito.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de resolución de arrendamiento rústico y reclamación de daños por obras no autorizadas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de resolución de arrendamiento rústico y reclamación de daños por obras no autorizadas” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-resolucion-arrendamiento-rustico-reclamacion-civ-0599`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] FECHAS
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7 LEC
- art. 249.1.6 LEC
- art. 6.1.1 LEC
- art. 7 LEC
- art. 251 LEC
- art. 253 LEC
- art. 23 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 25.c Ley 49/2003
- art. 1556 CC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con asistencia del Letrado suscrito D./Dña. [NOMBRE Y APELLIDOS], que tiene abierto despacho en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que por medio del presente escrito deduzco demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

Se ejercitan en la presente demanda acciones acumuladas de resolución contractual de arrendamiento de finca rústica y acción de reclamación por daños ocasionados a la finca objeto de este pleito.

La demanda se basa en los siguientes

HECHOS

PRIMERO.- Mi representado es propietario de la finca inscrita al n.º [NÚMERO], folio [FOLIO] del Libro [LIBRO] del Registro de la Propiedad n.º [NÚMERO] de

Mi mandante arrendó la mencionada finca al demandado, por contrato celebrado el día [FECHA], expresándose en el contrato que la finalidad del arriendo está determinada en la explotación agrícola de trigo.

Se acompaña dicho contrato como documento nº [Nº DE DOCUMENTO], en el que se estipuló una renta anual de [IMPORTE] euros.

SEGUNDO.- El demandado ha cultivado durante el primer año de duración del contrato en las condiciones estipuladas, dedicando la finca a la explotación agrícola de trigo, pero a partir del segundo año abadonó la explotación, dejando de cultivar la finca, y en el tercero en curso, con fecha [FECHA] ha llegado a conocimiento de mi representado por conducto del Presidente de la Federación regional de Hípica de [LOCALIDAD] que en la meritada finca se están realizando obras para subarrendar la finca a sociedades deportivas a fin de que utilicen el terreno para entrenamientos.

Se acompaña como documento nº [Nº DE DOCUMENTO] copia de la carta dirigida al Club [NOMBRE DE LA PARTE] donde se ofrece la finca libre de cultivos para su uso deportivo a cambio de un precio.

TERCERO.- Ante tal situación, mi mandante se personó en la finca con un Ingeniero Agrónomo, constatando que la misma se encuentra baldía, y que se han causado graves daños a la parte más apta para las tareas agrícolas.

Se acompañan cuatro fotografías en las que se aprecia el estado original de la finca y su estado actualmente (documentos nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO]) e informe pericial del Ingeniero Agrónomo Sr./a. D./Dña. [NOMBRE Y APELLIDOS], expresivo de los daños causados en la finca de mi representado (documento nº [Nº DE DOCUMENTO]).

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

I.1.La Jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

I.2. La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC.

I.3. La competencia territorial asimismo corresponde, conforme al art. 52.1.7º LEC, por cuanto el Tribunal es el del partido del lugar en que está sita la finca.

II PROCEDIMIENTO

La demanda deberá sustanciarse por las normas del juicio ordinario del Título II del Libro II LEC, a tenor de lo expresamente prevenido en el art. 249.1.6º LEC, al tener por objeto pretensiones relativas a contrato de arrendamiento de finca rústica, sin que opere la exclusión material de la acción de desahucio o de mera reclamación de cantidad.

III.- CAPACIDAD

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN

Corresponde la legitimación activa a mi mandante por tener la posesión mediata de la finca a título de dueño y por haber celebrado el contrato de arrendamiento con el demandado, por lo que es titular del derecho a resolver el contrato por incumplimiento, obteniendo la recuperación de la posesión inmediata, y a ser indemnizado por los daños causados en la finca.

La legitimación pasiva corresponde al demandado como arrendatario poseedor y causante de los daños.

V.- CUANTÍA

Se hace constar que la cuantía de la demanda es de [IMPORTE] euros ([IMPORTE EN CIFRA] €), resultado de sumar, al acumularse (art. 252.2ª) la cuantía por el importe de una anualidad de renta, conforme a la Regla 9ª del art. 251 LEC por la acción resolutoria del contrato de arrendamiento de la finca, y conforme a la Regla 1ª del art. 251 LEC por la acción de reclamación de daños ocasionados a la misma, lo que se deja expreso por imperio del art. 253 LEC.

VI.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC, se formula esta demanda por medio de Procurador de los Tribunales con poder general para pleitos y especial para percibir cantidades, con la dirección y firma de Letrado ejerciente colegiado.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4º y art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- ASUNTO DE FONDO

Se funda esta demanda en el art. 25.c) de la Ley 49/2003, de 26 de noviembre, de Arrendamientos Rústicos, en cuanto es evidente que el demandado ha incurrido en causa de resolución contractual: no explotar la finca, destinándola, en todo o parte, a fines o aprovechamientos distintos de los previstos contractualmente, sin que ello venga impuesto por ningún programa o plan cuyo cumplimiento sea necesario para la percepción de ayudas o compensaciones en aplicación de ninguna normativa estatal, autonómica o comunitaria aplicable, que se corresponda con el objeto previsto para el arrendamiento rústico de LAR (art. 1.1).

Se ejercita acumuladamente acción de reclamación de cantidad por los daños ocasionados a la finca objeto del contrato a causa de la realización de obras no autorizadas, que deben ser indemnizados por el demandado por haberlos causado voluntariamente y con una finalidad totalmente ajena a lo convenido por las partes en el contrato de arrendamiento (arts. 1556 y concordantes del CC).

IX.- COSTAS

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitirlo a trámite, me tenga por comparecido y parte demandante en la representación que acredito, y por formulada la demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS] acordando conferir traslado de la misma a dicho demandado, emplazándole para que comparezca y la conteste, y seguido el juicio por sus trámites, celebrada audiencia previa y juicio, se dicte sentencia por la que estimando íntegramente la demanda, se declare la resolución del contrato de arrendamiento de la finca descrita, condenando al demandado a estar y pasar por dicha resolución, desalojando la misma en el plazo legal, dejándola vacua, libre y expedita y a disposición de mi mandante; y le condene asimismo a indemnizar a mi mandante en la cantidad deeuros (€ [IMPORTE EN CIFRA]) por los daños causados en la finca, con expresa imposición de las costas al demandado.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
