[← Portfolio home](../README.md) · [Project 03 overview](README.md)

# CGI-GAP-001 — Function-Level Heatmap Data

### Cypher Group Inc. · NIST CSF 2.0 Maturity Assessment · v1.0 · 15 September 2026

> [!IMPORTANT]
> **Fictional data.** Cypher Group Inc. is a fictional company created for portfolio purposes.

Companion file to `03-nist-csf-gap-assessment.md`. Machine-readable copy:
`data/03-heatmap-data.csv`. A finished chart is in `images/03-radar-current-vs-target.png`.

---

## 1. Heatmap table — paste straight into Sheets or Excel

One value per cell, no merged cells, no formatting. Copy the block below, paste into A1, then use
**Data → Split text to columns** if your spreadsheet does not split on the pipe automatically — or
import `03-heatmap-data.csv` directly, which is cleaner.

| Function | Categories Assessed | Avg Current | Target | Gap |
|---|:-:|:-:|:-:|:-:|
| GOVERN | 6 | 1.33 | 2.67 | 1.33 |
| IDENTIFY | 3 | 1.67 | 2.67 | 1.00 |
| PROTECT | 5 | 1.00 | 3.00 | 2.00 |
| DETECT | 2 | 1.00 | 2.50 | 1.50 |
| RESPOND | 4 | 1.50 | 2.50 | 1.00 |
| RECOVER | 2 | 0.50 | 2.50 | 2.00 |
| **OVERALL** | **22** | **1.23** | **2.68** | **1.45** |

**Plain CSV, if you would rather type it than import:**

```csv
Function,Categories Assessed,Avg Current,Target,Gap
GOVERN,6,1.33,2.67,1.33
IDENTIFY,3,1.67,2.67,1.00
PROTECT,5,1.00,3.00,2.00
DETECT,2,1.00,2.50,1.50
RESPOND,4,1.50,2.50,1.00
RECOVER,2,0.50,2.50,2.00
OVERALL,22,1.23,2.68,1.45
```

### How each average was derived

| Function | Categories | Individual current scores | Sum | ÷ n | Avg |
|---|:-:|---|:-:|:-:|:-:|
| GOVERN | 6 | 1 + 2 + 2 + 2 + 1 + 0 | 8 | ÷ 6 | **1.33** |
| IDENTIFY | 3 | 1 + 3 + 1 | 5 | ÷ 3 | **1.67** |
| PROTECT | 5 | 2 + 1 + 2 + 0 + 0 | 5 | ÷ 5 | **1.00** |
| DETECT | 2 | 1 + 1 | 2 | ÷ 2 | **1.00** |
| RESPOND | 4 | 2 + 1 + 2 + 1 | 6 | ÷ 4 | **1.50** |
| RECOVER | 2 | 1 + 0 | 1 | ÷ 2 | **0.50** |
| **OVERALL** | **22** | sum of all 22 Category scores | **27** | **÷ 22** | **1.23** |

> **Note on the OVERALL row.** 1.23 is the mean of all 22 Category scores, *not* the mean of the six
> Function averages. Those two numbers differ because the Functions contain unequal numbers of Categories
> (GOVERN has 6, DETECT has 2). Averaging the averages would give every Function equal weight and silently
> overweight DETECT and RECOVER. **Exclude the OVERALL row from the radar chart** — it is a summary figure,
> not a seventh axis.

---

## 2. Radar chart build instructions

### Google Sheets

1. **File → Import → Upload** `03-heatmap-data.csv` → *Insert new sheet* → Import data.
2. Move or delete the **OVERALL** row so it is outside the chart range.
3. Select `A1:A7` together with `C1:D7` — that is the **Function** column plus **Avg Current** and
   **Target**, with the header row included. Hold Ctrl (Cmd on macOS) to select the non-adjacent columns.
   Do **not** include *Categories Assessed* or *Gap*; they are on a different scale and will flatten the chart.
4. **Insert → Chart**. In the Chart editor: **Setup → Chart type → Other → Radar chart**.
5. Tick **Use row 1 as headers**. The legend should read *Avg Current* and *Target*.
6. **Customise → Vertical axis → Min 0, Max 4.** This is the step everyone skips. Without it Sheets
   auto-scales from about 0.5 to 3.0, the gap looks catastrophic, and the first competent person to look
   at it will catch you.
7. **Customise → Series → Target** → line dash type *Dashed*, line thickness 2px. Leave **Avg Current**
   solid with a light fill. Target should read as an outline you are aiming at.
8. **Customise → Chart & axis titles → Chart title:**
   `Cypher Group Inc. — NIST CSF 2.0 Maturity: Current vs Target (fictional scenario)`
9. **Customise → Legend → Position: Bottom.**
10. Three-dot menu on the chart → **Download → PNG image**. Set the browser zoom to 150% first so the
    export lands above 1200 px wide — this PNG is the thumbnail for the GitHub README and the LinkedIn post.

### Excel

1. Open `03-heatmap-data.csv`, delete the OVERALL row.
2. Select Function + Avg Current + Target including headers.
3. **Insert → Charts → See All Charts → Radar → Radar with Markers.**
4. Right-click the value axis → **Format Axis → Bounds: Minimum 0, Maximum 4; Units: Major 1.**
5. Right-click the Target series → **Format Data Series → Line → Dash type → Dash.**
6. Right-click the chart → **Save as Picture** → PNG.

### Conditional-format heatmap on the full assessment grid

1. Import `data/03-nist-csf-gap-assessment.csv`.
2. Select the **Current Score (0-4)** column, excluding the header.
3. **Format → Conditional formatting → Colour scale.**
4. Set **Minpoint = Number 0 → red**, **Midpoint = Number 2 → yellow**, **Maxpoint = Number 4 → green**.
5. Repeat on the **Gap** column but invert it: **Minpoint = Number 0 → green**, **Maxpoint = Number 3 → red**.

> Pin the colour scale to **numbers**, never to Min/Max. If you leave it on Min/Max the colours re-scale
> every time a score changes, so a 2 could be green this quarter and orange next quarter. Pinned endpoints
> mean the colour carries the same meaning in every revision, which is the entire point of a heatmap.

---

## 3. Reading the shape

| Function | Avg Current | What the shape means |
|---|:-:|---|
| GOVERN | 1.33 | Unusually high for a pre-programme company — the visible return on the CGI-POL pack. Held down by GV.SC at 0 and GV.OV at 1. After Project 4, GV.SC is 2 and GOVERN rises to 1.67. |
| IDENTIFY | 1.67 | The highest Function, carried almost entirely by ID.RA at 3. Remove the risk register and this Function collapses to 1.00. |
| PROTECT | 1.00 | Largest absolute gap (2.00). People and data are protected on paper; the platform is not protected at all. |
| DETECT | 1.00 | The company has the legal right to monitor (CGI-POL-001 §4.10) and no ability to do it. |
| RESPOND | 1.50 | Highest operational Function, because CGI-POL-005 is genuinely good. Cannot rise until DETECT produces something to respond to. |
| RECOVER | 0.50 | The worst Function, and the one that decides whether a bad day becomes an extinction event. |

*End of CGI-GAP-001 heatmap data. All figures computed programmatically from the 22-Category assessment. All data fictional.*
