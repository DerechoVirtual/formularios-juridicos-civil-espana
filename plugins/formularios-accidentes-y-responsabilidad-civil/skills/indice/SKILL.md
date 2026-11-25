---
name: indice
description: "Índice de los 94 formularios de Accidentes, seguros y responsabilidad civil. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Accidentes, seguros y responsabilidad civil: índice de formularios

> Plugin `formularios-accidentes-y-responsabilidad-civil` · 94 formularios · normativa revisada el 25-11-2026.

## Qué es

Para reclamar daños: accidentes de tráfico y Consorcio de Compensación de Seguros, reclamaciones a aseguradoras, responsabilidad civil extracontractual y profesional (también sanitaria), vicios y defectos de construcción, y protección del honor, la intimidad y la propia imagen.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Demanda contra la aseguradora por las lesiones de un accidente de tráfico»
- «Reclamación de daños por defectos de construcción en una vivienda»
- «Demanda de protección del derecho al honor»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-accidentes-y-responsabilidad-civil:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (41)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0690 | Demanda de una aseguradora contra otra en ejercicio de la acción de repetición | `demanda-aseguradora-contra-otra-ejercicio-accion-civ-0690` |
| CIV-0692 | Demanda de juicio ordinario contra la aseguradora por impago de un seguro contra robo | `demanda-juicio-ordinario-contra-aseguradora-impago-civ-0692` |
| CIV-0693 | Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia | `demanda-danos-perjuicios-franquiciado-tras-resolucion-civ-0693` |
| CIV-0695 | Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado | `demanda-juicio-ordinario-resolver-contrato-servicios-civ-0695` |
| CIV-0697 | Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida | `demanda-beneficiario-contra-aseguradora-deniega-civ-0697` |
| CIV-0698 | Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes | `demanda-juicio-ordinario-beneficiario-incumplimiento-civ-0698` |
| CIV-0734 | Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora | `demanda-juicio-verbal-haga-obra-indemnice-contra-civ-0734` |
| CIV-0736 | Demanda de juicio verbal contra conductor y aseguradora por daños y lucro cesante en accidente | `demanda-juicio-verbal-contra-conductor-aseguradora-civ-0736` |
| CIV-0737 | Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica | `demanda-juicio-verbal-contra-aseguradora-incumplir-civ-0737` |
| CIV-0747 | Demanda del asegurado contra su propia compañía aseguradora | `demanda-asegurado-contra-propia-compania-aseguradora-civ-0747` |
| CIV-0763 | Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones | `demanda-juicio-ordinario-danos-trafico-tras-juicio-civ-0763` |
| CIV-0766 | Demanda de responsabilidad civil por la infidelidad de un cónyuge | `demanda-responsabilidad-civil-infidelidad-conyuge-civ-0766` |
| CIV-0768 | Demanda de repetición de la aseguradora contra el conductor condenado por delito vial | `demanda-repeticion-aseguradora-contra-conductor-civ-0768` |
| CIV-0771 | Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil | `demanda-contra-aseguradora-cobrar-indemnizacion-civ-0771` |
| CIV-0775 | Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar | `demanda-juicio-verbal-contra-aseguradora-civ-0775` |
| CIV-0810 | Demanda ordinaria de nulidad del contrato y, subsidiariamente, incumplimiento e indemnización | `demanda-ordinaria-nulidad-contrato-subsidiariamente-civ-0810` |
| CIV-0820 | Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora | `demanda-ordinaria-danos-materiales-accidente-trafico-civ-0820` |
| CIV-0823 | Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros | `demanda-juicio-verbal-danos-cosas-trafico-contra-civ-0823` |
| CIV-0825 | Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora | `demanda-juicio-ordinario-danos-trafico-contra-civ-0825` |
| CIV-0826 | Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico | `demanda-juicio-ordinario-contra-aseguradora-lesiones-civ-0826` |
| CIV-0845 | Demanda de juicio ordinario por daños derivados de accidente de circulación de vehículos de motor | `demanda-juicio-ordinario-danos-derivados-accidente-civ-0845` |
| CIV-0847 | Demanda sucinta de juicio verbal por daños derivados de la circulación de vehículos de motor | `demanda-sucinta-juicio-verbal-danos-derivados-civ-0847` |
| CIV-0848 | Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños | `demanda-juicio-ordinario-resolver-compraventa-inmueble-civ-0848` |
| CIV-0850 | Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros | `demanda-juicio-ordinario-accidente-trafico-contra-civ-0850` |
| CIV-0851 | Demanda contra la agencia minorista por defectuosa prestación de servicios de un viaje combinado | `demanda-contra-agencia-minorista-defectuosa-prestacion-civ-0851` |
| CIV-0853 | Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala | `demanda-juicio-ordinario-reclamar-honorarios-civ-0853` |
| CIV-2552 | Demanda de indemnización por incumplir un contrato o precontrato de compraventa de inmueble | `demanda-indemnizacion-incumplir-contrato-precontrato-civ-2552` |
| CIV-2562 | Demanda de juicio verbal por accidente de tráfico contra conductor, transportista y aseguradora | `demanda-juicio-verbal-accidente-trafico-contra-civ-2562` |
| CIV-2619 | Demanda ordinaria reclamando lo cubierto por el seguro obligatorio y el exceso al voluntario | `demanda-ordinaria-reclamando-lo-cubierto-seguro-civ-2619` |
| CIV-2620 | Demanda de juicio ordinario por el lucro cesante de un taxista tras un accidente de tráfico | `demanda-juicio-ordinario-lucro-cesante-taxista-tras-civ-2620` |
| CIV-2621 | Demanda del viajero herido en transporte público reclamando el seguro obligatorio de viajeros | `demanda-viajero-herido-transporte-publico-reclamando-civ-2621` |
| CIV-2622 | Demanda ordinaria al Consorcio de Compensación de Seguros por daños de vehículo desconocido | `demanda-ordinaria-consorcio-compensacion-seguros-danos-civ-2622` |
| CIV-2629 | Demanda verbal del perjudicado contra conductor, dueño y aseguradora pidiendo perito judicial | `demanda-verbal-perjudicado-contra-conductor-dueno-civ-2629` |
| CIV-2630 | Demanda contra la aseguradora por siniestro en periodo de gracia o seis meses tras vencer la póliza | `demanda-contra-aseguradora-siniestro-periodo-gracia-civ-2630` |
| CIV-2631 | Demanda ordinaria por daños contra el causante que conducía su vehículo sin seguro | `demanda-ordinaria-danos-contra-causante-conducia-civ-2631` |
| CIV-2632 | Demanda ordinaria contra el conductor cuya aseguradora está concursada, disuelta o insolvente | `demanda-ordinaria-contra-conductor-cuya-aseguradora-civ-2632` |
| CIV-2641 | Demanda ordinaria del perjudicado contra conductor, dueño y aseguradora pidiendo perito judicial | `demanda-ordinaria-perjudicado-contra-conductor-dueno-civ-2641` |
| CIV-2642 | Demanda ordinaria de los perjudicados por la muerte de una persona en accidente de tráfico | `demanda-ordinaria-perjudicados-muerte-persona-civ-2642` |
| CIV-2643 | Demanda ordinaria por daños causados por un vehículo robado contra el Consorcio y la aseguradora | `demanda-ordinaria-danos-causados-vehiculo-robado-civ-2643` |
| CIV-2659 | Demanda ordinaria de la aseguradora que se subroga frente a los responsables del siniestro | `demanda-ordinaria-aseguradora-subroga-frente-civ-2659` |
| CIV-2660 | Demanda ordinaria por accidente con elemento extranjero sometido a tribunales y ley españoles | `demanda-ordinaria-accidente-elemento-extranjero-civ-2660` |

