---
name: capitulaciones-matrimoniales-otorgadas-ante-notario-civ-0366
description: "Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio

> Formulario **CIV-0366** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:capitulaciones-matrimoniales-otorgadas-ante-notario-civ-0366`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NIF/DNI

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

Escritura de capitulaciones matrimoniales celebrada antes de contraer matrimonio, en la que se concreta el régimen matrimonial que les regirá a partir de ese momento, así como los derechos y obligaciones de cada uno de los contrayentes y futuros cónyuges.

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

D. [NOMBRE Y APELLIDOS], mayor de edad, soltero y de profesión [PROFESIÓN], vecino de esta ciudad y con domicilio en la calle [CALLE] núm. [NÚMERO], con D.N.I. número [NÚMERO]

Y Dña. [NOMBRE Y APELLIDOS], mayor de edad, soltera y de profesión [PROFESIÓN], vecina igualmente de esta ciudad y con domicilio en la calle [CALLE] núm [NÚMERO] con D.N.I. número [NIF/DNI]

Ambos intervienen en nombre, derecho y representación propia, recíprocamente se reconocen la suficiente capacidad legal para otorgar y llevar a efecto la escritura de Capitulaciones Matrimoniales que regirá el régimen económico del futuro matrimonio que tendrá lugar en [LOCALIDAD] a [FECHA] y que se basará en los siguientes:

PACTOS

PRIMERO.- El régimen económico matrimonial será el de separación de bienes y, en su consecuencia, cada uno de los esposos conservará el dominio, administración, uso y disfrute de los bienes que le pertenezcan en el momento de contraer matrimonio, así como de todos aquellos que adquiera en el futuro.

SEGUNDO.- Los bienes que cada cónyuge adquiera le pertenecerán en propiedad exclusiva y su titularidad vendrá determinada sin necesidad de otro requisito ni posibilidad de prueba en contrario, por lo que resulte de la escritura notarial, de la póliza de contratación de valores, del documento privado en defecto del público, de la cuenta corriente, depósito o libreta de ahorro o cualquier otra operación o documento bancario, y, en definitiva, del contrato o documento que, conforme a la legislación o a la práctica usual, confiera la titularidad con independencia de si se expresa o no la relación matrimonial. Si adquieren conjuntamente ambos cónyuges algún bien de su titularidad se determinará por lo convenido al tiempo de su adquisición, y a falta de ello, se entenderá que les pertenece por mitad y proindiviso.

TERCERO.- Cada cónyuge contribuirá a las cargas y obligaciones del matrimonio en proporción a sus correspondientes ingresos, haciendo suyos cada uno de ellos las rentas y productos de sus bienes destinándolos al fin que crean conveniente.

CUARTO.- En ningún caso los bienes de uno de los cónyuges responderán de las deudas, obligaciones y responsabilidades contraídas por el otro ni derivadas de cualquier actividad del mismo, aunque ésta redundare en beneficio de la familia, salvo el caso de que expresamente uno de ellos avale o afiance al otro.

QUINTO.- Contemplado el caso de una posible disolución del matrimonio, tendrán el carácter de privativos aquellos que cualquiera de los cónyuges hubiesen adquirido mediante cualquier clase de título bien sea lucrativo u oneroso; si hubiera bienes en que no pudiera demostrarse la atribución de la privaticidad a algún cónyuge en concreto o la procedencia de los mismos, se dividirán por mitad entre ellos.

SEXTO.- Cualquiera de los cónyuges por sí solo podrá pedir y obtener la inscripción o constancia de los presentes capítulos en los Registros Civil, Mercantil, de la Propiedad o en cualquier otro Registro, Oficina pública o privada, otorgando, a tal efecto, los documentos aclaratorios, descriptivos de bienes o complementarios que se necesiten sin precisar para todo ello la intervención del otro cónyuge.

Así lo otorgan los comparecientes, a quienes hago de palabra las advertencias y reservas legales.

Leída por mí el Notario a los otorgantes, la encuentran conforme y se ratifican en todo su contenido y firman conmigo

SING:

Firma de cónyuge	Firma de cónyuge

D./Dña. [NOMBRE Y APELLIDOS]

Notario

========================================================================
