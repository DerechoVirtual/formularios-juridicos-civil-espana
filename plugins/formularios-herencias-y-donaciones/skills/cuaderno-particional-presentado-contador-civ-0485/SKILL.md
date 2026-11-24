---
name: cuaderno-particional-presentado-contador-civ-0485
description: "Cuaderno particional presentado por el contador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cuaderno particional presentado por el contador

> Formulario **CIV-0485** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Cuaderno particional presentado por el contador designado por la Junta de interesados en la herencia del causante.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cuaderno particional presentado por el contador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cuaderno particional presentado por el contador” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:cuaderno-particional-presentado-contador-civ-0485`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (15 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (4 veces)
- [ ] OTROS DATOS (4 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DESCRIPCIÓN DE LOS BIENES
- [ ] ESTADO CIVIL
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS DE LOS HEREDEROS
- [ ] Nº
- [ ] Nº DE PLIEGOS
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 786.1 LEC

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

- Junto a «… que conoce la sección civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Operaciones divisorias del caudal relicto de D./Doña [NOMBRE Y APELLIDOS], practicadas por el contador D./Dña. [NOMBRE Y APELLIDOS], Letrado en ejercicio, designado por la Junta de interesados en la herencia celebrada el [FECHA], en autos de juicio de División de Herencia nº [NÚMERO] / de que conoce la sección civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [LOCALIDAD] y su partido, para lo que se ha tenido en cuenta las instrucciones especiales del testamento del difunto, y los pactos a que han llegado lo interesados, siempre sin perjudicar las legítimas de los herederos forzosos, la ley aplicable (Código Civil o norma del Derecho foral o especial que sea), partiendo del inventario formado judicialmente, y lo demás que resulta de los autos, papeles y documentos puestos a nuestra disposición y relacionados con los bienes, atendido el criterio legal de evitar la indivisión, al tiempo que la excesiva división de las fincas (art. 786.1 ‘in fine’ LEC).

BASES O SUPUESTOS

Primero

Sobre la muerte y disposición testamentaria del causante

D./Doña [NOMBRE Y APELLIDOS] falleció el día [FECHA], en estado de [ESTADO CIVIL], y dejó los herederos [NOMBRE Y APELLIDOS DE LOS HEREDEROS]

El citado causante otorgó testamento el día [FECHA] ante el Notario de [LOCALIDAD], con nº [NÚMERO] de su protocolo general corriente, y éste es el testamento vigente según el certificado del Registro Central de Actos de Última Voluntad.

Segundo

Sobre la dote y bienes parafernales de la viuda Don/Dña. [NOMBRE Y APELLIDOS]

Tercero

Sobre los bienes propios del causante [ÓRGANO]

Cuarto

Sobre las deudas de la sociedad de gananciales (o comunidad de bienes conyugal que sea)

Quinto

Liquidación de la sociedad de gananciales [OTROS DATOS]

(Se deducirá del valor de los gananciales la dote y parafernales, las deudas de la sociedad y los bienes privativos del marido, obteniendo el líquido cuya mitad se agrega a los bienes de la base tercera para formar el caudal partible)

Sexto

Bienes colacionables [DESCRIPCIÓN DE LOS BIENES]

Séptimo

Legados y bajas del tercio de libre disposición [OTROS DATOS]

Octavo

Luto y usufructo del viudo/a Don/Dña. [NOMBRE Y APELLIDOS]

Noveno

Mejoras y legítimas de los hijos [OTROS DATOS]

Décimo

Liquidación y división del caudal hereditario [OTROS DATOS]

(Caudal constituido por los bienes de la base tercera, la mitad del líquido de gananciales, con las bajas que procedan, del que se especificará la porción que corresponde a cada heredero)

LIQUIDACIONES

CUERPO GENERAL DE BIENES

SUMA EN TOTAL-EUROS

-LIQUIDACIÓN DE LA SOCIEDAD DE GANANCIALES-

-Constituye el capital de esta sociedad el importe antes establecido en el Cuerpo General de Bienes, ascendente a [IMPORTE] euros
-BAJAS:

Dote (base segunda)- euros

Parafernales (ídem) () euros

Deudas de la sociedad (base cuarta)-- euros

Bienes privativos (base tercera)-- euros

Total- euros

-Restan como haber líquido de la sociedad de gananciales, el importe de [IMPORTE] euros
-Cuya cantidad, dividida por mitad entre la viuda y los herederos del cónyuge difunto, corresponde a cada parte euros

-LIQUIDACIÓN DEL CAUDAL HEREDITARIO-

1.- Bienes aportados al matrimonio por el causante [IMPORTE] euros

2.- Su mitad de gananciales, importa [IMPORTE] euros

TOTAL DEL CAUDAL HEREDITARIO [IMPORTE] euros

(Si existen legitimarios y legados y mejoras se hará liquidación separada y a continuación, del tercio de libre disposición, deducidos de él los legados, gastos de entierro y funeral y última enfermedad, y de las mejoras, con lo que se llegará al haber de cada heredero)

-ADJUDICACIONES-

1.- HABER DEL VIUDO/A DON/DOÑA.

Ha de haber esta interesada:

-Para pago de las deudas de la sociedad de gananciales (base cuarta) [IMPORTE] euros
-Para la dote aportada (base segunda) [IMPORTE] euros
-Para bienes parafernales adquiridos durante el matrimonio y aportados al mismo (base segunda) euros
-Para su mitad de gananciales [IMPORTE] euros
-Para luto (base octava) [IMPORTE] euros
-Por cuota del caudal en usufructo (base octava) [IMPORTE] euros

Total Haber de Don/Dña. euros

ADJUDICACION Y PAGO:

-Para el pago de deuda de la sociedad, el metálico inventariado euros
-En pleno dominio, los siguientes bienes [IMPORTE] euros
-En usufructo, [IMPORTE] euros

Suma todo lo adjudicado, la cantidad de [IMPORTE] euros

Que es igual al Haber asignado.

2.- HABER DEL HEREDERO.

Ha de haber este interesado:

(Se continúa como en la adjudicación anterior)

COMPROBACIÓN

Suman los bienes adjudicados a [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros

Suman los bienes adjudicados a [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros

Cuya suma total es igual a la del valor del cuerpo general de bienes inventariado.

DECLARACIONES FINALES

1.- Si apareciesen otros bienes y créditos pertenecientes a esta herencia, se distribuirán entre los interesados en la misma proporción en que se ha dividido el caudal hereditario; en igual proporción pagarán también cualquier deuda, obligación o gravamen que pudiera resultar a posteriori y que no se ha tenido en cuenta por ignorarse su existencia.

2.- Los interesados quedan recíprocamente obligados a la evicción y saneamiento de los bienes que les han sido adjudicados.

3.- Se pagarán proporcionalmente a lo que reciban por los interesados los gastos del juicio de división de la herencia hasta su aprobación judicial, hechos en interés común, y serán de cuenta particular de cada uno los hechos en su interés respectivo.

4.- Se entregarán a cada uno de los interesados los títulos de propiedad de las fincas que se les adjudican, pero dado que los hay que son comunes, éstos quedarán en poder del heredero [NOMBRE Y APELLIDOS] sin perjuicio de que facilite a los demás interesados copias fehacientes a costa del caudal hereditario.

Con lo cual doy por terminadas las presentes operaciones divisorias practicadas con arreglo a nuestro leal saber y entender, y salvo error u omisión en las operaciones aritméticas que contiene, en [Nº DE PLIEGOS] pliegos, rubricados en todas sus páginas,

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Contador/a

========================================================================