### Contestaciones, oposiciones y alegaciones (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0770 | Contestación a la demanda de repetición de la aseguradora contra el asegurado | `contestacion-demanda-repeticion-aseguradora-contra-civ-0770` |
| CIV-0811 | Contestación por incumplimiento contractual con reconvención de resolución e indemnización | `contestacion-incumplimiento-contractual-reconvencion-civ-0811` |
| CIV-0822 | Contestación a demanda ordinaria de conductor y aseguradora codemandados por daños de un accidente | `contestacion-demanda-ordinaria-conductor-aseguradora-civ-0822` |
| CIV-2557 | Contestación a la demanda de indemnización por incumplir un contrato o precontrato de compraventa | `contestacion-demanda-indemnizacion-incumplir-contrato-civ-2557` |
| CIV-2561 | Contestación de la comunidad a la demanda de pago de la obra, con reconvención por daños | `contestacion-comunidad-demanda-pago-obra-reconvencion-civ-2561` |
| CIV-2593 | Contestación de la aseguradora a la demanda de lesiones y daños materiales por accidente de tráfico | `contestacion-aseguradora-demanda-lesiones-danos-civ-2593` |
| CIV-2594 | Contestación de la aseguradora en un accidente múltiple alegando prejudicialidad penal | `contestacion-aseguradora-accidente-multiple-alegando-civ-2594` |

