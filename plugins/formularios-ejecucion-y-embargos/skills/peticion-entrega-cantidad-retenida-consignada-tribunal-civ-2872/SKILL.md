---
name: peticion-entrega-cantidad-retenida-consignada-tribunal-civ-2872
description: "Petición de entrega de la cantidad retenida y consignada en el tribunal tras la vía de apremio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición de entrega de la cantidad retenida y consignada en el tribunal tras la vía de apremio

> Formulario **CIV-2872** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 25-11-2026.

## Qué es

Escrito presentado ante el Tribunal de Instancia solicitando entrega de la cantidad retenida y consignada en el Tribunal tras el procedimiento de apremio seguido en el procedimiento de ejecución forzosa ordinaria.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición de entrega de la cantidad retenida y consignada en el tribunal tras la vía de apremio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición de entrega de la cantidad retenida y consignada en el tribunal tras la vía de apremio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:peticion-entrega-cantidad-retenida-consignada-tribunal-civ-2872`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] COMPLETAR (2 veces)
- [ ] FECHA (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
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

- Junto a «…TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…IBIR] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [NÚMERO]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) REALIZACIÓN DE DINERO EFECTIVO, SALDOS DE CUENTAS CORRIENTES Y OTROS SIMILARES

La realización de los bienes embargados tiene lugar normalmente a través de la subasta judicial mediante la licitación pública ante el órgano jurisdiccional, que recibe las ofertas de dinero de quienes concurran y adjudica el bien al que ofrezca mayor precio.

No obstante, en razón de la naturaleza de los bienes embargados, en ciertos casos, no es preciso acudir a este procedimiento de realización, porque no precisen de ella (cuando lo embargado fuese dinero, sueldos, pensiones o créditos realizables en el acto) o porque tienen establecida una vía específica para realizarlos (títulos valores).

Así se regulan los casos en que se procederá a la entrega directa al ejecutante de los bienes embargados (art. 634) y aquéllos en que se procederá a su venta en mercados secundarios o por un determinado procedimiento de realización para el supuesto de acciones y otras formas de participación sociales (-art. 635-), esto es, medios de realización y enajenaciones distintos de la subasta.

El resto de los bienes o derechos habrán de realizarse mediante el convenio de realización o mediante la enajenación por los procedimientos de enajenación por medio de persona o entidad especializada o por subasta judicial. Este último como medio ordinario, siendo los anteriores alternativos (-art. 636-).

En el art. 634 se enumeran lo los supuestos de realización mediante entrega directa al ejecutante por su valor nominal de bienes embargados.

El número primero hace referencia al pago inmediato o entrega directa al ejecutante del dinero efectivo (moneda de curso legal). Lo normal es que no se llegue a la realización forzosa del dinero, pues si el deudor tiene dinero líquido hará el pago voluntariamente al acreedor evitando intereses y costas.

Frente a la regulación contenida en el art. 1481 de la Ley de Enjuiciamiento Civil de 1881, se omite toda referencia a los sueldos, salarios o pensiones, siguiendo las orientaciones doctrinales que ponen de manifiesto la dificultad de su entrega directa o pago al acreedor ejecutante, dado que los sueldos y pensiones dependen de que el deudor los perciba, de su cuantía (ya que debe calcularse cuál es la cantidad exacta a embargar, -art. 607-) y de su vencimiento periódico, por lo que sólo pueden entregarse en la medida que se vayan abonando, mediante una orden de retención a quien deba pagar al ejecutado para que ponga a disposición del acreedor las cantidades líquidas que resulten embargadas, logrando el cobro en sucesivos períodos de devengo (en este sentido, Fernández López, M. A., Derecho Procesal Civil, t. III, 4.ª ed., Madrid, 1995, págs. 270 y 271 y también en su monografía sobre El juicio ejecutivo, con Rifá Soler, J. M.ª y Valls Gombau, J. F., Madrid, 1997, pág. 812.).

En el segundo, se incluyen los saldos de cuentas corrientes y de otras de inmediata disposición, en sustitución del concepto de créditos realizables en el acto que se emplea en el -art. 1481- de la Ley de Enjuiciamiento Civil de 1881, por lo que parece se podrá realizar la entrega directa no sólo de los saldos de cuentas corrientes o a la vista, cheques bancarios, talones vencidos, sino también, certificados de depósito, pagarés, cédulas y otros instrumentos de ahorro que, aunque en rigor no podrían calificarse como créditos realizables en el acto, son créditos de seguro cobro y la diferencia entre su valor actual -mientras aún no han vencido- y su valor nominal pueden compensarse mediante un sencillo cómputo de intereses (Fernández López, M. A., Derecho Procesal Civil, t. III, Madrid, 1995).

Lógicamente, lo que habrá de entregarse al ejecutante es el saldo y no la titularidad de los derechos que el ejecutado tenga sobre la cuenta, por lo que el órgano jurisdiccional deberá llevar a cabo todas las actuaciones necesarias para que el ejecutante reciba el dinero depositado; por ejemplo, expedir requerimiento a las entidades financieras para que se entregue el importe del saldo al ejecutante directamente o se consigne en la cuenta del Tribunal que a su vez lo entregará al ejecutante (Franco Arias, J., «Comentarios sobre el procedimiento de apremio del Anteproyecto de Ley de Enjuiciamiento Civil», en Presente y futuro del proceso civil, obra colectiva).

El número tercero ordena la entrega cuando se trate de divisas convertibles, previa conversión, en su caso. Supuesto de difícil aplicabilidad, dada la dificultad de poder encontrar moneda extranjera o divisas en poder del ejecutado conforme al régimen de control de cambios.

A diferencia del 1481, no se contempla cuando ha de procederse a realizar la conversión (cuando se condene a la entrega en una determinada moneda y se haya embargado otra distinta, aunque sea nacional) y la posibilidad de que el ejecutante solicite entre su conversión o ser pagado en la moneda embargada sin necesidad de conversión.

El número cuarto ordena la entrega al ejecutante, de cualquier otro bien cuyo valor facial nominal coincida con su valor de mercado, o que, aunque inferior, el acreedor acepte la entrega del bien por su valor nominal (en el trámite de Ponencia se llega a un texto transaccional por el que se sustituye la dicción referida al valor facial al que se refería el Proyecto por la de valor nominal); lo que ha sido criticado, por contrario al -articulo 18.2- de la Ley Orgánica del Poder Judicial, al obligar al ejecutante a aceptar cualquier otro bien cuyo valor facial coincida con su valor de mercado. En estos casos, debería el Tribunal realizar la conversión y con el dinero obtenido satisfacer al ejecutante. Unicamente, sería admisible que, como posibilidad subsidiaria, se estableciera, en estos casos, que si el ejecutante solicita la adjudicación directa, pudiera prescindirse de la conversión y procederse a la entrega del bien al ejecutante, compensándose hasta donde ello fuera posible la deuda con el valor del bien (si el valor del bien fuera superior, el ejecutante debería consignar la diferencia) (Franco Arias, J., «Comentarios sobre el procedimiento de apremio del Anteproyecto de Ley de Enjuiciamiento Civil», en Presente y futuro del proceso civil, obra colectiva).

Cuando se trate de saldos favorables en cuenta, con vencimiento diferido (saldos de cuentas bancarias respecto de los que no cabe la inmediata disposición de sus fondos, los créditos que el ejecutado tenga frente al Estado y demás entidades públicas, en tanto son créditos de seguro cobro) la subasta no parece el mecanismo más adecuado para la realización de los derechos que ostente el ejecutado en relación a dichas cuentas. El propio tribunal adoptará las medidas oportunas para lograr su cobro, pudiendo designar un administrador cuando fuere conveniente o necesario para su realización, al estimarse, en definitiva que se tratan de créditos directamente realizables. Este apartado fue introducido en el trámite de Informe de la Ponencia a la Comisión de Justicia e Interior del Congreso de los Diputados, como consecuencia de la enmienda 532 del GP Socialista.

Igualmente, en el trámite de Informe de la Ponencia a la Comisión de Justicia e Interior del Congreso de los Diputados, como consecuencia de la enmienda 1320 del GP Catalán CiU, se incorporó el supuesto específico de ejecución de sentencias que condenen al pago de las cantidades debidas por incumplimiento de contratos de venta a plazos de bienes muebles, en las que el ejecutante podrá solicitar la entrega inmediata del bien o bienes muebles vendidos o financiados a plazos por el valor que resulte de las tablas o índices referenciales de depreciación que se hubieren establecido en el contrato.


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
