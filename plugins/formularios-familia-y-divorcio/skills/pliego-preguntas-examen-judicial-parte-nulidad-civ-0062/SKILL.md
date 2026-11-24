---
name: pliego-preguntas-examen-judicial-parte-nulidad-civ-0062
description: "Pliego de preguntas para el examen judicial de la parte en una nulidad canónica por el canon 1095.2. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Pliego de preguntas para el examen judicial de la parte en una nulidad canónica por el canon 1095.2

> Formulario **CIV-0062** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Pliego de preguntas para el examen judicial de la parte en una nulidad canónica por el canon 1095.2» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Pliego de preguntas para el examen judicial de la parte en una nulidad canónica por el canon 1095.2” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:pliego-preguntas-examen-judicial-parte-nulidad-civ-0062`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
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

Presentación por el Letrado o Procurador
Rasgos característicos de la familia en que creció
Aspectos de su familia que más han marcado su carácter y forma de ser
Rasgos de la familia del otro contrayente e influencia en su personalidad
Circunstancias en que se conocieron los cónyuges y decidieron iniciar su noviazgo
Experiencias previas en relaciones de noviazgo
Circunstancias de la propia personalidad y madurez en el momento de iniciarse el noviazgo
Personalidad y forma de ser del otro contrayente en el momento de iniciarse el noviazgo
Circunstancias del embarazo previo al noviazgo
Cómo afectó a la pareja la noticia del embarazo
Decisiones que adoptaron como consecuencia del embarazo
Consejos que recibieron de su ámbito familiar
Conocimiento mutuo previo al matrimonio
Medios de vida al contraer matrimonio
Vivienda
Inicio de la crisis matrimonial
Características de su convivencia matrimonial
Antecedentes psiquiátricos
Custodia de los hijos y cumplimiento de las obligaciones familiares
Posibilidades de reconciliación
Firmas

PLIEGO DE POSICIONES

Que presenta el letrado D./Dª [NOMBRE Y APELLIDOS], en representación y defensa de la parte actora/demandada dentro de la causa de nulidad matrimonial nº [NÚMERO], para el examen judicial del/de la esposa/esposo demandada/o D./Dª [NOMBRE Y APELLIDOS]

1. ¿Qué rasgos resaltaría usted como más característicos de la familia en la que usted nació y creció? (situación económica, profesión de los padres, nivel cultural, número de hijos y orden de nacimiento, valores y prácticas religiosas, etc.)

2. ¿Qué aspectos concretos de su familia, y de la vida familiar cree usted que la han marcado en mayor medida en su carácter, personalidad y forma de ser? ¿En qué modo considera que le han marcado y configurado su forma de ser y propia personalidad?

3. ¿Cuáles son los rasgos que mejor describen y caracterizan a la familia en la que nació y creció el/la esposo/a? ¿Cuáles de ellos cree usted que han marcado más su forma de ser de? ¿Por qué cree usted que eso es así?

4. ¿Cuándo (fecha concreta) y en qué circunstancias concretas se conocieron usted y el/la esposo/a? ¿En qué momento deciden iniciar la relación de noviazgo?

5. ¿Qué experiencia tenía usted en mantener una verdadera relación de noviazgo al momento de iniciar su noviazgo con ella/él? ¿Qué experiencia tenía él/ella en este tipo de relaciones?

6. ¿Cuáles piensa que son los rasgos de la personalidad que más le caracterizaban a usted en las fechas en que inició ese noviazgo? ¿Cómo se definiría usted? ¿Cómo piensa usted que era usted en cuanto a su madurez personal? ¿Cómo se encontraba usted en la relación familiar/laboral/social? ¿Cómo se encontraba anímicamente? ¿Cómo se encontraba a nivel afectivo?

7. ¿Cuáles eran los rasgos más característicos de la personalidad y forma de ser del/ de la esposo/a en aquella época?

8. ¿Cuándo conocieron ustedes su/el estado de embarazo? ¿Cuánto tiempo había transcurrido desde el inicio del noviazgo?

9. ¿Cómo les afecto a ustedes la noticia?

10. ¿Qué decisión adoptaron? ¿Qué le llevó a usted a tomar esa decisión?

11. ¿Qué les aconsejaron las personas cercanas y familiares? ¿Quiénes? ¿Atendieron sus consejos? ¿Por qué?

12. ¿Cree usted que el tiempo de noviazgo les había permitido un conocimiento mutuo suficiente que garantizase mínimamente la decisión de matrimoniar?

13. ¿Tenían ustedes trabajo que les procurase ingresos suficientes para realizar el proyecto matrimonial?

14. ¿Tenían ustedes vivienda en la que poder instalarse tras el matrimonio? ¿dónde se instalaron?

15. ¿Qué primeros problemas comenzaron a apreciar ustedes en su relación? ¿En qué momento del matrimonio sopesaron ya proceder a la separación?

16. ¿Cómo se desarrolló la convivencia matrimonial? ¿Cómo definiría usted su vida matrimonial? ¿Qué rasgos definirían mejor lo que fue ese tiempo?

17. ¿Han recibido usted o su esposo/a tratamiento psicológico en algún momento de su vida? ¿Por qué? ¿En qué modo ello afectó a la vida matrimonial y a la convivencia? ¿Considera usted que esa circunstancia degradó la convivencia?

18. ¿Quién mantiene la custodia o convivencia con los hijos comunes? ¿Por qué? ¿Cumple usted y su esposo/a sus obligaciones legales?

19. ¿Cree usted que su vida matrimonial con Jesús puede sanarse?

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.:

========================================================================
