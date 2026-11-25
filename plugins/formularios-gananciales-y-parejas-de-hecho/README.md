# Gananciales, regímenes económicos y parejas de hecho

> Plugin de Claude Code `formularios-gananciales-y-parejas-de-hecho` · **88 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la economía de la familia: capitulaciones matrimoniales, régimen de gananciales y de separación de bienes, inventario y liquidación de la sociedad de gananciales, compensación económica, parejas de hecho y estables (también forales) y donaciones entre cónyuges.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 88 está al final):

- **Demandas, peticiones y solicitudes iniciales** (18). Por ejemplo: Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido; Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación; Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña).
- **Contestaciones, oposiciones y alegaciones** (7). Por ejemplo: Contestación a la demanda de extinción de pareja estable (Derecho catalán); Contestación a la demanda de extinción de pareja de hecho sin hijos comunes; Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña.
- **Contratos, pactos y cláusulas** (14). Por ejemplo: Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán); Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña); Pacto de convivencia de una unión de hecho según el Derecho valenciano.
- **Estatutos, actas, certificaciones y escrituras** (21). Por ejemplo: Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores; Escritura de capitulaciones posteriores al matrimonio que adoptan la sociedad de gananciales; Escritura de aportación de un bien a la sociedad de gananciales.
- **Comunicaciones, requerimientos y cartas** (14). Por ejemplo: Solicitud de inventario en la liquidación del régimen económico matrimonial (Derecho catalán); Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán); Solicitud de inventario en la liquidación del régimen matrimonial (comunicación foral vasca).
- **Escritos de trámite y otros** (14). Por ejemplo: Liquidación del régimen económico-matrimonial de mutuo acuerdo (solicitud); Propuesta de inventario para reclamar la compensación por razón de trabajo (Derecho catalán); Nota de inscripción registral de la compraventa para la sociedad de gananciales.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Capitulaciones matrimoniales para pactar la separación de bienes»
   - «Demanda de liquidación de la sociedad de gananciales»
   - «Pacto de convivencia de una pareja de hecho»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-gananciales-y-parejas-de-hecho:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-gananciales-y-parejas-de-hecho:acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 5.459 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-gananciales-y-parejas-de-hecho@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-gananciales-y-parejas-de-hecho@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-gananciales-y-parejas-de-hecho.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (88)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0012 | Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores | `acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012` |
