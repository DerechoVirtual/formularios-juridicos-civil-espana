---
name: indice
description: "Índice de los 88 formularios de Gananciales, regímenes económicos y parejas de hecho. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Gananciales, regímenes económicos y parejas de hecho: índice de formularios

> Plugin `formularios-gananciales-y-parejas-de-hecho` · 88 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la economía de la familia: capitulaciones matrimoniales, régimen de gananciales y de separación de bienes, inventario y liquidación de la sociedad de gananciales, compensación económica, parejas de hecho y estables (también forales) y donaciones entre cónyuges.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Capitulaciones matrimoniales para pactar la separación de bienes»
- «Demanda de liquidación de la sociedad de gananciales»
- «Pacto de convivencia de una pareja de hecho»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-gananciales-y-parejas-de-hecho:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (18)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0052 | Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido | `demanda-liquidacion-gananciales-particion-herencia-civ-0052` |
| CIV-0187 | Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación | `demanda-disolucion-sociedad-gananciales-discapacidad-civ-0187` |
| CIV-0188 | Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña) | `demanda-consensual-medidas-parentales-economicas-tras-civ-0188` |
| CIV-0194 | Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales | `demanda-anadir-bienes-liquidacion-previa-sociedad-civ-0194` |
| CIV-0233 | Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña) | `demanda-conviviente-superstite-pareja-estable-contra-civ-0233` |
| CIV-0234 | Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común) | `demanda-cese-convivencia-pareja-estable-hecho-medidas-civ-0234` |
| CIV-0235 | Demanda de extinción de pareja estable según el Derecho civil catalán | `demanda-extincion-pareja-estable-segun-derecho-civil-civ-0235` |
| CIV-0236 | Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco | `demanda-cese-convivencia-pareja-hecho-segun-derecho-civ-0236` |
| CIV-0309 | Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho | `demanda-contenciosa-sobre-relaciones-paternofiliales-civ-0309` |
| CIV-0325 | Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-alimentos-civ-0325` |
| CIV-0353 | Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-hijos-civ-0353` |
| CIV-0372 | Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte | `demanda-rescindir-liquidacion-sociedad-conyugal-lesion-civ-0372` |
| CIV-2229 | Demanda de juicio verbal para fijar las visitas del hijo menor tras romperse la pareja de hecho | `demanda-juicio-verbal-fijar-visitas-hijo-menor-tras-civ-2229` |
| CIV-2233 | Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho | `solicitud-medidas-previas-sobre-custodia-hijos-tras-civ-2233` |
| CIV-2239 | Demanda ordinaria por la compensación pactada por desequilibrio tras romper la pareja de hecho | `demanda-ordinaria-compensacion-pactada-desequilibrio-civ-2239` |
| CIV-2241 | Demanda de juicio verbal de alimentos para el hijo común tras extinguirse la pareja de hecho | `demanda-juicio-verbal-alimentos-hijo-comun-tras-civ-2241` |
| CIV-2242 | Demanda de compensación por desequilibrio económico tras romper la pareja de hecho sin pacto expreso | `demanda-compensacion-desequilibrio-economico-tras-civ-2242` |
| CIV-2275 | Demanda verbal sucinta de cantidad tras romper de mutuo acuerdo una pareja de hecho madrileña | `demanda-verbal-sucinta-cantidad-tras-romper-mutuo-civ-2275` |

### Contestaciones, oposiciones y alegaciones (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0110 | Contestación a la demanda de extinción de pareja estable (Derecho catalán) | `contestacion-demanda-extincion-pareja-estable-derecho-civ-0110` |
| CIV-0230 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0230` |
| CIV-0231 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0231` |
| CIV-0237 | Contestación a la demanda de extinción de pareja de hecho | `contestacion-demanda-extincion-pareja-hecho-civ-0237` |
| CIV-0364 | Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales | `contestacion-demanda-juicio-ordinario-pide-rescindir-civ-0364` |
| CIV-2267 | Contestación que rechaza acumular compensación y alimentos del hijo tras romper la pareja de hecho | `contestacion-rechaza-acumular-compensacion-alimentos-civ-2267` |
| CIV-2273 | Contestación que opone la prescripción de la compensación reclamada tras romper la pareja de hecho | `contestacion-opone-prescripcion-compensacion-reclamada-civ-2273` |