### Contratos, pactos y cláusulas (15)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0732 | Contrato de servicios profesionales de asesoría jurídica o de abogado | `contrato-servicios-profesionales-asesoria-juridica-civ-0732` |
| CIV-0741 | Contrato de servicios de mantenimiento entre un cliente y una empresa | `contrato-servicios-mantenimiento-entre-cliente-empresa-civ-0741` |
| CIV-0742 | Contrato de servicios entre una aseguradora y un perito tasador | `contrato-servicios-entre-aseguradora-perito-tasador-civ-0742` |
| CIV-0743 | Contrato de servicios de limpieza entre una comunidad de propietarios y una empresa | `contrato-servicios-limpieza-entre-comunidad-civ-0743` |
| CIV-2549 | Contrato de arrendamiento de servicios profesionales para una actividad determinada | `contrato-arrendamiento-servicios-profesionales-civ-2549` |
| CIV-2607 | Contrato de prestación de servicios profesionales entre un cliente y su abogado | `contrato-prestacion-servicios-profesionales-entre-civ-2607` |
| CIV-2613 | Contrato de servicios profesionales entre el asegurado y el abogado de su aseguradora | `contrato-servicios-profesionales-entre-asegurado-civ-2613` |
| CIV-2626 | Contrato de servicios médicos entre el facultativo de la aseguradora y el perjudicado | `contrato-servicios-medicos-entre-facultativo-civ-2626` |
| CIV-2627 | Contrato de servicios profesionales entre una promotora o constructora y un arquitecto | `contrato-servicios-profesionales-entre-promotora-civ-2627` |
| CIV-2628 | Contrato de servicios ganaderos de cría y engorde de animales | `contrato-servicios-ganaderos-cria-engorde-animales-civ-2628` |
| CIV-2665 | Contrato privado de cesión de un contrato de servicios entre particulares | `contrato-privado-cesion-contrato-servicios-entre-civ-2665` |
| CIV-2672 | Contrato de servicios médicos entre una entidad o colegio y un médico | `contrato-servicios-medicos-entre-entidad-colegio-medico-civ-2672` |
| CIV-2673 | Contrato de servicios médicos entre una compañía de seguros y un médico | `contrato-servicios-medicos-entre-compania-seguros-civ-2673` |
| CIV-2681 | Acuerdo entre aseguradora y perjudicado para pagar los daños del vehículo con renuncia a acciones | `acuerdo-entre-aseguradora-perjudicado-pagar-danos-civ-2681` |
| CIV-2682 | Acuerdo extrajudicial que liquida la indemnización del accidente con renuncia a la vía judicial | `acuerdo-extrajudicial-liquida-indemnizacion-accidente-civ-2682` |

### Estatutos, actas, certificaciones y escrituras (1)

| Código | Formulario | Skill |
|---|---|---|
| CIV-2601 | Poder para cobrar una indemnización en nombre del poderdante | `poder-cobrar-indemnizacion-nombre-poderdante-civ-2601` |

