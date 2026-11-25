# Discapacidad y medidas de apoyo (Ley 8/2021)

> Plugin de Claude Code `formularios-discapacidad-y-medidas-de-apoyo` · **46 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para las personas con discapacidad tras la Ley 8/2021: provisión de medidas de apoyo, curatela, defensor judicial, guarda de hecho, autocuratela, revisión de medidas, internamientos no voluntarios y rendición de cuentas.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 46 está al final):

- **Demandas, peticiones y solicitudes iniciales** (4). Por ejemplo: Solicitud de nombramiento de defensor judicial para el tutelado; Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés); Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán).
- **Contestaciones, oposiciones y alegaciones** (3). Por ejemplo: Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad; Escrito de oposición a la apelación en el proceso de medidas judiciales de apoyo a la discapacidad; Contestación que se opone a la demanda de medidas de apoyo y propone un curador si se estima.
- **Recursos** (5). Por ejemplo: Recurso de apelación contra el auto que acuerda el internamiento; Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad; Recurso de apelación con prueba en segunda instancia contra la denegación de medidas de apoyo.
- **Contratos, pactos y cláusulas** (1). Por ejemplo: Contrato de compraventa de bienes de menores o de personas con discapacidad.
- **Comunicaciones, requerimientos y cartas** (7). Por ejemplo: Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán); Solicitud de autorización de internamiento no voluntario en un centro geriátrico; Solicitud del tutelado de revisar la tutela y remover al tutor.
- **Escritos de trámite y otros** (26). Por ejemplo: Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial; Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado; Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Solicitud de provisión de medidas de apoyo para una persona mayor»
   - «Nombramiento de defensor judicial»
   - «Revisión de las medidas de apoyo»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-discapacidad-y-medidas-de-apoyo:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-discapacidad-y-medidas-de-apoyo:escrito-tutor-pidiendo-autorizacion-internar-tutelado-civ-0373`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 2.907 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-discapacidad-y-medidas-de-apoyo@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-discapacidad-y-medidas-de-apoyo@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-discapacidad-y-medidas-de-apoyo.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (46)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0373 | Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial | `escrito-tutor-pidiendo-autorizacion-internar-tutelado-civ-0373` |
| CIV-0374 | Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado | `escrito-curador-pidiendo-prorroga-plazo-inventariar-civ-0374` |
| CIV-0375 | Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado | `escrito-tutor-pidiendo-autorizacion-judicial-demandar-civ-0375` |
| CIV-0376 | Escrito pidiendo excluir del cargo de tutor a una persona inhábil | `escrito-pidiendo-excluir-cargo-tutor-persona-inhabil-civ-0376` |
| CIV-0377 | Escrito de excusa sobrevenida para seguir en el cargo de tutor o curador | `escrito-excusa-sobrevenida-seguir-cargo-tutor-curador-civ-0377` |
| CIV-0378 | Escrito de excusa para no aceptar el cargo de tutor | `escrito-excusa-no-aceptar-cargo-tutor-civ-0378` |
| CIV-0379 | Escrito del tutor con informe de la situación del tutelado y rendición anual de cuentas | `escrito-tutor-informe-situacion-tutelado-rendicion-civ-0379` |
| CIV-0380 | Escrito alegando excusa sobrevenida para seguir como curador | `escrito-alegando-excusa-sobrevenida-seguir-como-curador-civ-0380` |
| CIV-0381 | Escrito que comunica al tribunal el fallecimiento del tutelado | `escrito-comunica-tribunal-fallecimiento-tutelado-civ-0381` |
| CIV-0382 | Solicitud de nombramiento de defensor judicial para el tutelado | `solicitud-nombramiento-defensor-judicial-tutelado-civ-0382` |
| CIV-0383 | Escrito del tutor pidiendo retribución por el ejercicio de la tutela | `escrito-tutor-pidiendo-retribucion-ejercicio-tutela-civ-0383` |
| CIV-0384 | Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán) | `solicitud-jurisdiccion-voluntaria-nombrar-asistente-civ-0384` |
| CIV-0385 | Solicitud de autorización de internamiento no voluntario en un centro geriátrico | `solicitud-autorizacion-internamiento-no-voluntario-civ-0385` |
| CIV-0386 | Documento de voluntades anticipadas o testamento vital | `documento-voluntades-anticipadas-testamento-vital-civ-0386` |
| CIV-0387 | Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés) | `demanda-constitucion-curatela-asistencia-nombramiento-civ-0387` |
| CIV-0388 | Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña) | `expediente-jurisdiccion-voluntaria-constituir-curatela-civ-0388` |
| CIV-0389 | Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón) | `expediente-jurisdiccion-voluntaria-constituir-tutela-civ-0389` |
| CIV-0390 | Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán) | `demanda-curatela-asistencia-nombramiento-curador-civ-0390` |
| CIV-0391 | Recurso de apelación contra el auto que acuerda el internamiento | `recurso-apelacion-contra-auto-acuerda-internamiento-civ-0391` |
| CIV-0392 | Solicitud del tutelado de revisar la tutela y remover al tutor | `solicitud-tutelado-revisar-tutela-remover-tutor-civ-0392` |
| CIV-0393 | Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave | `solicitud-jurisdiccion-voluntaria-curatela-persona-civ-0393` |
| CIV-0394 | Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad | `contestacion-demanda-medidas-judiciales-apoyo-persona-civ-0394` |
| CIV-0395 | Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad | `recurso-apelacion-contra-sentencia-sobre-medidas-apoyo-civ-0395` |
| CIV-0396 | Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta | `escrito-solicitando-internamiento-no-voluntario-civ-0396` |
| CIV-0397 | Solicitud de administrador de bienes como medida cautelar junto con la demanda de medidas de apoyo | `solicitud-administrador-bienes-como-medida-cautelar-civ-0397` |
| CIV-0398 | Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad | `demanda-contenciosa-revision-medidas-judiciales-apoyo-civ-0398` |
| CIV-0399 | Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad | `escrito-medidas-cautelares-previas-demanda-apoyos-civ-0399` |
| CIV-0400 | Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad | `solicitud-revision-jurisdiccion-voluntaria-medidas-civ-0400` |
| CIV-2316 | Escrito que pone en conocimiento del Fiscal hechos que pueden requerir medidas de apoyo | `escrito-pone-conocimiento-fiscal-hechos-pueden-civ-2316` |
| CIV-2317 | Escrito que pide comunicar al Registro de la Propiedad la sentencia de medidas de apoyo | `escrito-pide-comunicar-registro-propiedad-sentencia-civ-2317` |
| CIV-2318 | Comunicación del hospital al tribunal de un internamiento psiquiátrico urgente de un adulto | `comunicacion-hospital-tribunal-internamiento-civ-2318` |
| CIV-2319 | Escrito del defensor de la persona con discapacidad conforme con la demanda del Fiscal | `escrito-defensor-persona-discapacidad-conforme-demanda-civ-2319` |
| CIV-2320 | Contrato de compraventa de bienes de menores o de personas con discapacidad | `contrato-compraventa-bienes-menores-personas-civ-2320` |
| CIV-2321 | Otrosí en demanda de medidas de apoyo para nombrar un curador de la persona y otro de los bienes | `otrosi-demanda-medidas-apoyo-nombrar-curador-persona-civ-2321` |
| CIV-2322 | Recurso de apelación con prueba en segunda instancia contra la denegación de medidas de apoyo | `recurso-apelacion-prueba-segunda-instancia-contra-civ-2322` |
| CIV-2323 | Escrito que pide cautelares sobre el patrimonio tras presentar la demanda de medidas de apoyo | `escrito-pide-cautelares-sobre-patrimonio-tras-civ-2323` |
| CIV-2324 | Escrito entre dos sesiones de la vista de medidas de apoyo que alega hechos y pide prueba | `escrito-entre-dos-sesiones-vista-medidas-apoyo-alega-civ-2324` |
| CIV-2325 | Impugnación de la reposición contra el auto que deniega prueba en apelación sobre medidas de apoyo | `impugnacion-reposicion-contra-auto-deniega-prueba-civ-2325` |
| CIV-2326 | Escrito de oposición a la apelación en el proceso de medidas judiciales de apoyo a la discapacidad | `escrito-oposicion-apelacion-proceso-medidas-judiciales-civ-2326` |
| CIV-2327 | Recurso de apelación contra la sentencia dictada en el proceso de medidas judiciales de apoyo | `recurso-apelacion-contra-sentencia-dictada-proceso-civ-2327` |
| CIV-2328 | Petición de subsanación de la sentencia que omitió fijar el régimen de medidas de apoyo | `peticion-subsanacion-sentencia-omitio-fijar-regimen-civ-2328` |
| CIV-2329 | Recurso de reposición contra el auto que deniega prueba en apelación sobre medidas de apoyo | `recurso-reposicion-contra-auto-deniega-prueba-civ-2329` |
| CIV-2330 | Contestación que se opone a la demanda de medidas de apoyo y propone un curador si se estima | `contestacion-opone-demanda-medidas-apoyo-propone-civ-2330` |
| CIV-2331 | Escrito en segunda instancia del proceso de medidas de apoyo que alega hechos nuevos y pide prueba | `escrito-segunda-instancia-proceso-medidas-apoyo-alega-civ-2331` |
| CIV-2332 | Desistimiento del proceso de medidas de apoyo antes de que se persone la persona afectada | `desistimiento-proceso-medidas-apoyo-antes-persone-civ-2332` |
| CIV-2333 | Otrosí de la demanda de medidas de apoyo que pide designar quién representará a la persona afectada | `otrosi-demanda-medidas-apoyo-pide-designar-quien-civ-2333` |

## Privacidad

Ver `PRIVACY.md`.
