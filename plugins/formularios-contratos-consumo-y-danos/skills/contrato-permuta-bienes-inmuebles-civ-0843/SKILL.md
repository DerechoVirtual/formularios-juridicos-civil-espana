---
name: contrato-permuta-bienes-inmuebles-civ-0843
description: "Contrato de permuta de bienes inmuebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de permuta de bienes inmuebles

> Formulario **CIV-0843** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de permuta de dos inmuebles (aquí, un solar y una casa) entre dos partes, con compensación de la diferencia de valor y derecho de tanteo recíproco para el caso de que alguna de ellas venda en el futuro el bien recibido. Regula estado de los bienes, entrega de documentación, notificaciones, protección de datos, gastos, elevación a escritura pública y fuero.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de permuta de bienes inmuebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de permuta de bienes inmuebles” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-permuta-bienes-inmuebles-civ-0843`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] LINDERO (7 veces)
- [ ] DNI/NIE/PASAPORTE (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] CALLE (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] FECHA (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] CLASE DE TÍTULO (2 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] AÑO
- [ ] CLASE DE ESCRITURA
- [ ] DATOS REGISTRALES: TOMO, LIBRO, FOLIO, FINCA
- [ ] DATOS REGISTRALES: TOMO, LIBRO, FOLIO, FINCA, INSCRIPCIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO DE CADA PARTE A EFECTOS DE NOTIFICACIONES
- [ ] DÍA
- [ ] LOCALIDAD, CALLE Y NÚMERO
- [ ] MES
- [ ] NIF
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] PLAZO

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…cia del Tribunal Supremo (Sala de lo Civil, Sección 1.ª) de 27 de junio de 2007.»: el original califica el contrato de mercantil (cláusula Octava). La permuta entre particulares de inmuebles es, en general, un contrato civil (arts. 1538 y ss. del Código Civil); comprobar la calificación aplicable al caso. La referencia a los intereses de la Ley 3/2004 se ha dejado sin la mención al Ministerio de Economía y Hacienda, que ya no fija el tipo. Formulario adaptado a la reforma de la LO 1/2025.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO: La permuta de bienes inmuebles es un contrato por el que una parte transmite la propiedad de un bien inmueble a cambio de recibir como contraprestación otro bien inmueble (la permuta mercantil, con ánimo de lucrarse en la reventa, se regula en el artículo 346 del Código de Comercio). En cuanto a los intervinientes, si se trata de una persona física que interviene en su propio nombre y derecho es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea legal o convencional. En el mismo sentido si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran. Respecto a los pagos no satisfechos puntualmente, recuérdese que la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor sólo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones se devengará el interés de demora contractual o el fijado legalmente. En relación con la efectividad de la cláusula de reserva de dominio y su oponibilidad a terceros, hay que tener en cuenta lo dispuesto en el artículo 15 de la Ley 28/1998, de 13 de julio, de Venta a Plazos de Bienes Muebles. En caso de resolución del contrato por causa imputable a la parte compradora, tener en cuenta que la conceptuación de las arras penales por el artículo 1152 del Código Civil conduce a afirmar que, salvo que las partes acuerden lo contrario, la satisfacción de la pena sustituye a la indemnización de daños y abono de intereses en caso de falta de cumplimiento, desempeñando así una función propiamente liquidatoria; en el mismo sentido, la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1.ª) de 27 de junio de 2007.


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

DE UNA PARTE, (Datos de UNA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/NIE/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/NIE/PASAPORTE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

[Repetir el bloque anterior si hay varias personas en esta parte.]

Y DE OTRA, (Datos de la OTRA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/NIE/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/NIE/PASAPORTE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

[Repetir el bloque anterior si hay varias personas en esta parte.]

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y representación. [Repetir por cada parte que actúe en nombre propio.]

— D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de: [ELEGIR UNA DE LAS DOS SIGUIENTES:]

— (Si se trata de persona física) D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado/a en [DOMICILIO], con DNI/Pasaporte número [DNI/NIE/PASAPORTE].

— (Si se trata de persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD, CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [LOCALIDAD], [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que causó inscripción en el Registro Mercantil de [LOCALIDAD], [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA].

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PERMUTA y, a tal fin,

EXPONEN

I. Que D./Dña. [NOMBRE Y APELLIDOS] es propietario de un solar sito en la calle [CALLE] de [LOCALIDAD], de una superficie de [SUPERFICIE], lindante por la derecha con [LINDERO], por la izquierda con [LINDERO], al fondo con [LINDERO] y por el frente con la calle [CALLE]; dicho solar pertenece a D./Dña. [NOMBRE Y APELLIDOS] en virtud de la escritura de [CLASE DE TÍTULO] autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], el día [FECHA], se encuentra libre de cargas y gravámenes, y obra inscrito en el Registro de la Propiedad de [LOCALIDAD] al [DATOS REGISTRALES: TOMO, LIBRO, FOLIO, FINCA, INSCRIPCIÓN].

II. Que D./Dña. [NOMBRE Y APELLIDOS] es propietario de una casa sita en la calle [CALLE], de una superficie de [SUPERFICIE] metros cuadrados, lindante por la derecha con [LINDERO], a la izquierda con [LINDERO], por el fondo con [LINDERO] y por el frente con [LINDERO]; el referido edificio pertenece a D./Dña. [NOMBRE Y APELLIDOS] por título de [CLASE DE TÍTULO], en virtud de escritura de [CLASE DE ESCRITURA] autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] el día [FECHA]; la finca carece de cargas y gravámenes, y se encuentra inscrita en el Registro de la Propiedad de [LOCALIDAD] al [DATOS REGISTRALES: TOMO, LIBRO, FOLIO, FINCA].

III. Que estando interesadas ambas partes en intercambiar ambos inmuebles, formalizan el presente contrato en base a las siguientes

CLÁUSULAS

Primera.- Objeto

D./Dña. [NOMBRE Y APELLIDOS] cede a D./Dña. [NOMBRE Y APELLIDOS] el inmueble descrito en el Expositivo I del presente documento, libre de cargas y gravámenes, y al corriente de pago de impuestos, contribuciones y arbitrios. El valor de dicha finca se valora de mutuo acuerdo en la cantidad de [IMPORTE] euros. En contraprestación, D./Dña. [NOMBRE Y APELLIDOS] transmite a D./Dña. [NOMBRE Y APELLIDOS] el pleno dominio del inmueble descrito en el Expositivo II, asimismo al corriente de pago de impuestos, contribuciones y gravámenes, y libre de cargas. La finca es valorada de mutuo acuerdo por los comparecientes en la cantidad de [IMPORTE] euros.

[OPCIONAL — incluir si procede (si existe diferencia de precio entre los bienes)]

Segunda.- Diferencia de precio

En atención a la diferencia de valor existente entre ambos inmuebles, D./Dña. [NOMBRE Y APELLIDOS] abona en este acto a D./Dña. [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, confiriendo éste la más eficaz carta de pago, a través del presente documento.

Tercera.- Estado de los bienes

Los contratantes declaran conocer que los bienes inmuebles que se permutan en este acto se encuentran en buen estado de conservación y funcionamiento; no obstante ello, ambos se obligan al saneamiento por vicios ocultos existentes al momento de la transferencia, conforme a ley.

Cuarta.- Entrega

Es obligación de los permutantes entregarse mutuamente los documentos relativos a la propiedad del inmueble que en este acto cada uno transfiere, así como los recibos debidamente cancelados por concepto de [CONCEPTOS: por ejemplo, impuestos y suministros].

Quinta.- Tanteo

En este contrato las partes establecen un derecho de tanteo sobre los bienes permutados, si llegase el caso que alguno de los contratantes en un futuro decidiese vender el bien ahora adquirido mediante esta permuta. Para ello se lo comunicará a la otra parte poniéndola en antecedentes de la cantidad que desea por el mismo, y si transcurridos [PLAZO] desde su notificación no acepta la venta, podrá vender el bien libremente a una tercera persona por la misma cantidad, pero si dicha cantidad fuese inferior vuelve a estar en la obligación de comunicarlo y ofrecerlo nuevamente al permutante para que decida sobre su adquisición por el mismo período de tiempo que en la vez inicial.

Sexta.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato: [DOMICILIO DE CADA PARTE A EFECTOS DE NOTIFICACIONES].

Séptima.- Protección de datos personales

Ambas partes reconocen que la legislación sobre protección de datos personales (Reglamento (UE) 2016/679, RGPD, y Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento por cualquiera de los contratantes de las obligaciones establecidas en la normativa vigente sobre tratamiento de datos de carácter personal generará una indemnización en favor de la contraparte de [IMPORTE] euros.

Octava.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

Novena.- Gastos y formalización

Ambas partes pactan y aceptan que todos los gastos que se deriven de este contrato, así como los futuros trámites legales preceptivos, serán hechos efectivos por partes iguales, acordando que la elevación a escritura pública se llevará a efecto en el plazo de [Nº] meses.

Décima.- Fuero competente

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LA OTRA:]

— Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

— Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

[Si se suprime la cláusula Segunda, renumerar las siguientes.]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Firmado: D./Dña. [NOMBRE Y APELLIDOS]