| CIV-0052 | Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido | `demanda-liquidacion-gananciales-particion-herencia-civ-0052` |
| CIV-0065 | Escritura de capitulaciones posteriores al matrimonio que adoptan la sociedad de gananciales | `escritura-capitulaciones-posteriores-matrimonio-civ-0065` |
| CIV-0076 | Solicitud de inventario en la liquidación del régimen económico matrimonial (Derecho catalán) | `solicitud-inventario-liquidacion-regimen-economico-civ-0076` |
| CIV-0087 | Liquidación del régimen económico-matrimonial de mutuo acuerdo (solicitud) | `liquidacion-regimen-economico-matrimonial-mutuo-civ-0087` |
| CIV-0106 | Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán) | `solicitud-liquidacion-regimen-participacion-propuesta-civ-0106` |
| CIV-0107 | Propuesta de inventario para reclamar la compensación por razón de trabajo (Derecho catalán) | `propuesta-inventario-reclamar-compensacion-razon-civ-0107` |
| CIV-0110 | Contestación a la demanda de extinción de pareja estable (Derecho catalán) | `contestacion-demanda-extincion-pareja-estable-derecho-civ-0110` |
| CIV-0132 | Nota de inscripción registral de la compraventa para la sociedad de gananciales | `nota-inscripcion-registral-compraventa-sociedad-civ-0132` |
| CIV-0133 | Escritura de aportación de un bien a la sociedad de gananciales | `escritura-aportacion-bien-sociedad-gananciales-civ-0133` |
| CIV-0134 | Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes | `escritura-cese-proindivision-adjudicacion-entre-civ-0134` |
| CIV-0141 | Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán) | `convenio-regulador-tras-ruptura-union-hecho-derecho-civ-0141` |
| CIV-0157 | Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña) | `convenio-regulador-mutuo-acuerdo-sobre-hijos-fuera-civ-0157` |
| CIV-0179 | Pacto de convivencia de una unión de hecho según el Derecho valenciano | `pacto-convivencia-union-hecho-segun-derecho-valenciano-civ-0179` |
| CIV-0187 | Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación | `demanda-disolucion-sociedad-gananciales-discapacidad-civ-0187` |
| CIV-0188 | Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña) | `demanda-consensual-medidas-parentales-economicas-tras-civ-0188` |
| CIV-0194 | Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales | `demanda-anadir-bienes-liquidacion-previa-sociedad-civ-0194` |
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
| CIV-0211 | Convenio regulador de divorcio sin hijos con régimen de separación de bienes | `convenio-regulador-divorcio-sin-hijos-regimen-civ-0211` |
| CIV-0212 | Escritura de capitulaciones matrimoniales con régimen de participación | `escritura-capitulaciones-matrimoniales-regimen-civ-0212` |
| CIV-0216 | Escritura de capitulaciones matrimoniales con reconciliación de los cónyuges | `escritura-capitulaciones-matrimoniales-reconciliacion-civ-0216` |
| CIV-0221 | Escritura de poder para vender bienes gananciales | `escritura-poder-vender-bienes-gananciales-civ-0221` |
| CIV-0223 | Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico | `convenio-regulador-divorcio-custodia-compartida-civ-0223` |
| CIV-0224 | Convenio regulador de divorcio con hijos menores y liquidación del régimen económico matrimonial | `convenio-regulador-divorcio-hijos-menores-liquidacion-civ-0224` |
| CIV-0225 | Escritura de ratificación de la venta de bienes gananciales | `escritura-ratificacion-venta-bienes-gananciales-civ-0225` |
| CIV-0230 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0230` |
| CIV-0231 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0231` |
| CIV-0233 | Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña) | `demanda-conviviente-superstite-pareja-estable-contra-civ-0233` |
| CIV-0234 | Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común) | `demanda-cese-convivencia-pareja-estable-hecho-medidas-civ-0234` |
| CIV-0235 | Demanda de extinción de pareja estable según el Derecho civil catalán | `demanda-extincion-pareja-estable-segun-derecho-civil-civ-0235` |
| CIV-0236 | Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco | `demanda-cese-convivencia-pareja-hecho-segun-derecho-civ-0236` |
| CIV-0237 | Contestación a la demanda de extinción de pareja de hecho | `contestacion-demanda-extincion-pareja-hecho-civ-0237` |
| CIV-0238 | Solicitud de inventario en la liquidación del régimen matrimonial (comunicación foral vasca) | `solicitud-inventario-liquidacion-regimen-matrimonial-civ-0238` |
| CIV-0242 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0242` |
| CIV-0243 | Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro) | `solicitud-inventario-liquidacion-sociedad-conquistas-civ-0243` |
| CIV-0244 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (conquistas, Navarra) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0244` |
| CIV-0245 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0245` |
| CIV-0247 | Convenio de los cónyuges para liquidar la sociedad de gananciales | `convenio-conyuges-liquidar-sociedad-gananciales-civ-0247` |
| CIV-0256 | Propuesta de liquidación del régimen económico matrimonial de participación | `propuesta-liquidacion-regimen-economico-matrimonial-civ-0256` |
| CIV-0259 | Solicitud de liquidación del régimen económico matrimonial por uno de los cónyuges | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0259` |
| CIV-0282 | Cuaderno particional de la sociedad de gananciales disuelta, elaborado por el contador-partidor | `cuaderno-particional-sociedad-gananciales-disuelta-civ-0282` |
| CIV-0308 | Solicitud de liquidación del régimen económico matrimonial de participación | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0308` |
| CIV-0309 | Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho | `demanda-contenciosa-sobre-relaciones-paternofiliales-civ-0309` |
| CIV-0312 | Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación | `solicitud-liquidacion-sociedad-gananciales-propuesta-civ-0312` |
| CIV-0314 | Solicitud de formar inventario para liquidar el régimen económico matrimonial | `solicitud-formar-inventario-liquidar-regimen-economico-civ-0314` |
| CIV-0315 | Formación de inventario sin controversia (acta) | `formacion-inventario-sin-controversia-acta-civ-0315` |
| CIV-0325 | Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-alimentos-civ-0325` |
| CIV-0353 | Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-hijos-civ-0353` |
| CIV-0355 | Convenio regulador de la ruptura de pareja de hecho con hijos menores | `convenio-regulador-ruptura-pareja-hecho-hijos-menores-civ-0355` |
| CIV-0364 | Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales | `contestacion-demanda-juicio-ordinario-pide-rescindir-civ-0364` |
| CIV-0365 | Capitulaciones matrimoniales posteriores al matrimonio que modifican el régimen económico (Bizkaia) | `capitulaciones-matrimoniales-posteriores-matrimonio-civ-0365` |
| CIV-0366 | Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio | `capitulaciones-matrimoniales-otorgadas-ante-notario-civ-0366` |
| CIV-0372 | Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte | `demanda-rescindir-liquidacion-sociedad-conyugal-lesion-civ-0372` |
| CIV-2198 | Convenio regulador de divorcio con capitulaciones previas y custodia exclusiva de los hijos | `convenio-regulador-divorcio-capitulaciones-previas-civ-2198` |
| CIV-2229 | Demanda de juicio verbal para fijar las visitas del hijo menor tras romperse la pareja de hecho | `demanda-juicio-verbal-fijar-visitas-hijo-menor-tras-civ-2229` |
| CIV-2230 | Solicitud de medida cautelar previa de alimentos para el hijo menor tras romperse la pareja de hecho | `solicitud-medida-cautelar-previa-alimentos-hijo-menor-civ-2230` |
| CIV-2231 | Solicitud por otrosí de medida cautelar sobre la custodia del hijo tras romperse la pareja de hecho | `solicitud-otrosi-medida-cautelar-sobre-custodia-hijo-civ-2231` |
| CIV-2233 | Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho | `solicitud-medidas-previas-sobre-custodia-hijos-tras-civ-2233` |
| CIV-2239 | Demanda ordinaria por la compensación pactada por desequilibrio tras romper la pareja de hecho | `demanda-ordinaria-compensacion-pactada-desequilibrio-civ-2239` |
| CIV-2241 | Demanda de juicio verbal de alimentos para el hijo común tras extinguirse la pareja de hecho | `demanda-juicio-verbal-alimentos-hijo-comun-tras-civ-2241` |
| CIV-2242 | Demanda de compensación por desequilibrio económico tras romper la pareja de hecho sin pacto expreso | `demanda-compensacion-desequilibrio-economico-tras-civ-2242` |
| CIV-2256 | Solicitud de un cónyuge para liquidar judicialmente la sociedad de gananciales | `solicitud-conyuge-liquidar-judicialmente-sociedad-civ-2256` |
| CIV-2261 | Propuesta de liquidación de los gananciales que acompaña a la solicitud de liquidación | `propuesta-liquidacion-gananciales-acompana-solicitud-civ-2261` |
| CIV-2262 | Propuesta de inventario de los gananciales que acompaña a la solicitud de formación de inventario | `propuesta-inventario-gananciales-acompana-solicitud-civ-2262` |
| CIV-2265 | Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad | `otrosi-demanda-matrimonial-pide-formacion-inventario-civ-2265` |
| CIV-2267 | Contestación que rechaza acumular compensación y alimentos del hijo tras romper la pareja de hecho | `contestacion-rechaza-acumular-compensacion-alimentos-civ-2267` |
| CIV-2273 | Contestación que opone la prescripción de la compensación reclamada tras romper la pareja de hecho | `contestacion-opone-prescripcion-compensacion-reclamada-civ-2273` |
| CIV-2275 | Demanda verbal sucinta de cantidad tras romper de mutuo acuerdo una pareja de hecho madrileña | `demanda-verbal-sucinta-cantidad-tras-romper-mutuo-civ-2275` |
| CIV-2294 | Convenio de separación con liquidación de gananciales y crédito extinguido por confusión | `convenio-separacion-liquidacion-gananciales-credito-civ-2294` |
| CIV-2297 | Convenio de separación con hijos menores, liquidación del régimen y suspensión temporal | `convenio-separacion-hijos-menores-liquidacion-regimen-civ-2297` |
| CIV-2300 | Convenio de separación con hijos menores tras liquidar el régimen económico en capitulaciones | `convenio-separacion-hijos-menores-tras-liquidar-civ-2300` |
| CIV-2301 | Convenio regulador de divorcio con hijos mayores de edad y régimen económico ya liquidado | `convenio-regulador-divorcio-hijos-mayores-edad-regimen-civ-2301` |
| CIV-2302 | Convenio regulador de divorcio que incluye la liquidación de la sociedad de gananciales | `convenio-regulador-divorcio-incluye-liquidacion-civ-2302` |
| CIV-2303 | Capitulaciones tras el matrimonio que sustituyen el régimen por el de comunidad universal de bienes | `capitulaciones-tras-matrimonio-sustituyen-regimen-civ-2303` |
| CIV-2304 | Capitulaciones que cambian el régimen y disuelven la sociedad de gananciales sin liquidarla | `capitulaciones-cambian-regimen-disuelven-sociedad-civ-2304` |
| CIV-2308 | Capitulaciones que cambian el régimen y disuelven y liquidan la sociedad de gananciales | `capitulaciones-cambian-regimen-disuelven-liquidan-civ-2308` |

## Privacidad

Ver `PRIVACY.md`.
