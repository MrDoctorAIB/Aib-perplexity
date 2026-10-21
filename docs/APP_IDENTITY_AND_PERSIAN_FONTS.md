# App Identity, Typography, and Persian PDF Rules
Status: specification only; no app fonts or UI have been implemented.

## 1. One app, one approved visual identity

Each app or confirmed variant must have a small, documented design identity:
- app name and unique project ID
- icon/logo and primary/secondary colors
- typography roles: display/title, body, compact UI, code/numbers
- accessibility: legibility, scaling, contrast, and system font fallback
- language coverage, including Persian RTL if needed
- source/license and attribution for every bundled font

Do not create dozens of arbitrary fonts for one app. Start with a curated set of at most 3–5 font families per app (usually one primary family plus optional display/monospace roles). If the owner explicitly requests ten options, generate ten *candidates* for review, then select a small tested set. A font candidate list is not an implemented font system.

## 2. Shared typography registry

Track fonts in a table:
| App ID | Font family | Role | Languages | License/source | Bundled? | Verified in UI/PDF? |
|---|---|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD | No | No |

Never invent the name of a previously chosen special font. The exact font previously discussed by the owner has not yet been identified. Ask for the font file/name only when implementation requires it; meanwhile mark it TBD and use a legally available Unicode fallback.

## 3. Persian and Arabic PDF requirements

For Persian PDF generation:
- Use a licensed Unicode font with full Persian/Arabic glyph coverage, such as Vazirmatn or Noto Naskh Arabic when available.
- Embed the font when the PDF library supports it.
- Apply RTL paragraph direction and correct Arabic/Persian shaping; correct glyph coverage alone does not guarantee correct joining or order.
- Verify mixed Persian/Latin text, numerals, punctuation, URLs, tables, and code.
- Render representative pages and inspect letter joining, word order, clipping, missing glyphs, and copy/paste text extraction.
- Record the exact font file/version and the verification evidence for each release.
- If the required historical font is not supplied or identified, state that clearly instead of claiming it was used.

## 4. Browser variants

Potential browser names mentioned by the owner include Blue Browser, Red Browser, Kiwi, Firefox, Chrome, and Vivaldi. Treat them as an unverified discovery list, not proof that these are owned projects or that source code is available. Before making variants:
1. Inventory the actual installed apps and package IDs on Samsung/Xiaomi.
2. Determine whether the owner intends original apps, bookmarks/shortcuts, extensions, or separate browser products.
3. Identify each product's source and license.
4. Define meaningful functional differences before creating a new brand or fork.
5. Implement and verify one small prototype before duplicating variants.

Do not imply that a browser's font can be changed globally from another app. System-level fonts, browser settings, website fonts, and bundled app fonts are different scopes and require different supported mechanisms.
