# Hijos: custodia, visitas, alimentos, filiación y adopción

> Plugin de Claude Code `formularios-hijos-custodia-y-alimentos` · **159 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los asuntos de los hijos: guarda y custodia, régimen de visitas y estancias, alimentos y su modificación, patria potestad y desacuerdos en su ejercicio, filiación y paternidad, adopción y acogimiento, sustracción internacional de menores y protección de menores.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 159 está al final):

- **Demandas, peticiones y solicitudes iniciales** (61). Por ejemplo: Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación; Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor; Demanda de modificación de medidas por incumplimiento reiterado del régimen de visitas.
- **Contestaciones, oposiciones y alegaciones** (23). Por ejemplo: Contestación a la reconvención que pide alimentos para un hijo mayor de edad; Contestación a la reconvención de alimentos para un hijo mayor de edad según el Derecho catalán; Contestación a la demanda de modificación de medidas que pide la custodia compartida.
- **Recursos** (2). Por ejemplo: Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad; Recurso de apelación que alega la caducidad de la acción de impugnación de paternidad matrimonial.
- **Contratos, pactos y cláusulas** (4). Por ejemplo: Contrato de alimentos a favor de hijo con patria potestad prorrogada; Compraventa autorizada judicialmente de la vivienda de un menor para comprar otra con hipoteca; Contrato privado de venta de la vivienda de un menor por su madre con autorización judicial.
- **Estatutos, actas, certificaciones y escrituras** (17). Por ejemplo: Acta de inicio de un procedimiento de mediación familiar; Acta inicial o contrato de mediación familiar según la normativa aragonesa; Acta final de mediación familiar sin acuerdos según la normativa andaluza.
- **Comunicaciones, requerimientos y cartas** (16). Por ejemplo: Solicitud conjunta de mediación familiar presentada por ambas partes; Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos; Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC).
- **Escritos de trámite y otros** (36). Por ejemplo: Escrito conjunto para homologar un acuerdo de mediación familiar en un proceso de filiación; Escrito pidiendo levantar la suspensión del proceso porque la mediación familiar terminó sin acuerdo; Otrosí pidiendo la audiencia del menor en demanda de modificación de medidas sobre custodia.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de modificación de medidas para establecer la custodia compartida»
   - «Demanda de reclamación de alimentos para un hijo mayor de edad»
   - «Demanda de reclamación de la paternidad no matrimonial»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-hijos-custodia-y-alimentos:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-hijos-custodia-y-alimentos:solicitud-conjunta-mediacion-familiar-presentada-ambas-civ-0002`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 9.729 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-hijos-custodia-y-alimentos@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-hijos-custodia-y-alimentos@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-hijos-custodia-y-alimentos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (159)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0002 | Solicitud conjunta de mediación familiar presentada por ambas partes | `solicitud-conjunta-mediacion-familiar-presentada-ambas-civ-0002` |
| CIV-0003 | Acta de inicio de un procedimiento de mediación familiar | `acta-inicio-procedimiento-mediacion-familiar-civ-0003` |
| CIV-0006 | Escrito conjunto para homologar un acuerdo de mediación familiar en un proceso de filiación | `escrito-conjunto-homologar-acuerdo-mediacion-familiar-civ-0006` |
| CIV-0007 | Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación | `solicitud-mediacion-familiar-parte-cumplimiento-pacto-civ-0007` |
| CIV-0008 | Escrito pidiendo levantar la suspensión del proceso porque la mediación familiar terminó sin acuerdo | `escrito-pidiendo-levantar-suspension-proceso-porque-civ-0008` |
| CIV-0009 | Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos | `solicitud-aprobacion-judicial-acuerdo-mediacion-sobre-civ-0009` |
| CIV-0013 | Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor | `demanda-contenciosa-modificacion-medidas-reducir-civ-0013` |
| CIV-0014 | Demanda de modificación de medidas por incumplimiento reiterado del régimen de visitas | `demanda-modificacion-medidas-incumplimiento-reiterado-civ-0014` |
| CIV-0015 | Acta inicial o contrato de mediación familiar según la normativa aragonesa | `acta-inicial-contrato-mediacion-familiar-segun-civ-0015` |
| CIV-0016 | Acta final de mediación familiar sin acuerdos según la normativa andaluza | `acta-final-mediacion-familiar-sin-acuerdos-segun-civ-0016` |
| CIV-0017 | Acta final de mediación familiar con acuerdos según la normativa aragonesa | `acta-final-mediacion-familiar-acuerdos-segun-normativa-civ-0017` |
| CIV-0018 | Acta inicial o contrato de mediación familiar según la normativa andaluza | `acta-inicial-contrato-mediacion-familiar-segun-civ-0018` |
| CIV-0019 | Acta final de mediación familiar sin acuerdos según la normativa aragonesa | `acta-final-mediacion-familiar-sin-acuerdos-segun-civ-0019` |
| CIV-0020 | Acta final de mediación familiar con acuerdos según la normativa andaluza | `acta-final-mediacion-familiar-acuerdos-segun-normativa-civ-0020` |
| CIV-0022 | Acta final de mediación familiar que concluye por posturas irreconciliables de las partes | `acta-final-mediacion-familiar-concluye-posturas-civ-0022` |
| CIV-0023 | Acta final de mediación familiar que termina sin acuerdo | `acta-final-mediacion-familiar-termina-sin-acuerdo-civ-0023` |
| CIV-0027 | Acta inicial o contrato de mediación familiar sobre alimentos de un hijo mayor de edad | `acta-inicial-contrato-mediacion-familiar-sobre-civ-0027` |
| CIV-0028 | Acta final de mediación familiar con acuerdo sobre la pensión de alimentos | `acta-final-mediacion-familiar-acuerdo-sobre-pension-civ-0028` |
| CIV-0030 | Contestación a la reconvención que pide alimentos para un hijo mayor de edad | `contestacion-reconvencion-pide-alimentos-hijo-mayor-civ-0030` |
| CIV-0033 | Contestación a la reconvención de alimentos para un hijo mayor de edad según el Derecho catalán | `contestacion-reconvencion-alimentos-hijo-mayor-edad-civ-0033` |
| CIV-0044 | Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC) | `solicitud-decision-judicial-ante-desacuerdo-padres-civ-0044` |
| CIV-0045 | Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores | `solicitud-jurisdiccion-voluntaria-abuelos-asuman-civ-0045` |
| CIV-0066 | Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar | `solicitud-declaracion-gasto-extraordinario-tratamiento-civ-0066` |
| CIV-0067 | Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011) | `demanda-modificacion-medidas-pedir-custodia-compartida-civ-0067` |
| CIV-0068 | Contestación a la demanda de modificación de medidas que pide la custodia compartida | `contestacion-demanda-modificacion-medidas-pide-civ-0068` |
| CIV-0070 | Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida | `demanda-modificacion-medidas-mutuo-acuerdo-establecer-civ-0070` |
| CIV-0071 | Otrosí pidiendo la audiencia del menor en demanda de modificación de medidas sobre custodia | `otrosi-pidiendo-audiencia-menor-demanda-modificacion-civ-0071` |
| CIV-0072 | Escrito pidiendo alzar el embargo por extinción de la obligación de pagar alimentos | `escrito-pidiendo-alzar-embargo-extincion-obligacion-civ-0072` |
| CIV-0073 | Escrito inicial para hacer valer el asentimiento exigido en la adopción | `escrito-inicial-hacer-valer-asentimiento-exigido-civ-0073` |
| CIV-0077 | Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán) | `demanda-oposicion-declaracion-administrativa-desamparo-civ-0077` |
| CIV-0078 | Escrito inicial de oposición a la resolución de desamparo de un menor (Derecho catalán) | `escrito-inicial-oposicion-resolucion-desamparo-menor-civ-0078` |
| CIV-0079 | Demanda de juicio ordinario para recuperar la patria potestad | `demanda-juicio-ordinario-recuperar-patria-potestad-civ-0079` |
| CIV-0083 | Demanda de mutuo acuerdo de parejas de hecho con hijos menores | `demanda-mutuo-acuerdo-parejas-hecho-hijos-menores-civ-0083` |
| CIV-0084 | Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer | `solicitud-medidas-sobre-hijos-menores-ante-seccion-civ-0084` |
| CIV-0090 | Solicitud de derecho de visita de un menor a través de la Autoridad Central | `solicitud-derecho-visita-menor-traves-autoridad-central-civ-0090` |
| CIV-0095 | Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos | `demanda-exigir-cumplimiento-regimen-visitas-nietos-civ-0095` |
| CIV-0103 | Demanda de restitución de menores según el Convenio hispano-marroquí de 1997 | `demanda-restitucion-menores-segun-convenio-hispano-civ-0103` |
| CIV-0104 | Solicitud de devolución de un menor a través de la Autoridad Central | `solicitud-devolucion-menor-traves-autoridad-central-civ-0104` |
| CIV-0105 | Solicitud a la Autoridad Central de restitución de menores (Convenio hispano-marroquí de 1997) | `solicitud-autoridad-central-restitucion-menores-civ-0105` |
| CIV-0111 | Contestación del Ministerio Fiscal a la demanda de reclamación de filiación no matrimonial | `contestacion-ministerio-fiscal-demanda-reclamacion-civ-0111` |
| CIV-0112 | Contestación a la reclamación de filiación de la madre con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-madre-impugnacion-civ-0112` |
| CIV-0115 | Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-presunto-padre-civ-0115` |
| CIV-0116 | Contestación a la reclamación de filiación no matrimonial del hijo mayor de edad | `contestacion-reclamacion-filiacion-no-matrimonial-hijo-civ-0116` |
| CIV-0117 | Contestación a la reclamación de filiación del hijo con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-hijo-impugnacion-civ-0117` |
| CIV-0118 | Contestación del Ministerio Fiscal a la demanda de impugnación de filiación matrimonial | `contestacion-ministerio-fiscal-demanda-impugnacion-civ-0118` |
| CIV-0125 | Demanda de alimentos de un hijo contra sus padres | `demanda-alimentos-hijo-contra-padres-civ-0125` |
| CIV-0126 | Demanda de alimentos entre hermanos (Derecho civil catalán) | `demanda-alimentos-entre-hermanos-derecho-civil-catalan-civ-0126` |
| CIV-0127 | Contestación a la reclamación de filiación de la madre que pide prueba biológica | `contestacion-reclamacion-filiacion-madre-pide-prueba-civ-0127` |
| CIV-0131 | Escrito para continuar el procedimiento de filiación contra los herederos del demandado fallecido | `escrito-continuar-procedimiento-filiacion-contra-civ-0131` |
| CIV-0136 | Solicitud de la familia acogedora a la entidad pública para cesar el acogimiento | `solicitud-familia-acogedora-entidad-publica-cesar-civ-0136` |
| CIV-0137 | Demanda contra la declaración de no idoneidad para adoptar | `demanda-contra-declaracion-no-idoneidad-adoptar-civ-0137` |
| CIV-0139 | Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar | `escrito-sucinto-inicial-oposicion-declaracion-no-civ-0139` |
| CIV-0140 | Escrito para recuperar la guarda del menor asumida temporalmente por la entidad pública | `escrito-recuperar-guarda-menor-asumida-temporalmente-civ-0140` |
| CIV-0142 | Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán) | `demanda-mutuo-acuerdo-sobre-guarda-custodia-compartida-civ-0142` |
| CIV-0143 | Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor | `contestacion-demanda-guarda-visitas-alimentos-menores-civ-0143` |
| CIV-0146 | Demanda de extinción de la pensión alimenticia del hijo mayor por su matrimonio | `demanda-extincion-pension-alimenticia-hijo-mayor-civ-0146` |
| CIV-0148 | Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo | `demanda-reduccion-pension-alimenticia-nacimiento-nuevo-civ-0148` |
| CIV-0158 | Escrito para promover la adopción del menor acogido durante más de un año | `escrito-promover-adopcion-menor-acogido-durante-mas-ano-civ-0158` |
| CIV-0159 | Escrito para promover la adopción por el tutor | `escrito-promover-adopcion-tutor-civ-0159` |
| CIV-0160 | Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral | `escrito-promover-adopcion-pariente-tercer-ulterior-civ-0160` |
| CIV-0161 | Plan de parentalidad de mutuo acuerdo con custodia compartida | `plan-parentalidad-mutuo-acuerdo-custodia-compartida-civ-0161` |
| CIV-0162 | Plan de parentalidad de mutuo acuerdo con guarda individual | `plan-parentalidad-mutuo-acuerdo-guarda-individual-civ-0162` |
| CIV-0165 | Demanda de aumento de la pensión alimenticia por incremento de los gastos de los hijos | `demanda-aumento-pension-alimenticia-incremento-gastos-civ-0165` |
| CIV-0168 | Escrito pidiendo prohibir la salida de un menor al extranjero | `escrito-pidiendo-prohibir-salida-menor-extranjero-civ-0168` |
| CIV-0171 | Demanda de modificación del régimen de visitas con suspensión provisional | `demanda-modificacion-regimen-visitas-suspension-civ-0171` |
| CIV-0172 | Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña) | `demanda-modificacion-medidas-modificacion-provisional-civ-0172` |
| CIV-0174 | Demanda contra la declaración de desamparo por razones de fondo | `demanda-contra-declaracion-desamparo-razones-fondo-civ-0174` |
| CIV-0175 | Demanda contra la declaración de desamparo por defectos formales | `demanda-contra-declaracion-desamparo-defectos-formales-civ-0175` |
| CIV-0176 | Escrito inicial de oposición al desamparo presentado por el guardador de hecho | `escrito-inicial-oposicion-desamparo-presentado-civ-0176` |
| CIV-0177 | Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil | `demanda-rectificar-error-inscripcion-nacimiento-civ-0177` |
| CIV-0181 | Demanda de juicio verbal de alimentos del hijo mayor de edad | `demanda-juicio-verbal-alimentos-hijo-mayor-edad-civ-0181` |
| CIV-0183 | Escrito del progenitor pidiendo a la entidad pública que asuma temporalmente la guarda del menor | `escrito-progenitor-pidiendo-entidad-publica-asuma-civ-0183` |
| CIV-0185 | Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad | `solicitud-medidas-judiciales-desacuerdo-ejercicio-civ-0185` |
| CIV-0186 | Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña) | `demanda-contenciosa-medidas-parentales-alimentos-civ-0186` |
| CIV-0189 | Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán) | `solicitud-autorizacion-judicial-vender-bienes-hijos-civ-0189` |
| CIV-0190 | Escrito pidiendo plazo para formular demanda en el procedimiento de asentimiento a la adopción | `escrito-pidiendo-plazo-formular-demanda-procedimiento-civ-0190` |
| CIV-0191 | Solicitud de medidas cautelares en un proceso de filiación | `solicitud-medidas-cautelares-proceso-filiacion-civ-0191` |
| CIV-0193 | Escrito de contestación a la demanda en proceso sobre menores | `escrito-contestacion-demanda-proceso-sobre-menores-civ-0193` |
| CIV-0210 | Escritura de reconocimiento de filiación de un hijo mayor de edad | `escritura-reconocimiento-filiacion-hijo-mayor-edad-civ-0210` |
| CIV-0214 | Autorización notarial de viaje de un menor | `autorizacion-notarial-viaje-menor-civ-0214` |
| CIV-0217 | Escritura de consentimiento para el ejercicio de la patria potestad | `escritura-consentimiento-ejercicio-patria-potestad-civ-0217` |
| CIV-0218 | Escritura por la que se revoca la emancipación | `escritura-revoca-emancipacion-civ-0218` |
| CIV-0219 | Escritura de emancipación de un menor | `escritura-emancipacion-menor-civ-0219` |
| CIV-0227 | Escritura de emancipación por concesión de quienes ejercen la patria potestad | `escritura-emancipacion-concesion-quienes-ejercen-civ-0227` |
| CIV-0240 | Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán) | `demanda-guarda-custodia-alimentos-hijos-menores-civ-0240` |
| CIV-0251 | Solicitud de modificar el régimen de visitas por incumplimiento del otro progenitor | `solicitud-modificar-regimen-visitas-incumplimiento-civ-0251` |
| CIV-0255 | Solicitud del representante legal del menor a la entidad pública para cesar el acogimiento | `solicitud-representante-legal-menor-entidad-publica-civ-0255` |
| CIV-0257 | Demanda de guarda y custodia y alimentos de hijos menores | `demanda-guarda-custodia-alimentos-hijos-menores-civ-0257` |
| CIV-0261 | Escrito para exigir el asentimiento necesario en la adopción | `escrito-exigir-asentimiento-necesario-adopcion-civ-0261` |
| CIV-0264 | Demanda de reclamación de filiación paterna | `demanda-reclamacion-filiacion-paterna-civ-0264` |
| CIV-0265 | Demanda de impugnación de la filiación paterna | `demanda-impugnacion-filiacion-paterna-civ-0265` |
| CIV-0266 | Escrito de contestación a la demanda de reclamación o impugnación de paternidad | `escrito-contestacion-demanda-reclamacion-impugnacion-civ-0266` |
| CIV-0278 | Demanda de juicio ordinario de privación de la patria potestad | `demanda-juicio-ordinario-privacion-patria-potestad-civ-0278` |
| CIV-0279 | Encabezamiento de demanda con procurador y padres como representantes de hijo menor | `encabezamiento-demanda-procurador-padres-como-civ-0279` |
| CIV-0280 | Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores | `demanda-alimentos-progenitor-contra-otro-nombre-hijos-civ-0280` |
| CIV-0281 | Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores | `contestacion-fiscal-demanda-oposicion-resolucion-civ-0281` |
| CIV-0287 | Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores | `contestacion-demanda-alimentos-progenitor-contra-otro-civ-0287` |
| CIV-0289 | Solicitud de cumplimiento del régimen de visitas fijado en la sentencia de separación | `solicitud-cumplimiento-regimen-visitas-fijado-civ-0289` |
| CIV-0290 | Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio | `demanda-modificacion-medidas-incumplimiento-reiterado-civ-0290` |
| CIV-0298 | Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente | `demanda-reconocimiento-necesidad-asentimiento-adopcion-civ-0298` |
| CIV-0299 | Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos | `contestacion-demanda-modificacion-medidas-sobre-civ-0299` |
| CIV-0322 | Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto | `contestacion-demanda-sobre-comunicacion-visitas-civ-0322` |
| CIV-0329 | Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente | `demanda-oposicion-resolucion-administrativa-proteccion-civ-0329` |
| CIV-0334 | Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos | `solicitud-actualizar-pension-alimentos-segun-ipc-civ-0334` |
| CIV-0338 | Solicitud de ejecución para que el ejecutado entregue los hijos a la madre custodia | `solicitud-ejecucion-ejecutado-entregue-hijos-madre-civ-0338` |
| CIV-0340 | Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional | `demanda-contenciosa-modificacion-medidas-sobre-guarda-civ-0340` |
| CIV-0341 | Demanda contenciosa de modificación de medidas para aumentar la pensión de alimentos del hijo menor | `demanda-contenciosa-modificacion-medidas-aumentar-civ-0341` |
| CIV-0347 | Escrito inicial de oposición a resolución administrativa de protección de menores | `escrito-inicial-oposicion-resolucion-administrativa-civ-0347` |
| CIV-0352 | Reconocimiento y ejecución en España de sentencia extranjera de alimentos (demanda) | `reconocimiento-ejecucion-espana-sentencia-extranjera-civ-0352` |
| CIV-0358 | Contrato de alimentos a favor de hijo con patria potestad prorrogada | `contrato-alimentos-favor-hijo-patria-potestad-civ-0358` |
| CIV-0359 | Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor | `demanda-juicio-verbal-sobre-comunicacion-visitas-civ-0359` |
| CIV-0360 | Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial | `demanda-juicio-verbal-sobre-regimen-visitas-hijo-menor-civ-0360` |
| CIV-0361 | Demanda de juicio ordinario para extinguir una adopción | `demanda-juicio-ordinario-extinguir-adopcion-civ-0361` |
| CIV-0367 | Demanda de juicio verbal para que el progenitor pague alimentos al hijo | `demanda-juicio-verbal-progenitor-pague-alimentos-hijo-civ-0367` |
| CIV-0368 | Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado | `demanda-madre-reclamando-filiacion-no-matrimonial-hijo-civ-0368` |
| CIV-0369 | Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita | `demanda-fiscal-impugnando-reconocimiento-paternidad-civ-0369` |
| CIV-0370 | Contestación del demandado como padre a la demanda de filiación no matrimonial | `contestacion-demandado-como-padre-demanda-filiacion-no-civ-0370` |
| CIV-0371 | Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación | `demanda-padre-reclamando-filiacion-hijo-menor-difunto-civ-0371` |
| CIV-2196 | Demanda para impugnar la filiación matrimonial determinada por reconocimiento | `demanda-impugnar-filiacion-matrimonial-determinada-civ-2196` |
| CIV-2197 | Otrosí que pide alimentos provisionales urgentes en la demanda de reclamación de filiación | `otrosi-pide-alimentos-provisionales-urgentes-demanda-civ-2197` |
| CIV-2204 | Demanda de los parientes de un menor en acogimiento contra la familia acogedora para fijar visitas | `demanda-parientes-menor-acogimiento-contra-familia-civ-2204` |
| CIV-2225 | Otrosí que pide pericial psicológica del menor en la demanda de relación con abuelos o allegados | `otrosi-pide-pericial-psicologica-menor-demanda-civ-2225` |
| CIV-2227 | Otrosí que pide oír al menor en la demanda de relación con abuelos, parientes o allegados | `otrosi-pide-oir-menor-demanda-relacion-abuelos-civ-2227` |
| CIV-2228 | Contestación que pide que las visitas de los abuelos sean en presencia del progenitor demandado | `contestacion-pide-visitas-abuelos-sean-presencia-civ-2228` |
| CIV-2236 | Demanda de la madre que impugna la paternidad matrimonial y reclama la no matrimonial de su hijo | `demanda-madre-impugna-paternidad-matrimonial-reclama-civ-2236` |
| CIV-2237 | Demanda del hijo mayor de edad que impugna su paternidad no matrimonial | `demanda-hijo-mayor-edad-impugna-paternidad-no-civ-2237` |
| CIV-2240 | Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad | `recurso-apelacion-valoracion-negativa-prueba-biologica-civ-2240` |
| CIV-2244 | Demanda del padre biológico que impugna la paternidad matrimonial y reclama la suya sobre un menor | `demanda-padre-biologico-impugna-paternidad-matrimonial-civ-2244` |
| CIV-2248 | Escrito entre dos sesiones de la vista en juicio de filiación que alega hechos nuevos y pide prueba | `escrito-entre-dos-sesiones-vista-juicio-filiacion-civ-2248` |
| CIV-2249 | Escrito del demandado que acepta someterse a la prueba biológica de paternidad | `escrito-demandado-acepta-someterse-prueba-biologica-civ-2249` |
| CIV-2250 | Escrito en segunda instancia del juicio de filiación que alega hechos nuevos y pide prueba | `escrito-segunda-instancia-juicio-filiacion-alega-civ-2250` |
| CIV-2254 | Demanda de un interesado legítimo para declarar la filiación matrimonial por posesión de estado | `demanda-interesado-legitimo-declarar-filiacion-civ-2254` |
| CIV-2255 | Demanda de ejecución para que el progenitor custodio cumpla el régimen de visitas entregando al hijo | `demanda-ejecucion-progenitor-custodio-cumpla-regimen-civ-2255` |
| CIV-2257 | Contestación a la demanda que impugna el reconocimiento de paternidad extramatrimonial | `contestacion-demanda-impugna-reconocimiento-paternidad-civ-2257` |
| CIV-2258 | Contestación del demandado a la demanda de impugnación de la paternidad matrimonial | `contestacion-demandado-demanda-impugnacion-paternidad-civ-2258` |
| CIV-2264 | Demanda del hijo mayor de edad que reclama la paternidad no matrimonial | `demanda-hijo-mayor-edad-reclama-paternidad-no-civ-2264` |
| CIV-2266 | Escrito de oposición a la apelación contra la sentencia dictada en un juicio de filiación | `escrito-oposicion-apelacion-contra-sentencia-dictada-civ-2266` |
| CIV-2268 | Contestación que se opone a acumular la reclamación de legítima a la de paternidad no matrimonial | `contestacion-opone-acumular-reclamacion-legitima-civ-2268` |
| CIV-2272 | Contestación a la demanda que impugna la paternidad matrimonial y reclama otra no matrimonial | `contestacion-demanda-impugna-paternidad-matrimonial-civ-2272` |
| CIV-2274 | Demanda del padre que impugna su paternidad matrimonial sobre un hijo menor | `demanda-padre-impugna-paternidad-matrimonial-sobre-civ-2274` |
| CIV-2276 | Escrito conjunto de cónyuges sin hijos menores para seguir por mutuo acuerdo antes de contestar | `escrito-conjunto-conyuges-sin-hijos-menores-seguir-civ-2276` |
| CIV-2277 | Escrito conjunto de cónyuges con hijos menores para seguir por mutuo acuerdo tras la contestación | `escrito-conjunto-conyuges-hijos-menores-seguir-mutuo-civ-2277` |
| CIV-2278 | Escrito del demandado que se niega a la prueba biológica de paternidad | `escrito-demandado-niega-prueba-biologica-paternidad-civ-2278` |
| CIV-2279 | Recurso de apelación que alega la caducidad de la acción de impugnación de paternidad matrimonial | `recurso-apelacion-alega-caducidad-accion-impugnacion-civ-2279` |
| CIV-2285 | Demanda del hijo mayor de edad que impugna la maternidad no matrimonial sin posesión de estado | `demanda-hijo-mayor-edad-impugna-maternidad-no-civ-2285` |
| CIV-2287 | Escrito que pide medidas cautelares urgentes mientras se tramita el juicio de filiación | `escrito-pide-medidas-cautelares-urgentes-mientras-civ-2287` |
| CIV-2288 | Escrito del demandante que propone nombrar un defensor judicial al menor codemandado | `escrito-demandante-propone-nombrar-defensor-judicial-civ-2288` |
| CIV-2290 | Otrosí de la demanda de impugnación de filiación que pide proteger el patrimonio del hijo menor | `otrosi-demanda-impugnacion-filiacion-pide-proteger-civ-2290` |
| CIV-2291 | Otrosí de la demanda de reclamación de filiación que pide alimentos provisionales al demandado | `otrosi-demanda-reclamacion-filiacion-pide-alimentos-civ-2291` |
| CIV-2292 | Otrosí de la demanda de impugnación de filiación que pide proteger la persona del hijo menor | `otrosi-demanda-impugnacion-filiacion-pide-proteger-civ-2292` |
| CIV-2295 | Compraventa autorizada judicialmente de la vivienda de un menor para comprar otra con hipoteca | `compraventa-autorizada-judicialmente-vivienda-menor-civ-2295` |
| CIV-2299 | Contrato privado de venta de la vivienda de un menor por su madre con autorización judicial | `contrato-privado-venta-vivienda-menor-madre-civ-2299` |
| CIV-2306 | Poder de la madre con patria potestad del heredero para elevar a público una compraventa privada | `poder-madre-patria-potestad-heredero-elevar-publico-civ-2306` |
| CIV-2307 | Reconocimiento notarial de hijo extramatrimonial con alimentos y rectificación del Registro Civil | `reconocimiento-notarial-hijo-extramatrimonial-civ-2307` |
| CIV-2309 | Declaración de datos para inscribir una defunción en el Registro Civil consular | `declaracion-datos-inscribir-defuncion-registro-civil-civ-2309` |
| CIV-2310 | Declaración de datos para inscribir un nacimiento en el Registro Civil consular | `declaracion-datos-inscribir-nacimiento-registro-civil-civ-2310` |
| CIV-2312 | Declaración de datos para inscribir un matrimonio en el Registro Civil consular | `declaracion-datos-inscribir-matrimonio-registro-civil-civ-2312` |
| CIV-2314 | Contrato de servicios con una entidad colaboradora de adopción internacional | `contrato-servicios-entidad-colaboradora-adopcion-civ-2314` |
| CIV-2315 | Contestación a la demanda de guarda y custodia y alimentos de hijos menores | `contestacion-demanda-guarda-custodia-alimentos-hijos-civ-2315` |

## Privacidad

Ver `PRIVACY.md`.
