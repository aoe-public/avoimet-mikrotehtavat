# Mikrotehtäväkirjasto – Pilottirunko (v0.1)

Tämä kansio demonstroi avoimen mikrotehtäväkirjaston rakenteen yhdellä valmiilla moottorilla (`yrittajyys-investointi-takaisinmaksuaika`), kahdella alakohtaisella skenaariolla (`maatila`, `kahvila`) ja kuudella S2-tukikielellä (`en`, `sv`, `uk`, `et`, `ar` RTL-tuella, `so`).

## Tiedostorakenne
- `catalog.json` — Staattinen indeksi, jonka mikä tahansa agentti voi lukea ilman MCP-asennusta.
- `tasks/yrittajyys-investointi-takaisinmaksuaika/`
  - `manifest.json` — ePeruste- ja `aoe.fi`-metatiedot sekä parametrirajat.
  - `widget.html` — Itsenäinen WCAG 2.1 AA -widget (toimii sekä suoraan selaimessa tuplaklikkaamalla että upotettuna `<iframe>`-elementtinä).
  - `presets/maatila.json` & `presets/kahvila.json` — Erotettu skenaariokerros (uuden toimialan lisääminen ei vaadi koodia).
  - `i18n/s2_bundle.json` — Esigeneroitu S2-ammattisanasto (ml. arabian RTL-tuki).

## Käyttö URL-parametreilla (kun julkaistu portaalissa)
- `widget.html?preset=maatila&s2=uk` → Maatila-skenaario + ukrainan S2-sanasto
- `widget.html?preset=kahvila&s2=ar` → Kahvila-skenaario + arabian RTL-sanasto
