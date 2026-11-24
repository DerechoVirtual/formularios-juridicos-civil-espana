---
name: contrato-ejecucion-obra-aportacion-materiales-civ-0709
description: "Contrato de ejecución de obra con aportación de materiales por el contratista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ejecución de obra con aportación de materiales por el contratista

> Formulario **CIV-0709** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ejecución de obra con aportación de materiales por el contratista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ejecución de obra con aportación de materiales por el contratista” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-ejecucion-obra-aportacion-materiales-civ-0709`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] PLAZO (5 veces)
- [ ] CALLE (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LAS OBRAS
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] NÚMERO DE LA CALLE
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 158 Real Decreto Legislativo 1/2020

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

En [LOCALIDAD], a [DÍA] de [MES] 20

Comparecen:

De una parte [NOMBRE Y APELLIDOS], como COMITENTE (persona física o jurídica)

(Persona física: D/D.ª [NOMBRE Y APELLIDOS] mayor de edad, casado, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. [DNI/NIE])

(Persona jurídica: constituída en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D. e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm. [NÚMERO DE LA CALLE] y con CIF núm. representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. cuyas facultades derivan del poder otorgando por el notario D. [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna)

De otra parte, como CONTRATISTA (persona física o jurídica)

Ambas partes se reconocen con carácter mutuo y tienen capacidad legal suficiente para otorgar el presente contrato de ejecución de obra con aportación de materiales.

Convienen:

1. Disposiciones generales: a) El COMITENTE [DENOMINACIÓN SOCIAL] (detallar denominación) es propietario de una empresa dedicada a [ACTIVIDAD] (detallar actividad). La citada empresa se encuentra ubicada en un inmueble situado en [DIRECCIÓN] (detallar municipio, provincia, calle y número). La finca está inscrita en el Registro de la propiedad de [LOCALIDAD] (detallar Registro), número [NÚMERO] (detallar número) y está libre de cargas. b) El COMITENTE quiere instalar en el inmueble citado la siguiente maquinaria [DESCRIPCIÓN DEL BIEN] (detallar maquinaria), para lo cual es necesaria la ejecución de las siguientes obras [DESCRIPCIÓN DE LAS OBRAS] (detallar obras). Las obras se realizarán según consta en el proyecto realizado por el técnico [NOMBRE Y APELLIDOS] (detallar nombre y apellidos), visado por el Colegio de [LOCALIDAD] (especificar colegio profesional y provincia), con fecha de [FECHA] (especificar fecha), firmado por ambas partes. El proyecto técnico aparece recogido en el anexo correspondiente. c) El CONTRATISTA es una entidad dedicada a la instalación y montaje de [ACTIVIDAD] (detallar actividad), y está en posesión de todos los permisos y licencias que acreditan poder realizar la obra proyectada. Se incluyen las altas fiscales y laborales necesarias. d) El CONTRATISTA a través del presente contrato se obliga a la realización de la instalación pactada, con todas las obras necesarias para ello, suministrando la maquinaria a instalar y los materiales necesarios para ello.

2. Objeto. En virtud de este contrato, el CONTRATISTA se compromete a realizar en el inmueble propiedad del COMITENTE la instalación y montaje de la maquinaria detallada en las disposiciones generales, así como las obras necesarias para ello, y que se detallan en el proyecto técnico recogido en el anexo. Para la realización del objeto de este contrato se exigirá la diligencia prevista según los usos profesionales del sector.

3. Precio. El precio final de la ejecución de la obra asciende a la cantidad de [IMPORTE] (detallar en número y letra) euros. En el precio se encuentra incluida la maquinaria que el CONTRATISTA procederá a instalar, así como su transporte y cualquier otro gasto adicional que pueda generarse.

El pago del precio se realizará mediante ingreso en la c/c número [NÚMERO] (detallar), en el Banco [ENTIDAD BANCARIA] (detallar), sucursal [DIRECCIÓN] (detallar número de oficina o, en su caso, lugar), o mediante cheque bancario conformado, a nombre del CONTRATISTA.

El precio se distribuirá del modo siguiente: un porcentaje [PORCENTAJE] (detallar) se abonará a la firma de este contrato que tiene valor de carta de pago por dicha cantidad. Un porcentaje [PORCENTAJE] (detallar) al inicio de las obras. El porcentaje que resta [PORCENTAJE] (detallar) en el plazo máximo de [PLAZO] (detallar días), a partir de la finalización de la obra.

4. Plazo. El CONTRATISTA se obliga a finalizar la obra proyectada y dejar la instalación en perfecto funcionamiento en el plazo de [PLAZO] (detallar) meses a partir del inicio de la obra. Dicho inicio tendrá lugar en el plazo máximo de [PLAZO] (detallar) días, desde la firma del presente contrato.

5. Suministro de materiales. El CONTRATISTA queda obligado a suministrar toda la maquinaria y materiales que resulten necesarios para la ejecución de la obra objeto de este contrato, incluyendo ejecución y obras adicionales. Los materiales a suministrar coincidirán con las calidades que se detallan en la memoria incorporada al anexo correspondiente. Será de cuenta del CONTRATISTA su adquisición, entendiéndose el precio incluido en el precio total a abonar por el COMITENTE y contemplado en el apartado 3 de este contrato.

6. Mano de obra. El CONTRATISTA queda igualmente obligado a aportar toda la mano de obra que sea necesaria para la ejecución de la obra. La mano de obra deberá estar al corriente de todas las obligaciones legales predispuestas.

7. Subcontratas. El presente contrato faculta al CONTRATISTA para subcontratar la ejecución de partes determinadas de la obra pactada a terceros. El CONTRATISTA responderá por el trabajo realizado y asume la obligación de pago del precio pactado.

8. Entrega de la obra. En el momento de la finalización de la obra proyectada, el COMITENTE procederá una recepción de carácter provisional en presencia de las dos partes de este contrato, así como del autor del proyecto técnico. Se levantará el acta correspondiente. Tras el transcurso de [PLAZO] (detallar) meses, se procederá a la recepción definitiva de la obra. El tiempo transcurrido servirá de plazo de garantía de la correcta ejecución de la obra.

9. Cláusula penal. Para el caso de que llegada la fecha prevista para la entrega de la obra ésta no se encuentra finalizada, además de la posibilidad de resolver el contrato y solicitar la correspondiente indemnización por daños y perjuicios, el CONTRATISTA queda obligado por este contrato a abonar al COMITENTE la cantidad de [IMPORTE] (detallar en letra y número) euros, en concepto de cláusula penal por cada día de retraso en la ejecución, a partir del primer mes, del tiempo pactado para la recepción de la obra. Se excepcionan los supuestos en los que el retraso sea debido a fuerza mayor o a una circunstancia que no pueda ser imputable al CONTRATISTA.

10. Terminación y resolución del contrato. Se consideran causas de terminación y resolución de este contrato: a) la terminación normal del contrato bien por haberse procedido a la ejecución total de la obra pactada; por haber concluido el tiempo pactado, o por el acuerdo mutuo de las partes; b) por incumplimiento de cualquiera de las cláusulas del contrato sin subsanación por parte del incumplidor en el periodo de [PLAZO] (detallar) días desde que le fuera notificado por escrito dicho incumplimiento.

La declaración de concurso de cualquiera de las partes obliga a solicitar a la parte afectada la resolución del contrato de acuerdo con el artículo 158 del Real Decreto Legislativo 1/2020, de 5 de mayo, Texto Refundido de la Ley Concursal.

La resolución de este contrato, no excluye cualquier otra reparación legal o judicial que cualquiera de las partes considere oportuno obtener.

11. Gastos e impuestos. Todos los gastos, impuestos, contribuciones o tases, tanto presentes como futuros, se abonarán por ambas partes, conforme a la Ley.

12. Elevación a documento público. Cualquiera de las partes puede solicitar la elevación a documento público del presente contrato, debiendo el solicitante hacer frente a los gastos derivados de la elevación.

13. Arbitraje. Las partes se comprometen a acudir a un arbitraje de Derecho privado, conforme a la legislación vigente, para dirimir todos los posibles conflictos que entre ellas pudiera surgir, en particular, como consecuencia de la interpretación o incumplimiento del presente contrato. Las partes renuncian expresamente al ejercicio de cualesquier acción ante tribunales.

EL COMITENTE [NOMBRE Y APELLIDOS] EL CONTRATISTA
