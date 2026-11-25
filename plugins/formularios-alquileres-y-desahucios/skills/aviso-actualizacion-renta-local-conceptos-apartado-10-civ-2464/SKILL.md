---
name: aviso-actualizacion-renta-local-conceptos-apartado-10-civ-2464
description: "Aviso de actualización de renta del local y conceptos del apartado 10 de la DT segunda LAU. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Aviso de actualización de renta del local y conceptos del apartado 10 de la DT segunda LAU

> Formulario **CIV-2464** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Aviso de actualización de renta del local y conceptos del apartado 10 de la DT segunda LAU» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Aviso de actualización de renta del local y conceptos del apartado 10 de la DT segunda LAU” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:aviso-actualizacion-renta-local-conceptos-apartado-10-civ-2464`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] Nº
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Solo aplicable a locales de negocio anteriores al 9-5-1985 que subsistan: los de arrendatario persona jurídica sujetos al apartado 4 de la DT 3.ª ya se extinguieron; en la práctica quedan los de persona física o cónyuge subrogado (DT 3.ª.3) o con plazo pactado aún vigente (DT 3.ª.5).
- Junto a «…sica o cónyuge subrogado (DT 3.ª.3) o con plazo pactado aún vigente (DT 3.ª.5).]»: Las tablas de porcentajes se cuentan por periodos anuales desde el 1-1-1995: comprobar el porcentaje exigible al practicar hoy la actualización.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Complementariamente a lo indicado en el Formulario "Notificación de actualización de renta", el presente tiene por objeto la actualización de renta y, coetáneamente, la aplicación al arrendatario de los conceptos que autoriza el apartado 10 de la Disp. Trans. Segunda de la L. 29/1994, 24 nov. A este respecto, y aun cuando el tema ya ha sido aludido en los Formularios números "Notificación de incremento por repercusiones fiscales" y "Notificación de repercusión del coste de servicios y suministros" ... ...no obstante se tratara en ellos la aplicación individualizada de los conceptos allí mencionados... ... cabe añadir:

1.º Que se puede exigir del arrendatario el total importe de la cuota del Impuesto sobre Bienes Inmuebles. De no hallarse individualizada la cuota habrá de dividirse en proporción a la superficie de cada vivienda de las que componen el edificio.
2.º Que se podrá repercutir en el arrendatario el coste de los servicios y suministros que se produzcan a partir de la entrada en vigor de la Ley. Se exceptúan los supuestos en que por pacto expreso entre las partes todos estos gastos sean por cuenta del arrendador.

Entienden los autores Lozano Romeral y De Fuentes Bardaji, (Todo sobre la nueva Ley de Arrendamientos Urbanos, Ed. Praxis, S.A., 1994, págs. 315 y 316) que el precepto se refiere «a la parte del flujo continuo que se produzca a partir del 1 de enero de 1995. No se trataría, por consiguiente, de una referencia hecha a nuevos servicios y suministros que se comiencen a prestar a partir de la entrada en vigor de la L.A.U. (pensemos en una casa sin portero que empieza a tenerlo), sino de servicios y suministros que ya se vengan percibiendo. El coste correspondiente a partir del 1 de enero de 1995 podrá ser repercutido al arrendatario en su integridad», tesis con la que estamos de acuerdo.

(2) Para los contratos de arrendamiento de locales de negocio celebrados con anterioridad al 9 de mayo de 1985, la L. 29/1994, 24 nov. prevé, en su Disp. Trans. Tercera, apartado 6, la posibilidad de actualizar la renta previo requerimiento fehaciente al arrendatario, que podrá ser realizado en la fecha en que, a partir de la entrada en vigor de la Ley, se cumpla una anualidad de vigencia del contrato. La renta pactada inicialmente en el contrato que dio origen al arrendamiento deberá mantener, con la renta actualizada, la misma proporción que el Índice General Nacional del Sistema de Índices de Precios de Consumo o el Índice General Nacional Índice General Urbano del Sistema de Índices de Costes de Vida del mes anterior la fecha del contrato con respecto del índice correspondiente al mes anterior a la fecha de cada actualización.

De la renta actualizada que corresponda a cada período anual sólo será exigible al arrendatario el porcentaje previsto en las tablas contenidas en las reglas 3.ª y 4.ª.

Habrá de tenerse en cuenta en cada momento, por lo tanto, ya que constituye un criterio fundamental para la aplicación del calendario de la actualización, los plazos de extinción del contrato regulados en el apartado 3 y apartado 4, reglas 1.ª y 2.ª. La Ley establece en dicho sentido una relación directa entre el período de extinción y el plazo de actualización, de guisa tal que a menor plazo para la extinción se asigna también, como es obvio, un menor plazo para alcanzar el 100% de la actualización.

Todo ello conforme al siguiente esquema que podríamos establecer:

1.º) Casos en que corresponde la actualización en un período de diez años, por remisión a la regla 9.ª-a, del apartado 11, de la Disposición Transitoria Segunda:

Arrendamientos concertados con personas físicas, que son los comprendidos en el apartado 3, y con personas jurídicas cuyos contratos se extinguen en un período de quince o veinte años y que son:

a) Los que desarrollen en el local arrendado actividades comerciales comprendidas en la División 6 de la tarifa del I.A.E., y cuyos locales no tengan una superficie superior a 2.500 metros cuadrados (comprendidos en apartado 4, regla 1.ª).
b) Los que desarrollando actividades diferentes a las mencionadas en el precedente apartado les corresponda una cuota según las tarifas del I.A.E. inferior a 130.000 pesetas / 781,32 euros (comprendidos en apartado 4, regla 2.ª).
2.º) Casos en que corresponde la actualización en un período de cinco años, a tenor de lo previsto en la regla 3.ª del apartado 6 de la Disposición Transitoria Tercera:

Arrendamientos concertados con personas jurídicas cuyos contratos se extinguen en un período de cinco o diez años y que son:

a) Los que, comprendidos en el apartado 4, regla 1.ª, la superficie del local sea superior a 2.500 metros cuadrados.
b) Los que desarrollando actividades diferentes a actividades comerciales comprendidas en la División 6 de la tarifa del I.A.E. les corresponda una cuota de tal Impuesto superior a 130.000 pesetas / 781,32 euros (comprendidos en apartado 4, regla 2.ª).

La División 6 del I.A.E. comprende Actividades industriales, comerciales mineras. Comercio, restaurantes y hostelería. Reparaciones.

Véanse normas reguladoras del I.A.E., contenidas en las siguientes disposiciones: RD Leg. 2/2004, 5 mar., Haciendas Locales; L. 6/1991, 11 mar., modificación parcial de I.A.E., y R.D.Leg. 1175/1990, 28 sep., aprueba las tarifas e instrucción del I.A.E. Asimismo, deben tenerse en cuenta las sucesivas Leyes de Presupuestos Generales del Estado, que han ido modificando el I.A.E.


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
