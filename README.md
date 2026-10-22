# DSC Manager: three versions to compare (22-Oct-2026)

Open each file in a browser (double-click). The header shows **V1**, **V2** or **V3**. Sample data is the same in all three (15 clients, 25 DSCs, 6 clients without a DSC at the start). Each version keeps its own saved data.

| | V1 KDK baseline | V2 KDK refined | V3 Workbench (own design) |
|---|---|---|---|
| File | V1_KDK_baseline.html | V2_KDK_refined.html | V3_Workbench.html |
| Look | KDK blue band, light left panel | Same as V1 | Teal accent, warm page, white top bar with tabs, no side panel |
| Text | 12.5–13 px, 24 px figures | 12 px, 22 px figures, tighter rows (30 px) | Same as V2 |
| Text size switch | no | Tools → Text size (Small / Default / Large) | Same as V2 |
| Token colour | dropdown | Swatches in real colours, live token picture, "Other" opens a colour picker (exact shade saved) | Same as V2, plus tokens drawn in their real colour on the client board |
| Overview | 4 tiles, banner, portal cards, renewals table | Same, slimmer | Certificates bar, signatory coverage per portal, Others, and one "Needs action" list (expired, expiring, missing) with Add / View buttons |
| Finding a client's DSCs | All DSCs grouped list + side panel | Same | Clients tab: pick a client, see GST / TDS / ITR / Others columns with each signatory and its token card, or a dashed "Missing DSC" card with Add DSC |
| Rows visible, Clients with No DSC (1093 px) | 7 | 9 | 9 |

## Tested (Edge, this machine)
- V2: 86 + 29 + 9 behaviour checks passed (navigation, filters, add, scan, undo, keys, colour picker).
- V3: 31 behaviour checks passed (tabs, overview, client board, add from a slot, colour picker). The All DSCs and No DSC screens are the same code as V2 and were covered by the V2 run.
- All three: size matrix at 11 sizes plus dark mode, no errors, no sideways page scroll, no text under 12 px at the default text size.
- Not tested: Firefox, Safari, a screen reader. V3 was not run through the full V2 suite (its side panel does not exist).

## Limits
- Scan DSC is a demo and never reads a USB token.
- "Small" text size makes text about 11 px, which is under the KDK 12 px rule. It is only used if you choose it.
- V3 breaks some KDK rules on purpose (colours, top tabs instead of a left panel). It follows the state-colour, icon-with-word and keyboard rules.