### Contratos, pactos y cláusulas (14)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0141 | Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán) | `convenio-regulador-tras-ruptura-union-hecho-derecho-civ-0141` |
| CIV-0157 | Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña) | `convenio-regulador-mutuo-acuerdo-sobre-hijos-fuera-civ-0157` |
| CIV-0179 | Pacto de convivencia de una unión de hecho según el Derecho valenciano | `pacto-convivencia-union-hecho-segun-derecho-valenciano-civ-0179` |
| CIV-0211 | Convenio regulador de divorcio sin hijos con régimen de separación de bienes | `convenio-regulador-divorcio-sin-hijos-regimen-civ-0211` |
| CIV-0223 | Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico | `convenio-regulador-divorcio-custodia-compartida-civ-0223` |
| CIV-0224 | Convenio regulador de divorcio con hijos menores y liquidación del régimen económico matrimonial | `convenio-regulador-divorcio-hijos-menores-liquidacion-civ-0224` |
| CIV-0247 | Convenio de los cónyuges para liquidar la sociedad de gananciales | `convenio-conyuges-liquidar-sociedad-gananciales-civ-0247` |
| CIV-0355 | Convenio regulador de la ruptura de pareja de hecho con hijos menores | `convenio-regulador-ruptura-pareja-hecho-hijos-menores-civ-0355` |
| CIV-2198 | Convenio regulador de divorcio con capitulaciones previas y custodia exclusiva de los hijos | `convenio-regulador-divorcio-capitulaciones-previas-civ-2198` |
| CIV-2294 | Convenio de separación con liquidación de gananciales y crédito extinguido por confusión | `convenio-separacion-liquidacion-gananciales-credito-civ-2294` |
| CIV-2297 | Convenio de separación con hijos menores, liquidación del régimen y suspensión temporal | `convenio-separacion-hijos-menores-liquidacion-regimen-civ-2297` |
| CIV-2300 | Convenio de separación con hijos menores tras liquidar el régimen económico en capitulaciones | `convenio-separacion-hijos-menores-tras-liquidar-civ-2300` |
| CIV-2301 | Convenio regulador de divorcio con hijos mayores de edad y régimen económico ya liquidado | `convenio-regulador-divorcio-hijos-mayores-edad-regimen-civ-2301` |
| CIV-2302 | Convenio regulador de divorcio que incluye la liquidación de la sociedad de gananciales | `convenio-regulador-divorcio-incluye-liquidacion-civ-2302` |

### Estatutos, actas, certificaciones y escrituras (21)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0012 | Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores | `acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012` |
| CIV-0065 | Escritura de capitulaciones posteriores al matrimonio que adoptan la sociedad de gananciales | `escritura-capitulaciones-posteriores-matrimonio-civ-0065` |
| CIV-0133 | Escritura de aportación de un bien a la sociedad de gananciales | `escritura-aportacion-bien-sociedad-gananciales-civ-0133` |
| CIV-0134 | Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes | `escritura-cese-proindivision-adjudicacion-entre-civ-0134` |
| CIV-0197 | Escritura de extinción de pareja de hecho según el Derecho vasco | `escritura-extincion-pareja-hecho-segun-derecho-vasco-civ-0197` |
| CIV-0198 | Escritura de constitución de pareja de hecho según el Derecho vasco | `escritura-constitucion-pareja-hecho-segun-derecho-vasco-civ-0198` |
| CIV-0199 | Escritura de constitución de unión de hecho según el Derecho de Madrid | `escritura-constitucion-union-hecho-segun-derecho-madrid-civ-0199` |
| CIV-0200 | Escritura de constitución de pareja de hecho según el Derecho de Extremadura | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0200` |
| CIV-0201 | Escritura de constitución de pareja de hecho según el Derecho de Canarias | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0201` |
| CIV-0202 | Escritura de constitución de pareja estable según el Derecho de Asturias | `escritura-constitucion-pareja-estable-segun-derecho-civ-0202` |
| CIV-0203 | Escritura de constitución de pareja de hecho según el Derecho de Andalucía | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0203` |
| CIV-0204 | Escritura de constitución de pareja estable no casada según el Derecho aragonés | `escritura-constitucion-pareja-estable-no-casada-segun-civ-0204` |
| CIV-0205 | Escritura de constitución de unión de hecho según el Derecho valenciano | `escritura-constitucion-union-hecho-segun-derecho-civ-0205` |
| CIV-0206 | Escritura de extinción de pareja estable según el Derecho catalán | `escritura-extincion-pareja-estable-segun-derecho-civ-0206` |
| CIV-0207 | Escritura de constitución de pareja estable según el Derecho catalán | `escritura-constitucion-pareja-estable-segun-derecho-civ-0207` |
| CIV-0208 | Escritura de capítulos matrimoniales según el Derecho catalán | `escritura-capitulos-matrimoniales-segun-derecho-catalan-civ-0208` |
| CIV-0209 | Escritura de capítulos matrimoniales según el Derecho aragonés | `escritura-capitulos-matrimoniales-segun-derecho-civ-0209` |
| CIV-0212 | Escritura de capitulaciones matrimoniales con régimen de participación | `escritura-capitulaciones-matrimoniales-regimen-civ-0212` |
| CIV-0216 | Escritura de capitulaciones matrimoniales con reconciliación de los cónyuges | `escritura-capitulaciones-matrimoniales-reconciliacion-civ-0216` |
| CIV-0221 | Escritura de poder para vender bienes gananciales | `escritura-poder-vender-bienes-gananciales-civ-0221` |
| CIV-0225 | Escritura de ratificación de la venta de bienes gananciales | `escritura-ratificacion-venta-bienes-gananciales-civ-0225` |

### Comunicaciones, requerimientos y cartas (14)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0076 | Solicitud de inventario en la liquidación del régimen económico matrimonial (Derecho catalán) | `solicitud-inventario-liquidacion-regimen-economico-civ-0076` |
| CIV-0106 | Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán) | `solicitud-liquidacion-regimen-participacion-propuesta-civ-0106` |
| CIV-0238 | Solicitud de inventario en la liquidación del régimen matrimonial (comunicación foral vasca) | `solicitud-inventario-liquidacion-regimen-matrimonial-civ-0238` |
| CIV-0242 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0242` |
| CIV-0243 | Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro) | `solicitud-inventario-liquidacion-sociedad-conquistas-civ-0243` |
| CIV-0244 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (conquistas, Navarra) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0244` |
| CIV-0245 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0245` |
| CIV-0259 | Solicitud de liquidación del régimen económico matrimonial por uno de los cónyuges | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0259` |
| CIV-0308 | Solicitud de liquidación del régimen económico matrimonial de participación | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0308` |
| CIV-0312 | Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación | `solicitud-liquidacion-sociedad-gananciales-propuesta-civ-0312` |
| CIV-0314 | Solicitud de formar inventario para liquidar el régimen económico matrimonial | `solicitud-formar-inventario-liquidar-regimen-economico-civ-0314` |
| CIV-2230 | Solicitud de medida cautelar previa de alimentos para el hijo menor tras romperse la pareja de hecho | `solicitud-medida-cautelar-previa-alimentos-hijo-menor-civ-2230` |
| CIV-2231 | Solicitud por otrosí de medida cautelar sobre la custodia del hijo tras romperse la pareja de hecho | `solicitud-otrosi-medida-cautelar-sobre-custodia-hijo-civ-2231` |
| CIV-2256 | Solicitud de un cónyuge para liquidar judicialmente la sociedad de gananciales | `solicitud-conyuge-liquidar-judicialmente-sociedad-civ-2256` |

