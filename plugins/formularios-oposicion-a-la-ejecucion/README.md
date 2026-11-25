# Oposición a la ejecución, tercerías y recursos en la ejecución

> Plugin de Claude Code `formularios-oposicion-a-la-ejecucion` · **108 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para defenderse en la ejecución o discutir sus incidentes: oposición del ejecutado por motivos de fondo y procesales y su impugnación, tercerías de dominio y de mejor derecho, suspensión de la ejecución, nulidad de actuaciones y recursos contra las resoluciones de la ejecución.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 108 está al final):

- **Demandas, peticiones y solicitudes iniciales** (7). Por ejemplo: Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado; Demanda de tercería de dominio sobre un bien confesado como privativo; Demanda de tercería de dominio frente al ejecutante.
- **Contestaciones, oposiciones y alegaciones** (54). Por ejemplo: Escrito de oposición a la ejecución del fiador solidario o avalista; Escrito de oposición a la ejecución de un auto que homologa un acuerdo de mediación; Oposición a la ejecución de un acuerdo de mediación por motivos procesales o de fondo.
- **Recursos** (9). Por ejemplo: Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima); Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima); Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral.
- **Estatutos, actas, certificaciones y escrituras** (1). Por ejemplo: Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3).
- **Comunicaciones, requerimientos y cartas** (5). Por ejemplo: Solicitud de suspensión de la ejecución de un laudo por haberse ejercitado la acción de anulación; Solicitud del ejecutante de ampliar el embargo tras admitirse una tercería de dominio; Solicitud del demandado rebelde de suspensión de la ejecución.
- **Escritos de trámite y otros** (32). Por ejemplo: Escrito del ejecutante impugnando la oposición a la ejecución de un acuerdo de mediación; Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad; Escrito del ejecutante que impugna la oposición a la ejecución.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Oposición a la ejecución de una sentencia por pago»
   - «Demanda de tercería de dominio sobre un bien embargado»
   - «Impugnación de la oposición formulada por el ejecutado»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-oposicion-a-la-ejecucion:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-oposicion-a-la-ejecucion:escrito-oposicion-ejecucion-fiador-solidario-avalista-civ-1395`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 6.739 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-oposicion-a-la-ejecucion@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-oposicion-a-la-ejecucion@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-oposicion-a-la-ejecucion.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (108)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1395 | Escrito de oposición a la ejecución del fiador solidario o avalista | `escrito-oposicion-ejecucion-fiador-solidario-avalista-civ-1395` |
| CIV-1403 | Escrito de oposición a la ejecución de un auto que homologa un acuerdo de mediación | `escrito-oposicion-ejecucion-auto-homologa-acuerdo-civ-1403` |
| CIV-1404 | Oposición a la ejecución de un acuerdo de mediación por motivos procesales o de fondo | `oposicion-ejecucion-acuerdo-mediacion-motivos-civ-1404` |
| CIV-1405 | Escrito del ejecutante impugnando la oposición a la ejecución de un acuerdo de mediación | `escrito-ejecutante-impugnando-oposicion-ejecucion-civ-1405` |
| CIV-1409 | Escrito de oposición a la ejecución dineraria por cláusulas abusivas | `escrito-oposicion-ejecucion-dineraria-clausulas-civ-1409` |
| CIV-1419 | Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima | `escrito-oposicion-motivos-fondo-ejecucion-auto-cuantia-civ-1419` |
| CIV-1421 | Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio | `alegaciones-ejecutado-incidente-abusividad-apreciada-civ-1421` |
| CIV-1429 | Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad | `escrito-ejecutante-ejecucion-ordinaria-impugnando-civ-1429` |
| CIV-1438 | Oposición a la ejecución por pluspetición derivada de cláusula abusiva | `oposicion-ejecucion-pluspeticion-derivada-clausula-civ-1438` |
| CIV-1446 | Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado | `demanda-terceria-dominio-conyuge-deudor-bien-privativo-civ-1446` |
| CIV-1447 | Demanda de tercería de dominio sobre un bien confesado como privativo | `demanda-terceria-dominio-sobre-bien-confesado-como-civ-1447` |
| CIV-1452 | Oposición a la ejecución provisional que pide reducir la pensión compensatoria | `oposicion-ejecucion-provisional-pide-reducir-pension-civ-1452` |
| CIV-1454 | Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC) | `oposicion-conyuge-embargo-bienes-gananciales-deudas-civ-1454` |
| CIV-1456 | Oposición del cónyuge del ejecutado al embargo de bienes agermanados seguido como deuda consorcial | `oposicion-conyuge-ejecutado-embargo-bienes-agermanados-civ-1456` |
| CIV-1458 | Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes | `oposicion-conyuge-embargo-bienes-agermanados-haber-civ-1458` |
| CIV-1467 | Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado | `oposicion-ejecucion-sentencia-impago-pensiones-civ-1467` |
| CIV-1468 | Oposición a ejecutar un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012) | `oposicion-ejecutar-acuerdo-mediacion-sobre-alimentos-civ-1468` |
| CIV-1476 | Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones | `oposicion-motivos-fondo-ejecucion-sentencia-civ-1476` |
| CIV-1480 | Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima) | `apelacion-ejecutado-contra-auto-desestima-oposicion-civ-1480` |
| CIV-1481 | Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima) | `apelacion-ejecutante-contra-auto-estima-oposicion-auto-civ-1481` |
| CIV-1482 | Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima | `oposicion-motivos-procesales-fondo-ejecucion-auto-civ-1482` |
| CIV-1487 | Oposición a la ejecución provisional de una condena no dineraria | `oposicion-ejecucion-provisional-condena-no-dineraria-civ-1487` |
| CIV-1489 | Escrito del ejecutante que impugna la oposición a la ejecución | `escrito-ejecutante-impugna-oposicion-ejecucion-civ-1489` |
| CIV-1492 | Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil | `oposicion-ejecucion-no-notificar-saldo-deudor-poliza-civ-1492` |
| CIV-1499 | Solicitud de suspensión de la ejecución de un laudo por haberse ejercitado la acción de anulación | `solicitud-suspension-ejecucion-laudo-haberse-civ-1499` |
| CIV-1500 | Impugnación de la oposición a la ejecución forzosa de un laudo arbitral | `impugnacion-oposicion-ejecucion-forzosa-laudo-arbitral-civ-1500` |
| CIV-1501 | Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral | `recurso-reposicion-contra-auto-deniega-despachar-civ-1501` |
| CIV-1502 | Oposición al despacho de ejecución de un laudo arbitral por defectos procesales | `oposicion-despacho-ejecucion-laudo-arbitral-defectos-civ-1502` |
| CIV-1505 | Escrito del ejecutante que impugna la oposición de fondo a la ejecución por impago de pensiones | `escrito-ejecutante-impugna-oposicion-fondo-ejecucion-civ-1505` |
| CIV-1506 | Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo | `oposicion-ejecutar-impago-pensiones-alegando-mayoria-civ-1506` |
| CIV-1507 | Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas | `oposicion-ejecucion-medidas-familiares-incumplimiento-civ-1507` |
| CIV-1509 | Oposición a la ejecución por impago de pensiones en proceso matrimonial alegando compensación | `oposicion-ejecucion-impago-pensiones-proceso-civ-1509` |
| CIV-1510 | Oposición a la ejecución forzosa de medidas de un proceso matrimonial | `oposicion-ejecucion-forzosa-medidas-proceso-matrimonial-civ-1510` |
| CIV-1520 | Recurso directo de revisión contra la resolución del LAJ contraria al título ejecutivo | `recurso-directo-revision-contra-resolucion-laj-civ-1520` |
| CIV-1521 | Recurso directo de revisión contra el decreto del LAJ que declara terminada la ejecución | `recurso-directo-revision-contra-decreto-laj-declara-civ-1521` |
| CIV-1526 | Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo | `recurso-directo-revision-contra-decreto-laj-deniega-civ-1526` |
| CIV-1532 | Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio | `alegaciones-ejecutado-tasacion-pericial-aportando-civ-1532` |
| CIV-1534 | Demanda de tercería de dominio frente al ejecutante | `demanda-terceria-dominio-frente-ejecutante-civ-1534` |
| CIV-1535 | Solicitud del ejecutante de ampliar el embargo tras admitirse una tercería de dominio | `solicitud-ejecutante-ampliar-embargo-tras-admitirse-civ-1535` |
| CIV-1536 | Escrito de contestación a una demanda de tercería de mejor derecho | `escrito-contestacion-demanda-terceria-mejor-derecho-civ-1536` |
| CIV-1539 | Oposición del acreedor a la liquidación de frutos y rentas presentada por el deudor (modelo) | `oposicion-acreedor-liquidacion-frutos-rentas-civ-1539` |
| CIV-1541 | Oposición del deudor a la reclamación de daños y perjuicios en la ejecución | `oposicion-deudor-reclamacion-danos-perjuicios-ejecucion-civ-1541` |
| CIV-1546 | Impugnación de la tasación de costas por indebidas (procurador) y por excesivas (abogado) | `impugnacion-tasacion-costas-indebidas-procurador-civ-1546` |
| CIV-1547 | Oposición a la impugnación de la tasación de costas por excesivas en el orden civil | `oposicion-impugnacion-tasacion-costas-excesivas-orden-civ-1547` |
| CIV-1554 | Oposición a la ejecución de título extrajudicial por compensación | `oposicion-ejecucion-titulo-extrajudicial-compensacion-civ-1554` |
| CIV-1555 | Recurso de reposición genérico contra resolución dictada en la ejecución | `recurso-reposicion-generico-contra-resolucion-dictada-civ-1555` |
| CIV-1558 | Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho) | `oposicion-ejecucion-titulo-extrajudicial-defectos-civ-1558` |
| CIV-1560 | Oposición a ejecución de título extrajudicial por falta de capacidad o representación del ejecutante | `oposicion-ejecucion-titulo-extrajudicial-falta-civ-1560` |
| CIV-1561 | Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial | `impugnacion-ejecutante-oposicion-motivos-fondo-civ-1561` |
| CIV-1562 | Oposición a la ejecución de resolución judicial por caducidad de la acción ejecutiva | `oposicion-ejecucion-resolucion-judicial-caducidad-civ-1562` |
| CIV-1563 | Oposición a la ejecución de resolución judicial por motivos de fondo (pago) | `oposicion-ejecucion-resolucion-judicial-motivos-fondo-civ-1563` |
| CIV-1564 | Recurso de apelación contra el auto que estima la oposición a la ejecución | `recurso-apelacion-contra-auto-estima-oposicion-civ-1564` |
| CIV-1565 | Oposición a actuaciones ejecutivas concretas por infracción de la ley | `oposicion-actuaciones-ejecutivas-concretas-infraccion-civ-1565` |
| CIV-1567 | Solicitud del demandado rebelde de suspensión de la ejecución | `solicitud-demandado-rebelde-suspension-ejecucion-civ-1567` |
| CIV-1572 | Recurso de reposición contra resolución de ejecución que contradice el título ejecutivo | `recurso-reposicion-contra-resolucion-ejecucion-civ-1572` |
| CIV-1573 | Impugnación de la oposición por el ejecutante ofreciendo caución | `impugnacion-oposicion-ejecutante-ofreciendo-caucion-civ-1573` |
| CIV-1574 | Oposición a la ejecución provisional de sentencia en materia de arrendamientos urbanos | `oposicion-ejecucion-provisional-sentencia-materia-civ-1574` |
| CIV-1581 | Impugnación por el demandado del cálculo de intereses del acreedor demandante | `impugnacion-demandado-calculo-intereses-acreedor-civ-1581` |
| CIV-1582 | Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio | `oposicion-demanda-ejecutiva-condena-sentencia-indebido-civ-1582` |
| CIV-1583 | Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución | `impugnacion-ejecutante-liquidacion-intereses-ejecutado-civ-1583` |
| CIV-1587 | Escrito de oposición a la ejecución por pluspetición | `escrito-oposicion-ejecucion-pluspeticion-civ-1587` |
| CIV-1589 | Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente | `oposicion-aseguradora-obligatoria-ejecucion-auto-civ-1589` |
| CIV-1592 | Solicitud de suspensión de la ejecución por admisión de demanda de revisión de sentencia firme | `solicitud-suspension-ejecucion-admision-demanda-civ-1592` |
| CIV-1594 | Solicitud de levantar la suspensión de la ejecución por desestimación de la demanda de revisión | `solicitud-levantar-suspension-ejecucion-desestimacion-civ-1594` |
| CIV-1598 | Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3) | `certificado-sustitutivo-titulo-ejecutivo-europeo-civ-1598` |
| CIV-1617 | Escrito de impugnación de la tasación de costas por honorarios indebidos | `escrito-impugnacion-tasacion-costas-honorarios-civ-1617` |
| CIV-1620 | Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional | `escrito-ejecutante-mercantil-impugna-oposicion-embargo-civ-1620` |
| CIV-1621 | Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante | `oposicion-embargo-ejecucion-provisional-inactividad-civ-1621` |
| CIV-1622 | Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores | `contestacion-terceria-dominio-alegando-abuso-civ-1622` |
| CIV-1623 | Demanda de tercería de mejor derecho de acreedores laborales frente a la Seguridad Social en apremio | `demanda-terceria-mejor-derecho-acreedores-laborales-civ-1623` |
| CIV-1642 | Demanda de tercería de mejor derecho en el orden civil | `demanda-terceria-mejor-derecho-orden-civil-civ-1642` |
| CIV-1648 | Escrito de oposición por motivos de fondo a la ejecución de sentencia firme de condena | `escrito-oposicion-motivos-fondo-ejecucion-sentencia-civ-1648` |
| CIV-1649 | Escrito de oposición por motivos de fondo a la ejecución de una póliza de contrato mercantil | `escrito-oposicion-motivos-fondo-ejecucion-poliza-civ-1649` |
| CIV-1650 | Escrito impugnando la oposición a la ejecución por motivos de fondo | `escrito-impugnando-oposicion-ejecucion-motivos-fondo-civ-1650` |
| CIV-1651 | Escrito de oposición por defecto procesal a la ejecución de sentencia firme de condena | `escrito-oposicion-defecto-procesal-ejecucion-sentencia-civ-1651` |
| CIV-1652 | Escrito de oposición por defecto procesal a la ejecución de póliza de contrato mercantil | `escrito-oposicion-defecto-procesal-ejecucion-poliza-civ-1652` |
| CIV-1653 | Escrito del ejecutante que contesta a la oposición basada en defecto procesal | `escrito-ejecutante-contesta-oposicion-basada-defecto-civ-1653` |
| CIV-1657 | Escrito del ejecutante contestando a la oposición a la ejecución provisional por infracción procesal | `escrito-ejecutante-contestando-oposicion-ejecucion-civ-1657` |
| CIV-1658 | Oposición a la ejecución provisional no dineraria por difícil restauración si se revoca la sentencia | `oposicion-ejecucion-provisional-no-dineraria-dificil-civ-1658` |
| CIV-1659 | Escrito de oposición a la ejecución provisional solicitada tras remitirse los autos a la Audiencia | `escrito-oposicion-ejecucion-provisional-solicitada-civ-1659` |
| CIV-1673 | Escrito del ejecutante que contesta a las alegaciones del ejecutado y pide aprobar las cuentas | `escrito-ejecutante-contesta-alegaciones-ejecutado-pide-civ-1673` |
| CIV-1684 | Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos | `oposicion-conyuge-no-ejecutado-embargo-gananciales-civ-1684` |
| CIV-1691 | Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro | `demanda-terceria-dominio-sobre-inmueble-aportado-civ-1691` |
| CIV-1695 | Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura | `demanda-terceria-dominio-contra-embargo-preventivo-civ-1695` |
| CIV-1700 | Escrito del ejecutado que se opone al allanamiento del ejecutante a la tercería | `escrito-ejecutado-opone-allanamiento-ejecutante-civ-1700` |
| CIV-1702 | Escrito del ejecutante contestando a la oposición a ejecución provisional por difícil restauración | `escrito-ejecutante-contestando-oposicion-ejecucion-civ-1702` |
| CIV-1703 | Escrito de oposición a una actuación concreta de la ejecución provisional dineraria | `escrito-oposicion-actuacion-concreta-ejecucion-civ-1703` |
| CIV-1704 | Escrito del ejecutante contestando a la oposición a una actuación concreta en ejecución provisional | `escrito-ejecutante-contestando-oposicion-actuacion-civ-1704` |
| CIV-2831 | Oposición a la ejecución del supuesto socio o gestor de una entidad sin personalidad jurídica | `oposicion-ejecucion-supuesto-socio-gestor-entidad-sin-civ-2831` |
| CIV-2833 | Oposición del copropietario a la ejecución contra la comunidad por estar al corriente de pago | `oposicion-copropietario-ejecucion-contra-comunidad-civ-2833` |
| CIV-2834 | Oposición del copropietario a la ejecución por no haber sido parte en el proceso declarativo | `oposicion-copropietario-ejecucion-no-haber-sido-parte-civ-2834` |
| CIV-2835 | Impugnación del ejecutante a la oposición del copropietario que niega su responsabilidad subsidiaria | `impugnacion-ejecutante-oposicion-copropietario-niega-civ-2835` |
| CIV-2838 | Oposición del deudor a la relación de daños y perjuicios con petición de perito en la ejecución | `oposicion-deudor-relacion-danos-perjuicios-peticion-civ-2838` |
| CIV-2842 | Impugnación de la oposición del cónyuge no ejecutado que alega que los gananciales no responden | `impugnacion-oposicion-conyuge-no-ejecutado-alega-civ-2842` |
| CIV-2847 | Alegaciones del ejecutado frente a la rendición de cuentas del ejecutante | `alegaciones-ejecutado-frente-rendicion-cuentas-civ-2847` |
| CIV-2848 | Allanamiento del ejecutante a la tercería de mejor derecho basada en título ejecutivo | `allanamiento-ejecutante-terceria-mejor-derecho-basada-civ-2848` |
| CIV-2849 | Desistimiento del ejecutante ante la tercería de mejor derecho basada en título ejecutivo | `desistimiento-ejecutante-ante-terceria-mejor-derecho-civ-2849` |
| CIV-2850 | Escrito del ejecutado conforme con el allanamiento del ejecutante a la tercería de mejor derecho | `escrito-ejecutado-conforme-allanamiento-ejecutante-civ-2850` |
| CIV-2851 | Allanamiento del ejecutante a la tercería de mejor derecho no basada en título ejecutivo | `allanamiento-ejecutante-terceria-mejor-derecho-no-civ-2851` |
| CIV-2853 | Desistimiento del ejecutante ante la tercería de mejor derecho no basada en título ejecutivo | `desistimiento-ejecutante-ante-terceria-mejor-derecho-civ-2853` |
| CIV-2861 | Conformidad del abogado de quien pidió la tasación con la impugnación por honorarios excesivos | `conformidad-abogado-quien-pidio-tasacion-impugnacion-civ-2861` |
| CIV-2862 | Impugnación de la tasación de costas por incluir partidas, derechos o gastos indebidos | `impugnacion-tasacion-costas-incluir-partidas-derechos-civ-2862` |
| CIV-2864 | Impugnación de la tasación de costas por omitir gastos y derechos debidos | `impugnacion-tasacion-costas-omitir-gastos-derechos-civ-2864` |
| CIV-2865 | Impugnación de la tasación de costas por honorarios del abogado indebidos y excesivos | `impugnacion-tasacion-costas-honorarios-abogado-civ-2865` |
| CIV-2866 | Impugnación de la tasación de costas por honorarios excesivos en tutela de derecho real inscrito | `impugnacion-tasacion-costas-honorarios-excesivos-civ-2866` |
| CIV-2880 | Escrito del ejecutante que contesta a la oposición de la ejecutada en el juicio ejecutivo | `escrito-ejecutante-contesta-oposicion-ejecutada-juicio-civ-2880` |
| CIV-2883 | Escrito del ejecutante que impugna por motivos de fondo la oposición a la ejecución | `escrito-ejecutante-impugna-motivos-fondo-oposicion-civ-2883` |
| CIV-2884 | Escrito del ejecutante que impugna por defectos procesales la oposición a la ejecución | `escrito-ejecutante-impugna-defectos-procesales-civ-2884` |

## Privacidad

Ver `PRIVACY.md`.
