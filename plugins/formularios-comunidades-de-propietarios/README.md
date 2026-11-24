# Comunidades de propietarios

> Plugin de Claude Code `formularios-comunidades-de-propietarios` · **46 formularios** · Civil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la propiedad horizontal: convocatorias y actas de junta, estatutos, impugnación de acuerdos, reclamación de cuotas a morosos, obras en elementos comunes y privativos, actividades molestas y relaciones con el administrador.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 46 está al final):

- **Demandas, peticiones y solicitudes iniciales** (16). Por ejemplo: Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad; Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación; Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad.
- **Contestaciones, oposiciones y alegaciones** (4). Por ejemplo: Oposición al monitorio por gastos comunes de comunidad de propietarios de menos de 2.000 euros; Oposición al monitorio por gastos comunes de comunidad de propietarios de entre 2.000 y 15.000 euros; Oposición al monitorio por gastos comunes de comunidad de propietarios de más de 15.000 euros.
- **Contratos, pactos y cláusulas** (2). Por ejemplo: Contrato de servicios de limpieza para una comunidad de propietarios; Contrato de arrendamiento de un elemento común para instalar antenas de telefonía.
- **Estatutos, actas, certificaciones y escrituras** (8). Por ejemplo: Estatutos de una subcomunidad de plazas de garaje y trasteros; Estatutos de una comunidad de propietarios; Acta de constitución de una comunidad de propietarios.
- **Comunicaciones, requerimientos y cartas** (7). Por ejemplo: Comunicación a la junta de propietarios para dividir materialmente un elemento privativo; Comunicación del administrador de la comunidad sobre la necesidad de reparaciones urgentes; Comunicación del propietario disidente que cambia el sentido de su voto.
- **Escritos de trámite y otros** (9). Por ejemplo: Escrito del propietario disidente que solicita acceso a servicios o instalaciones comunitarias; Diligencia del administrador-secretario que subsana un error en el acta de la junta de propietarios; División Horizontal (escritura).

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Impugnación de un acuerdo de la junta de propietarios»
   - «Reclamación de cuotas de comunidad impagadas»
   - «Acción de cesación por actividad molesta en un piso»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-comunidades-de-propietarios:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-comunidades-de-propietarios:comunicacion-junta-propietarios-dividir-materialmente-civ-0609`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 2.863 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-comunidades-de-propietarios@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-comunidades-de-propietarios@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-comunidades-de-propietarios.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (46)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0609 | Comunicación a la junta de propietarios para dividir materialmente un elemento privativo | `comunicacion-junta-propietarios-dividir-materialmente-civ-0609` |
| CIV-0610 | Escrito del propietario disidente que solicita acceso a servicios o instalaciones comunitarias | `escrito-propietario-disidente-solicita-acceso-civ-0610` |
| CIV-0611 | Comunicación del administrador de la comunidad sobre la necesidad de reparaciones urgentes | `comunicacion-administrador-comunidad-sobre-necesidad-civ-0611` |
| CIV-0612 | Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad | `demanda-propietario-suspender-obra-nueva-hecha-sin-civ-0612` |
| CIV-0613 | Oposición al monitorio por gastos comunes de comunidad de propietarios de menos de 2.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0613` |
| CIV-0614 | Oposición al monitorio por gastos comunes de comunidad de propietarios de entre 2.000 y 15.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0614` |
| CIV-0615 | Oposición al monitorio por gastos comunes de comunidad de propietarios de más de 15.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0615` |
| CIV-0616 | Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación | `demanda-comunidad-contra-secretario-administrador-civ-0616` |
| CIV-0617 | Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad | `demanda-reclamacion-gastos-extraordinarios-propietario-civ-0617` |
| CIV-0618 | Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua | `demanda-juicio-equidad-propiedad-horizontal-sobre-civ-0618` |
| CIV-0619 | Diligencia del administrador-secretario que subsana un error en el acta de la junta de propietarios | `diligencia-administrador-secretario-subsana-error-acta-civ-0619` |
| CIV-0620 | Demanda de la comunidad de propietarios contra el administrador por rendición de cuentas y daños | `demanda-comunidad-propietarios-contra-administrador-civ-0620` |
| CIV-0621 | Demanda de juicio verbal para reclamar cuotas de la comunidad de propietarios | `demanda-juicio-verbal-reclamar-cuotas-comunidad-civ-0621` |
| CIV-0622 | Contrato de servicios de limpieza para una comunidad de propietarios | `contrato-servicios-limpieza-comunidad-propietarios-civ-0622` |
| CIV-0623 | Estatutos de una subcomunidad de plazas de garaje y trasteros | `estatutos-subcomunidad-plazas-garaje-trasteros-civ-0623` |
| CIV-0624 | Contrato de arrendamiento de un elemento común para instalar antenas de telefonía | `contrato-arrendamiento-elemento-comun-instalar-antenas-civ-0624` |
| CIV-0625 | Comunicación del propietario disidente que cambia el sentido de su voto | `comunicacion-propietario-disidente-cambia-sentido-voto-civ-0625` |
| CIV-0626 | Comunicación de supresión del servicio de portería o conserjería | `comunicacion-supresion-servicio-porteria-conserjeria-civ-0626` |
| CIV-0627 | Comunicación para encargar un informe técnico sobre una instalación o servicio común | `comunicacion-encargar-informe-tecnico-sobre-civ-0627` |
| CIV-0628 | Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas | `demanda-declarar-ilegales-cuotas-participacion-civ-0628` |
| CIV-0629 | División Horizontal (escritura) | `division-horizontal-escritura-civ-0629` |
| CIV-0630 | Demanda de la comunidad contra un propietario por obras en su elemento privativo (Cataluña) | `demanda-comunidad-contra-propietario-obras-elemento-civ-0630` |
| CIV-0631 | Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña) | `demanda-impugnacion-acuerdo-junta-propietarios-abuso-civ-0631` |
| CIV-0632 | Solicitud de diligenciado del libro de actas en el Registro por una comunidad recién constituida | `solicitud-diligenciado-libro-actas-registro-comunidad-civ-0632` |
| CIV-0633 | Estatutos de una comunidad de propietarios | `estatutos-comunidad-propietarios-civ-0633` |
| CIV-0634 | Acta de constitución de una comunidad de propietarios | `acta-constitucion-comunidad-propietarios-civ-0634` |
| CIV-0635 | Estatutos reguladores de una urbanización | `estatutos-reguladores-urbanizacion-civ-0635` |
| CIV-0636 | Reglamento de régimen interior de una comunidad de propietarios | `reglamento-regimen-interior-comunidad-propietarios-civ-0636` |
| CIV-0637 | Normas de régimen interior de una urbanización | `normas-regimen-interior-urbanizacion-civ-0637` |
| CIV-0638 | Escritura de declaración de obra nueva y división horizontal | `escritura-declaracion-obra-nueva-division-horizontal-civ-0638` |
| CIV-0639 | Demanda de juicio ordinario de impugnación de acuerdos de la junta de propietarios | `demanda-juicio-ordinario-impugnacion-acuerdos-junta-civ-0639` |
| CIV-0640 | Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario | `contestacion-propiedad-horizontal-reconvencion-civ-0640` |
| CIV-0641 | Requerimiento al propietario para que cese en actividades prohibidas en la comunidad | `requerimiento-propietario-cese-actividades-prohibidas-civ-0641` |
| CIV-0642 | Acta de junta de propietarios que aprueba la liquidación de deuda y la reclamación al moroso | `acta-junta-propietarios-aprueba-liquidacion-deuda-civ-0642` |
| CIV-0643 | Instancia al Registro de la Propiedad para diligenciar el libro de actas de la comunidad | `instancia-registro-propiedad-diligenciar-libro-actas-civ-0643` |
| CIV-0644 | Autorización escrita para representar a un propietario en la junta | `autorizacion-escrita-representar-propietario-junta-civ-0644` |
| CIV-0645 | Designación de representante en la junta por los copropietarios proindiviso de un piso o local | `designacion-representante-junta-copropietarios-civ-0645` |
| CIV-0646 | Acta de junta de propietarios que acuerda la remoción de cargos electos | `acta-junta-propietarios-acuerda-remocion-cargos-electos-civ-0646` |
| CIV-0647 | Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes | `demanda-juicio-ordinario-propietario-contra-comunidad-civ-0647` |
| CIV-0648 | Demanda de juicio de equidad en propiedad horizontal para nombrar presidente de la comunidad | `demanda-juicio-equidad-propiedad-horizontal-nombrar-civ-0648` |
| CIV-0649 | Demanda de juicio de equidad en propiedad horizontal para adoptar acuerdo sin mayorías legales | `demanda-juicio-equidad-propiedad-horizontal-adoptar-civ-0649` |
| CIV-0650 | Encabezamiento de demanda monitoria de la comunidad de propietarios presentada por su presidente | `encabezamiento-demanda-monitoria-comunidad-civ-0650` |
| CIV-0651 | Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad | `convocatoria-junta-ordinaria-propietarios-presidente-civ-0651` |
| CIV-0652 | Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta | `demanda-impugnacion-acuerdos-comunidad-falta-citacion-civ-0652` |
| CIV-0653 | Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad | `demanda-privacion-uso-vivienda-actividades-danosas-civ-0653` |
| CIV-0654 | Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes | `demanda-alteracion-no-consentida-elementos-privativos-civ-0654` |

## Privacidad

Ver `PRIVACY.md`.
