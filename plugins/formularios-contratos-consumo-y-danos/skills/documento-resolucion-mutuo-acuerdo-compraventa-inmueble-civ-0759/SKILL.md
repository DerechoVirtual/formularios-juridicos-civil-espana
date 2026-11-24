---
name: documento-resolucion-mutuo-acuerdo-compraventa-inmueble-civ-0759
description: "Documento de resolución por mutuo acuerdo de una compraventa de inmueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Documento de resolución por mutuo acuerdo de una compraventa de inmueble

> Formulario **CIV-0759** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Documento privado por el que vendedor y comprador de un inmueble, de común acuerdo (mutuo disenso), dejan sin efecto un contrato de compraventa ya firmado, devuelven las cantidades entregadas a cuenta y se otorgan finiquito recíproco.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Documento de resolución por mutuo acuerdo de una compraventa de inmueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Documento de resolución por mutuo acuerdo de una compraventa de inmueble” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:documento-resolucion-mutuo-acuerdo-compraventa-inmueble-civ-0759`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DNI/PASAPORTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] AÑADIR TANTOS PÁRRAFOS IGUALES COMO COMPRADORES HAYA
- [ ] AÑADIR TANTOS PÁRRAFOS IGUALES COMO VENDEDORES HAYA
- [ ] CARGO O APODERADO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN DEL INMUEBLE
- [ ] IDENTIFICACIÓN DEL INMUEBLE Y DATOS REGISTRALES
- [ ] IMPORTE
- [ ] NIF
- [ ] NOMBRE DEL COMPARECIENTE
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] Nº DE PROTOCOLO
- [ ] PODER O TÍTULO DE REPRESENTACIÓN

## Normas que cita el formulario

- art. 1262 CC

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE,

[AÑADIR TANTOS PÁRRAFOS IGUALES COMO VENDEDORES HAYA]

(Datos de LA PARTE VENDEDORA O VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede: solo en caso de estado civil casado/a]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA PARTE VENDEDORA O VENDEDOR.

Y DE OTRA,

[AÑADIR TANTOS PÁRRAFOS IGUALES COMO COMPRADORES HAYA]

(Datos de LA PARTE COMPRADORA O COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede: solo en caso de estado civil casado/a]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA PARTE COMPRADORA O COMPRADOR.

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Si todas las partes actúan en nombre y representación propia: Todos los comparecientes intervienen en su propio nombre y representación.

— Si alguna de las partes actúa en su propio nombre y representación: [NOMBRE DEL COMPARECIENTE] interviene en su propio nombre y representación.

[OPCIONAL — incluir si procede: si alguna de las partes actúa en nombre y representación de persona física o jurídica; repetir tantas veces como representaciones haya]

D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE], en nombre y representación de [ELEGIR: D./Dña. [NOMBRE Y APELLIDOS], persona física, en virtud de [PODER O TÍTULO DE REPRESENTACIÓN] / la sociedad [DENOMINACIÓN SOCIAL], con NIF [NIF], en calidad de [CARGO O APODERADO], en virtud de [TÍTULO DE REPRESENTACIÓN: escritura otorgada ante el Notario [NOMBRE DEL NOTARIO], de fecha [FECHA], nº de protocolo [Nº DE PROTOCOLO]].

Ambas partes, en las respectivas calidades con que actúan, se reconocen mutua y recíprocamente plena capacidad legal para cuanto pasan a manifestar y convenir y, de sus libres y espontáneas voluntades,

MANIFIESTAN

I.- Que suscribieron el [FECHA] contrato privado de compraventa de [ELEGIR: la vivienda / la vivienda y plaza de garaje / el local / otro inmueble], [ELEGIR: en construcción / terminado], sito en [DIRECCIÓN DEL INMUEBLE], identificado como [IDENTIFICACIÓN DEL INMUEBLE Y DATOS REGISTRALES]. Se acompaña copia del citado contrato como anexo al presente documento.

II.- Que [EXPONER EL MOTIVO DE LA RESOLUCIÓN. Ejemplo del modelo original: el vendedor no tiene, en el momento actual, la capacidad económica que tenía en el momento de la firma del contrato, y no puede, en los términos pactados, continuar con la ejecución de las obras de edificación de la citada vivienda].

ACUERDAN

Dar por resuelto y extinguido el referido contrato de compraventa en los términos fijados en los siguientes,

PACTOS

Primero.- Ambas partes, de común y mutuo acuerdo, convienen en RESOLVER y, por tanto, dejan sin efecto legal y forma alguna dicho contrato privado de compraventa que habían suscrito en fecha [FECHA].

Segundo.- El comprador recibe en este acto del vendedor la cantidad de [IMPORTE] euros, importe a que asciende la cantidad entregada a cuenta por el comprador a la fecha del citado contrato.

Tercero.- Con la firma de este documento, y la entrega por la parte vendedora y recepción por la parte compradora de la antedicha cantidad, se acuerda, en su consecuencia, dar por finiquitada y liquidada su relación contractual, sin que en adelante tengan nada que reclamarse como consecuencia del contrato de compraventa que se resuelve, renunciando mutua y expresamente al ejercicio de acciones legales que pudieran derivarse de aquella venta.

Y en prueba de conformidad con todo ello, firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

PARTE VENDEDORA O VENDEDOR: D./Dña. [NOMBRE Y APELLIDOS] PARTE COMPRADORA O COMPRADOR: D./Dña. [NOMBRE Y APELLIDOS]

[FIRMA] [FIRMA]

NOTA EXPLICATIVA

Conforme a constante y reiterada jurisprudencia, el mutuo acuerdo resolutorio o pacto de resolución constituye en nuestro ordenamiento jurídico una causa de extinción de las obligaciones por resolución, disolución o ruptura del vínculo contractual, habiéndose referido a ella, entre otras, las SSTS de 21 de mayo de 1992, 25 de octubre de 1999, rec. 646/1995, 6 de octubre de 2000, rec. 2775/1995, y 30 de diciembre de 2002, rec. 566/2000. Al referirse a la resolución por «mutuo acuerdo» o de «común acuerdo», el mutuo disenso comporta, en la apreciación de la doctrina más autorizada y la jurisprudencia dominante, la constancia de un consentimiento de signo contrario al constitutivo del vínculo contractual (contrarius consensus), esto es, la existencia de un «acuerdo de voluntades», «convenio» o «pacto» de las partes contratantes dirigido a resolver o disolver el contrato celebrado por ellas dejando sin efecto las obligaciones derivadas del mismo; presupone, en otras palabras, la conclusión de «un negocio jurídico extintivo» (STS de 5 de abril de 1979), «la suscripción de común acuerdo de un convenio solutorio y liberatorio del anterior» (STS de 13 de febrero de 1965) o, lo que es igual, la manifestación de un «consentimiento contrario a la existencia del contrato» (STS de 30 de diciembre de 2002, rec. 1956/1997) que, como el consentimiento constitutivo, requiere el encuentro, concurso o entrecruzamiento de las concordes voluntades de sus otorgantes (art. 1262 CC), sea de manera simultánea, sea de forma sucesiva. Lo mismo que el consentimiento constitutivo, el extintivo o resolutorio propio del mutuo disenso puede manifestarse tanto expresa como tácitamente, a través de actos que inequívoca y concluyentemente revelen la común voluntad de los contratantes de dejar sin efecto el negocio concluido, desligándose de las obligaciones por ellos contraídas y renunciando a exigir su efectividad y cumplimiento (STS de 25 de octubre de 1999, rec. 465/1995), pero ese tácito consentimiento ha de quedar probado. El mutuo disenso o común acuerdo de resolución del contrato no está sujeto a forma determinada.
