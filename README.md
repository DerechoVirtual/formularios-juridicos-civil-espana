# Formularios jurídicos de España para Claude · Civil

14 plugins de formularios de Civil, uno por materia. Cada formulario es una skill que Claude rellena paso a paso con los datos del caso y entrega en Word tal cual es el formulario (Times New Roman 12, interlineado 1,15 y texto justificado): 2209 skills en total, contando la skill `indice` de cada plugin, que sirve para encontrar el formulario adecuado.

Todas las skills trabajan con **Jurisprudenciator** (https://jurisprudenciator.lexiaipro.org): antes de redactar comprueban que el conector responde y verifican en fuentes oficiales las normas que cita el formulario. Sin Jurisprudenciator conectado, las skills no redactan. Normativa revisada el 24-11-2026.

Las demás jurisdicciones están en repositorios propios: [Mercantil](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana), [Seguridad Social](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana), [Administrativo y Tributario](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana), [Laboral](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana), [Penal](https://github.com/DerechoVirtual/formularios-juridicos-penal-espana).

## Instalación

En Claude Code:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-familia-y-divorcio@formularios-juridicos-civil-espana
```

Cada plugin ocupa contexto en la conversación, así que conviene instalar solo los de las materias con las que se trabaja.

En Claude (web, escritorio y Cowork) se puede añadir este repositorio desde **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o subir cada plugin como ZIP. Los ZIP están en la página de [versiones](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest).

## Plugins

| Plugin | Contenido | Skills | ZIP |
|---|---|---:|---|
| `formularios-familia-y-divorcio` | Familia: divorcio, custodia, pensiones y parejas | 373 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-familia-y-divorcio.zip) |
| `formularios-discapacidad-y-medidas-de-apoyo` | Discapacidad y medidas de apoyo (Ley 8/2021) | 29 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-discapacidad-y-medidas-de-apoyo.zip) |
| `formularios-herencias-y-donaciones` | Herencias, testamentos y donaciones | 95 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-herencias-y-donaciones.zip) |
| `formularios-alquileres-y-desahucios` | Alquileres y desahucios | 115 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-alquileres-y-desahucios.zip) |
| `formularios-comunidades-de-propietarios` | Comunidades de propietarios | 47 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-comunidades-de-propietarios.zip) |
| `formularios-propiedad-y-derechos-reales` | Propiedad, posesión, servidumbres e hipotecas | 29 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-propiedad-y-derechos-reales.zip) |
| `formularios-contratos-consumo-y-danos` | Contratos civiles, consumo y reclamación de daños | 174 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-contratos-consumo-y-danos.zip) |
| `formularios-proceso-civil` | Proceso civil: demandas, contestaciones, prueba y vista | 290 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-proceso-civil.zip) |
| `formularios-reclamar-deudas-monitorio` | Cobrar deudas: monitorio y cambiario | 55 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-reclamar-deudas-monitorio.zip) |
| `formularios-medidas-cautelares-civiles` | Medidas cautelares y diligencias preliminares | 71 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-medidas-cautelares-civiles.zip) |
| `formularios-recursos-civiles` | Recursos civiles: reposición, apelación, casación y queja | 126 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-recursos-civiles.zip) |
| `formularios-ejecucion-y-embargos` | Ejecución de sentencias y embargos | 312 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-ejecucion-y-embargos.zip) |
| `formularios-mediacion-arbitraje-y-voluntaria` | Mediación, MASC, arbitraje y jurisdicción voluntaria | 93 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-mediacion-arbitraje-y-voluntaria.zip) |
| `formularios-resoluciones-judiciales-civiles` | Resoluciones judiciales civiles: autos, decretos y diligencias | 400 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-resoluciones-judiciales-civiles.zip) |

## Estructura

```
.claude-plugin/marketplace.json  catálogo del marketplace
plugins/<plugin>/                .claude-plugin/plugin.json, .mcp.json, skills/, README.md, PRIVACY.md, LICENSE
```

## Aviso

Los documentos que se generan son borradores que debe revisar un abogado; no constituyen asesoramiento jurídico. Las skills no guardan datos del cliente y las consultas a Jurisprudenciator describen el problema jurídico, no los datos personales.

Soporte: https://jurisprudenciator.lexiaipro.org/incidencias · Licencia: ver [LICENSE](LICENSE).
