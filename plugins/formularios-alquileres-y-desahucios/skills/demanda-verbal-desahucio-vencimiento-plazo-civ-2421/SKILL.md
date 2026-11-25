---
name: demanda-verbal-desahucio-vencimiento-plazo-civ-2421
description: "Demanda verbal de desahucio por vencimiento del plazo del arrendamiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda verbal de desahucio por vencimiento del plazo del arrendamiento

> Formulario **CIV-2421** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Demanda de Juicio Verbal de Desahucio por expiración de plazo del contrato de arrendamiento urbano, amparada en lo establecido por los artículos 9 y 10 LEC 2000.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda verbal de desahucio por vencimiento del plazo del arrendamiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda verbal de desahucio por vencimiento del plazo del arrendamiento” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-verbal-desahucio-vencimiento-plazo-civ-2421`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (24 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] CALLE (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] PISO (3 veces)
- [ ] Nº (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] FECHAS
- [ ] LUGAR
- [ ] PARTIDO JUDICIAL

## Normas que cita el formulario

- art. 10 Ley 29/1994
- art. 439.6 LEC
- art. 36 LEC
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 23 LEC
- art. 250.1.1.º LEC
- art. 253 LEC
- art. 3.k Ley 12/2023
- art. 5 Ley Orgánica 1/2025
- art. 9 Ley 29/1994
- art. 1569 Código Civil
- art. 394 Ley 1/2000
- art. 438.6 LEC
- art. 549.3 LEC
- art. 437.1 LEC

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

- Al principio del formulario: Contratos anteriores al 6-3-2019: los plazos de duración mínima y de preaviso son los de la redacción del art. 9 y 10 LAU vigente al firmarlos (comprobar).
- Junto a «…o son los de la redacción del art. 9 y 10 LAU vigente al firmarlos (comprobar).]»: El RDL 28/2026 (estabilidad de los arrendamientos de vivienda habitual) fue derogado por el Congreso el 12-11-2026 (BOE-A-2026-23754); el art. 10 LAU está en la redacción de la Ley 12/2023.
- Junto a «…2026 (BOE-A-2026-23754); el art. 10 LAU está en la redacción de la Ley 12/2023.]»: Hechos sobre vivienda habitual y gran tenedor: adaptarlos y aportar la certificación registral (art. 439.6 LEC); arrendatario vulnerable: art. 441.5-7 LEC y suspensión del art. 2 RDL 29/2026.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) En los Fundamentos de Derecho Sustantivo del Formulario ya se indica de forma exhaustiva la razón que abona el ejercicio de la acción.

Es preceptiva la intervención de Procurador (art. 23 LEC) y de Letrado (art. 31 LEC). La cuantía debe señalarse en la demanda al venir así exigido por el art. 253 LEC, estableciéndose ésta conforme a las reglas contenidas en el art. 251. La regla 9 de dicho precepto, dotada de nueva redacción por el apartado Nueve del Artículo Segundo de la Ley 19/2009, de 23 de noviembre, establece que en los juicios de arrendamientos de bienes, salvo cuando tengan por objeto reclamaciones de las rentas o cantidades debidas, la cuantía de la demanda será el importe de una anualidad de renta, cualquiera que sea la periodicidad con que ésta aparezca fijada en el contrato.

El Formulario también es susceptible de aplicación, en su estructura, en el caso de arrendamientos para uso distinto del de vivienda, pero entonces deberá suprimirse la referencia a los arts. 9 y 10 de la LAU 1994 por la invocación de los preceptos que, en su caso, correspondan. Lo mismo ocurre si se trata de arrendamientos subsistentes el día 1 de enero de 1995, ora lo sean de vivienda ora de local de negocio, si bien en tal caso deberá invocarse:

En el caso de arrendamientos celebrados a partir del 9 de mayo de 1985, la Disposición Transitoria Primera, apartados 1 ó 2, según se trate de viviendas o locales, y el art. 9.º del R.D.L. 2/1985, de 30 de abril, que suprimió la prórroga forzosa. Nótese, empero, que en arrendamientos de viviendas de producirse la tácita reconducción lo será por el plazo de tres años, aplicándose al arrendamiento renovado lo dispuesto en la Ley 29/1994, de 24 de noviembre, para los arrendamientos de vivienda.

En el caso de arrendamientos de local de negocio celebrados antes del 9 de mayo de 1985 que no se encuentren en prórroga porque aún no haya transcurrido el plazo determinado pactado, deberá citarse el apartado 5 de la Disposición Transitoria Tercera LAU 1994.

En el caso de arrendamientos de vivienda celebrados antes del 9 de mayo de 1985 en los que se hubiera producido subrogación mortis causa y haya transcurrido el período de duración de la misma según las previsiones de los apartados 4 a 8 de la Disposición Transitoria Segunda LAU 1994, deberá invocarse el apartado concreto que corresponda.

En relación a la cuantía, el R.D. 1417/2001, de 17 de diciembre (BOE de 27 de diciembre), solo convirtió a euros las cuantías originales de la LEC; los límites vigentes resultan de los arts. 249.2 y 250.2 LEC (15.000 euros).


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
