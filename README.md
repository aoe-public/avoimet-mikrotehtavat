# Avoimet mikrotehtävät (OER + S2)

Itsenäinen avoimen lähdekoodin oppimateriaalikirjasto (yhteensopiva `aoe.fi`-palvelun kanssa – ei Opetushallituksen virallinen kanava).

Kaikki mikrotehtävät toimivat täysin selaimessa ilman kirjautumista tai henkilötietojen keräämistä (Zero PII) ja täyttävät **WCAG 2.1 AA** -saavutettavuusperiaatteet.

## Lisenssit
| Kohde | Lisenssi | Tiedosto |
| :--- | :--- | :--- |
| Lähdekoodi (HTML, CSS, JS) | **MIT** | [`LICENSE`](./LICENSE) |
| Oppimateriaalit, skenaariot ja S2-sanastot | **CC BY 4.0** | [`LICENSE-CONTENT.md`](./LICENSE-CONTENT.md) |
| Kuvailutiedot / metatiedot (`catalog.json`, `manifest.json`) | **CC0** | [`LICENSE-CONTENT.md`](./LICENSE-CONTENT.md) |

## Tiedostorakenne
- `index.html` — Opettajaportaali (esikatselu, `<iframe>`-upotuskoodi, suorat linkit, HTML-lataus).
- `catalog.json` & `llms.txt` — Staattinen indeksi tekoälyagenteille ilman MCP-asennusta.
- `tasks/yrittajyys-investointi-takaisinmaksuaika/`
  - `manifest.json` — ePeruste- ja `aoe.fi`-metatiedot sekä parametrirajat.
  - `widget.html` — Itsenäinen 2-välilehtinen mikrotehtävämoottori (Simulaattori + Sokraattinen haastekoe).
  - `presets/maatila.json` & `presets/kahvila.json` — Alakohtaiset skenaariot.
  - `i18n/s2_bundle.json` — Esigeneroidut S2-ammattisanastot (ml. arabian RTL-tuki).

## Käyttö URL-parametreilla
- `?preset=maatila&s2=uk` → Maatila-skenaario + ukrainan S2-sanasto
- `?preset=kahvila&s2=ar` → Kahvila-skenaario + arabian RTL-sanasto
