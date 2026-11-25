---
name: peticion-inquilinos-instalar-infraestructuras-comunes-civ-2512
description: "Petición de los inquilinos para instalar infraestructuras comunes de telecomunicaciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición de los inquilinos para instalar infraestructuras comunes de telecomunicaciones

> Formulario **CIV-2512** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición de los inquilinos para instalar infraestructuras comunes de telecomunicaciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición de los inquilinos para instalar infraestructuras comunes de telecomunicaciones” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:peticion-inquilinos-instalar-infraestructuras-comunes-civ-2512`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (3 veces)
- [ ] CALLE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] FECHA
- [ ] LUGAR
- [ ] PISO

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

Notas al pie del formulario original:
(1) Para realizar la notificación de elevación de renta por instalación o adaptación de infraestructuras para servicios de telecomunicación, utilizar el Formulario "Notificación de elevación de renta por instalación o adaptación de infraestructuras de común acceso para servicios de telecomunicación"

Este Formulario tiene como objetivo dar cumplimiento a las previsiones del art. 4.1 del R.D.L. 1/1998, 27 feb. (B.O.E. 28-2). Según el mismo, el propietario de un edificio incluido en el ámbito de aplicación de la norma que decida la instalación de una infraestructura común de acceso a servicios de telecomunicación o la adaptación de la existente, debe notificarlo por escrito a los arrendatarios, al menos con dos meses de antelación a la fecha de comienzo de las obras encaminadas a la instalación o adaptación. Establece el art. 4.2 de la normativa mencionada que si no existe consentimiento de los arrendatarios a la instalación el propietario no podrá repercutir en ellos el coste.

La repercusión del coste de la nueva infraestructura o de la adaptación de la preexistente por el propietario de un edificio en los arrendatarios se realizará, desde el mes siguiente al que se lleven a cabo, en la cuantía y proporción previstas en el art. 19 de la L. 29/1994, 24 nov., de Arrendamientos Urbanos.

A la conservación de las infraestructuras se aplica el art. 21 de la LAU 1994 en cuanto a la obligación de obras de conservación.

La instalación o adaptación de una infraestructura se considera obra de mejora a los efectos de lo establecido en el art. 22 de la LAU 1994.

La instalación de la infraestructura en edificaciones ya concluidas en el momento de entrada en vigor del R.D.L. 1/1998 (lo que tuvo lugar el 29 de febrero de 1998) o que se concluyan en el plazo de los ocho meses siguientes a tal fecha, resulta obligatoria en los siguientes casos:

a) Cuando el número de antenas instaladas, individuales o colectivas, sea superior a un tercio del número de viviendas y locales, en cuyo caso deben ser sustituidas en el plazo de seis meses siguientes a la entrada en vigor del R.D.L. mencionado, por una infraestructura común. De superarse dicho porcentaje después de la entrada en vigor el plazo de los seis meses se computará desde el momento en que se produzca tal circunstancia. El coste de la infraestructura, en tal caso, será a cargo de quienes tengan instaladas las antenas.
b) Cuando la Administración competente, de acuerdo con la normativa vigente aplicable, considere peligrosa o antiestética la colocación de antenas individuales en un edificio. El coste de la instalación será a cargo de quienes deseasen la recepción de los servicios sin perjuicio de poder repercutir en los arrendatarios el importe de la inversión.

No resulta obligatoria la instalación de la infraestructura cuando el edificio no reúna condiciones para soportarla, de acuerdo con informe emitido al respecto por la Administración competente.

(2) En concordancia con lo señalado en el Formulario "Notificación de elevación de renta por instalación o adaptación de infraestructuras de común acceso para servicios de telecomunicación", el que nos ocupa responde a la notificación que preceptivamente debe realizarse al arrendatario, conforme a lo dispuesto en el art. 4.3 del R.D.L. 1/1998, 27 feb. y art. 19 de la LAU 1994, para hacer efectivo el derecho del arrendador el incremento de renta por razón de obras de instalación de infraestructura común de acceso a servicios de telecomunicación o adaptación de las existentes.

El art. 4.3 del R.D.L. 1/1998, 27 feb., establece que la repercusión del coste por obras de tal índole se realizará, desde el mes siguiente al que se lleven a cabo, en la cuantía y proporción previstas en el art. 19 de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos. Por consiguiente, debe acudirse a las pautas establecidas en este último precepto a fin de determinar el importe objeto de repercusión y la forma de distribución del mismo.

(3) El presente Formulario responde a aquellos supuestos en que son los propios arrendatarios los interesados en instalar la infraestructura común y, por ello, solicitan la correspondiente autorización al propietario. A tal respecto, el art. 4.3 del R.D.L. 1/1998, 27 feb., prevé que si son los arrendatarios los que solicitan la instalación será a su costa el gasto que aquélla represente y, al concluir el arrendamiento, la infraestructura instalada o adaptada quedará en el edificio a disposición de su propietario. También en tal caso, y de conformidad a lo establecido en el art. 5.2 del R.D.L. 1/1998, de 27 de febrero, tan citado, los gastos de conservación de la infraestructura serán de cargo de los arrendatarios.


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