### Escritos de trámite y otros (14)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0087 | Liquidación del régimen económico-matrimonial de mutuo acuerdo (solicitud) | `liquidacion-regimen-economico-matrimonial-mutuo-civ-0087` |
| CIV-0107 | Propuesta de inventario para reclamar la compensación por razón de trabajo (Derecho catalán) | `propuesta-inventario-reclamar-compensacion-razon-civ-0107` |
| CIV-0132 | Nota de inscripción registral de la compraventa para la sociedad de gananciales | `nota-inscripcion-registral-compraventa-sociedad-civ-0132` |
| CIV-0256 | Propuesta de liquidación del régimen económico matrimonial de participación | `propuesta-liquidacion-regimen-economico-matrimonial-civ-0256` |
| CIV-0282 | Cuaderno particional de la sociedad de gananciales disuelta, elaborado por el contador-partidor | `cuaderno-particional-sociedad-gananciales-disuelta-civ-0282` |
| CIV-0315 | Formación de inventario sin controversia (acta) | `formacion-inventario-sin-controversia-acta-civ-0315` |
| CIV-0365 | Capitulaciones matrimoniales posteriores al matrimonio que modifican el régimen económico (Bizkaia) | `capitulaciones-matrimoniales-posteriores-matrimonio-civ-0365` |
| CIV-0366 | Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio | `capitulaciones-matrimoniales-otorgadas-ante-notario-civ-0366` |
| CIV-2261 | Propuesta de liquidación de los gananciales que acompaña a la solicitud de liquidación | `propuesta-liquidacion-gananciales-acompana-solicitud-civ-2261` |
| CIV-2262 | Propuesta de inventario de los gananciales que acompaña a la solicitud de formación de inventario | `propuesta-inventario-gananciales-acompana-solicitud-civ-2262` |
| CIV-2265 | Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad | `otrosi-demanda-matrimonial-pide-formacion-inventario-civ-2265` |
| CIV-2303 | Capitulaciones tras el matrimonio que sustituyen el régimen por el de comunidad universal de bienes | `capitulaciones-tras-matrimonio-sustituyen-regimen-civ-2303` |
| CIV-2304 | Capitulaciones que cambian el régimen y disuelven la sociedad de gananciales sin liquidarla | `capitulaciones-cambian-regimen-disuelven-sociedad-civ-2304` |
| CIV-2308 | Capitulaciones que cambian el régimen y disuelven y liquidan la sociedad de gananciales | `capitulaciones-cambian-regimen-disuelven-liquidan-civ-2308` |
