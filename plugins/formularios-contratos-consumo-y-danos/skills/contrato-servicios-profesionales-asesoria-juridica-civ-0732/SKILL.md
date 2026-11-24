---
name: contrato-servicios-profesionales-asesoria-juridica-civ-0732
description: "Contrato de servicios profesionales de asesoría jurídica o de abogado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios profesionales de asesoría jurídica o de abogado

> Formulario **CIV-0732** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de arrendamiento de servicios de asesoría jurídica y/o despacho de abogados.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios profesionales de asesoría jurídica o de abogado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios profesionales de asesoría jurídica o de abogado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-servicios-profesionales-asesoria-juridica-civ-0732`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] NIF
- [ ] SUCURSAL
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 1262 Código Civil

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

Modelo de contrato de arrendamiento de servicios de asesoría jurídica y/o despacho de abogados.

Notas al pie del formulario original:
(1) Téngase en cuenta que, según el art. 1583 CC, el contrato puede celebrarse sin tiempo fijo.

(2) Téngase en cuenta la posibilidad de combinar cláusulas híbridas arbitraje/jurisdicción, como las de mediación o las de sumisión a determinada jurisdicción, bien permitiendo la elección a una de las partes, o a la demandante, o delimitando qué tipo de contiendas irían a una u otra vía, como señala la Audiencia Provincial de Madrid, Sección 28ª, Auto 147/2013 de 18 Oct. 2013, Rec. 66/2013, ref. La Ley 172387/2013).


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

En [LUGAR], a [FECHA].

REUNIDOS:

De una parte, Don/Doña [NOMBRE Y APELLIDOS], en nombre y representación de la entidad mercantil [DENOMINACIÓN SOCIAL] con domicilio social en [LOCALIDAD], provista de NIF [NIF], constituida mediante escritura pública otorgada ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], inscrita en el Registro Mercantil de [LOCALIDAD] en el [DATOS REGISTRALES]. Acredita dicha representación mediante la presentación de la escritura de poder otorgada ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] el día [FECHA], con número [NÚMERO] de los de su protocolo. En lo sucesivo EL DESPACHO.

De otra parte, Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, provisto de DNI núm. [DNI/NIE], con domicilio a efecto de notificaciones en [DOMICILIO] quien interviene en su propio nombre y derecho, en lo sucesivo EL/LA CLIENTE.

MANIFIESTAN

I.- Que EL DESPACHO es una entidad dedicada al asesoramiento jurídico así como a la defensa de los intereses de sus clientes ante Tribunales, arbitrajes, etc.

II.- Que EL/LA CLIENTE está interesado/a en contratar los servicios del DESPACHO, y éste a prestarlos a favor del CLIENTE o de la persona física o jurídica que éste designe.

En su virtud han decidido celebrar el presente CONTRATO DE ARRENDAMIENTO DE SERVICIOS, que se sujetará a las siguientes

CLÁUSULAS

Primera.- Objeto del contrato

EL/LA CLIENTE contrata los servicios jurídicos ofrecidos por EL DESPACHO, quien acepta prestarlos, y consistentes en las siguientes actividades:

a) Asesoramiento sobre [DESCRIBIR].
b) Información sobre la evolución del asunto encomendado, con informes a entregar por escrito con periodicidad mensual.
c) En su caso, acuerdo con las partes implicadas en el asunto encomendado.
d) En caso de que no sea posible llegar a un acuerdo, emprender cuantas actuaciones judiciales sean precisas, encargándose el DESPACHO de su dirección letrada. Todos los procedimientos judiciales objeto de este contrato serán tramitados por profesionales del derecho, pudiendo EL CLIENTE comprobarlo personalmente en los Colegios Profesionales respectivos.

Segunda.- Precio

Mediante este contrato de arrendamiento de servicios jurídicos, el CLIENTE se compromete a abonar previamente la cantidad determinada en concepto PROVISIÓN DE FONDOS de [IMPORTE] euros.

El coste total previsto para la prestación de servicios pactada se estima, según sea posible una solución extrajudicial o no, en:

a) [IMPORTE] euros para el caso de que dicha solución extrajudicial sea posible.
b) [IMPORTE] euros para el caso de que sea necesario emprender acciones judiciales, en cuyo caso el 50 % de esta cuantía deberá quedar abonada al momento de interponerse la oportuna demanda, y el resto en el momento de obtener la sentencia. En caso de necesidad de recursos posteriores a la sentencia, éstos se minutarán conforme a las normas mínimas establecidas al efecto por el Iltre. Colegio de Abogados de [COLEGIO].

Tercera.- Forma de pago

EL CLIENTE abonará los honorarios mediante tarjeta de crédito o débito, domiciliación o transferencia bancaria a la cuenta nº [NÚMERO] entidad [ENTIDAD BANCARIA] oficina [SUCURSAL], de la que es titular EL DESPACHO.

El uso fraudulento de tarjetas de créditos, o la denegación de la operación de cobro por cualquier causa, dará derecho al DESPACHO a rescindir el servicio jurídico contratado, sin perjuicio de las responsabilidades civiles y penales correspondientes.

Cuarta.- Duración

La vigencia del presente contrato se prorrogará hasta [FECHA].

Quinta.- Desistimiento por EL CLIENTE

Tras la contratación y pago del Servicio Jurídico, el Cliente podrá cancelar y desistir de dicha contratación en un plazo de 7 días hábiles, con o sin causa justificada, sin ningún tipo de penalización, siempre y cuando el servicio no se hubiese prestado ya por EL DESPACHO.

Para formular este desistimiento EL CLIENTE deberá comunicarlo expresamente al DESPACHO por cualquier medio que permita la constancia de su recepción.

Sexta.- Suministro de datos y secreto profesional

EL CLIENTE facilitará al DESPACHO cuantos datos, informes o material estime éste necesario para poder llevar a cabo la prestación del servicio para el que se le contrata. EL CLIENTE será responsable de la veracidad y calidad de los datos suministrados así como de las consecuencias que la falta de dicha veracidad pueda acarrear.

EL DESPACHO se compromete a prestar sus servicios bajo su deber de confidencialidad respecto de los datos personales suministrados por EL CLIENTE para la resolución de su caso. Por ello no serán difundidos ni compartidos, salvo que medie consentimiento expreso del cliente.

Séptima.- Protección de datos personales

El CLIENTE da su permiso para que sus datos sean tratados y, además, utilizados para enviar comunicaciones comerciales de promoción y publicidad de los servicios y productos ofrecidos por EL DESPACHO. El DESPACHO pone a disposición de sus clientes la dirección de correo electrónico y el teléfono [TELÉFONO].

El DESPACHO declara que cumple la normativa vigente respecto a la protección de datos, en particular el Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la Protección de las Personas Físicas en lo que respecta al Tratamiento de Datos Personales y a la Libre Circulación de éstos.

Octava.- Legislación aplicable y jurisdicción

Las partes reconocen que la legislación aplicable al presente contrato, y a todas las relaciones jurídicas dimanantes del mismo, será la española, por expresa aplicación de lo dispuesto en el art.1262 del Código Civil.

Las partes acuerdan someterse para la resolución de cualquier controversia, conflicto o reclamación derivada del presente contrato, a los Tribunales de [LOCALIDAD], por ser éste el lugar de celebración del contrato, con renuncia expresa a cualquier otro fuero que pudiera corresponderles.

EL DESPACHO

EL CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