### Comunicaciones, requerimientos y cartas (14)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0699 | Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios | `requerimiento-comprador-resolver-compraventa-inmueble-civ-0699` |
| CIV-0703 | Requerimiento al avalista (banco o aseguradora) de devolver lo pagado tras resolver la compraventa | `requerimiento-avalista-banco-aseguradora-devolver-lo-civ-0703` |
| CIV-0710 | Reclamación de daños por defectos en la calidad del suministro eléctrico | `reclamacion-danos-defectos-calidad-suministro-electrico-civ-0710` |
| CIV-0715 | Reclamación a la aerolínea por daños o pérdida del equipaje facturado | `reclamacion-aerolinea-danos-perdida-equipaje-facturado-civ-0715` |
| CIV-0733 | Carta a la aseguradora reclamando el pago de la cobertura de un seguro de defensa jurídica | `carta-aseguradora-reclamando-pago-cobertura-seguro-civ-0733` |
| CIV-0746 | Reclamación del conductor perjudicado a la compañía aseguradora | `reclamacion-conductor-perjudicado-compania-aseguradora-civ-0746` |
| CIV-2615 | Reclamación al Consorcio de Compensación de Seguros por auto ejecutivo con conductor sin seguro | `reclamacion-consorcio-compensacion-seguros-auto-civ-2615` |
| CIV-2616 | Reclamación al Consorcio de Compensación de Seguros por auto ejecutivo con aseguradora insolvente | `reclamacion-consorcio-compensacion-seguros-auto-civ-2616` |
| CIV-2617 | Reclamación al Consorcio de Compensación de Seguros por auto ejecutivo con vehículo robado | `reclamacion-consorcio-compensacion-seguros-auto-civ-2617` |
| CIV-2618 | Reclamación al Consorcio de Compensación de Seguros por auto ejecutivo con vehículo desconocido | `reclamacion-consorcio-compensacion-seguros-auto-civ-2618` |
| CIV-2624 | Reclamación extrajudicial previa al conductor que circulaba sin seguro | `reclamacion-extrajudicial-previa-conductor-circulaba-civ-2624` |
| CIV-2625 | Reclamación extrajudicial previa por daños causados por un vehículo desconocido | `reclamacion-extrajudicial-previa-danos-causados-civ-2625` |
| CIV-2661 | Reclamación extrajudicial previa al conductor cuya aseguradora está concursada o insolvente | `reclamacion-extrajudicial-previa-conductor-cuya-civ-2661` |
| CIV-2663 | Reclamación extrajudicial previa por daños causados por un vehículo robado | `reclamacion-extrajudicial-previa-danos-causados-civ-2663` |

### Escritos de trámite y otros (16)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0683 | Escrito de desistimiento del tomador de un seguro de vida | `escrito-desistimiento-tomador-seguro-vida-civ-0683` |
| CIV-0684 | Escrito del consumidor para desistir de servicios financieros contratados a distancia | `escrito-consumidor-desistir-servicios-financieros-civ-0684` |
| CIV-0721 | Hoja de reclamación en servicios de asistencia técnica de aparatos de uso doméstico | `hoja-reclamacion-servicios-asistencia-tecnica-aparatos-civ-0721` |
| CIV-0724 | Desistimiento del consumidor en servicios financieros a distancia con datos del producto adquirido | `desistimiento-consumidor-servicios-financieros-civ-0724` |
| CIV-0745 | Oferta motivada de la aseguradora al perjudicado sin reclamación previa | `oferta-motivada-aseguradora-perjudicado-sin-civ-0745` |
| CIV-0755 | Impugnación de la jura de cuentas del abogado por honorarios excesivos | `impugnacion-jura-cuentas-abogado-honorarios-excesivos-civ-0755` |
| CIV-2633 | Hechos y fundamentos de un accidente de tráfico por cambio indebido de vía o calzada | `hechos-fundamentos-accidente-trafico-cambio-indebido-civ-2633` |
| CIV-2634 | Hechos y fundamentos de un accidente de tráfico por invasión del carril contiguo | `hechos-fundamentos-accidente-trafico-invasion-carril-civ-2634` |
| CIV-2635 | Hechos y fundamentos de un accidente de tráfico con un vehículo de servicios de urgencia | `hechos-fundamentos-accidente-trafico-vehiculo-civ-2635` |
| CIV-2636 | Hechos y fundamentos de un accidente de tráfico al incorporarse un vehículo a la circulación | `hechos-fundamentos-accidente-trafico-incorporarse-civ-2636` |
| CIV-2637 | Hechos y fundamentos de un accidente de tráfico en un cruce sin señalizar | `hechos-fundamentos-accidente-trafico-cruce-sin-civ-2637` |
| CIV-2638 | Hechos y fundamentos de un accidente de tráfico por adelantamiento indebido | `hechos-fundamentos-accidente-trafico-adelantamiento-civ-2638` |
| CIV-2639 | Hechos y fundamentos de un accidente de tráfico por colisión en cadena | `hechos-fundamentos-accidente-trafico-colision-cadena-civ-2639` |
| CIV-2640 | Hechos y fundamentos de un accidente de tráfico por atropello de peatón | `hechos-fundamentos-accidente-trafico-atropello-peaton-civ-2640` |
| CIV-2671 | Hechos y fundamentos de un accidente de tráfico por alcance entre vehículos en el mismo sentido | `hechos-fundamentos-accidente-trafico-alcance-entre-civ-2671` |
| CIV-2683 | Hechos y fundamentos de un accidente de tráfico en un cruce señalizado | `hechos-fundamentos-accidente-trafico-cruce-senalizado-civ-2683` |
