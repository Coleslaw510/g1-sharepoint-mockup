# G1 Budget SharePoint Page — Design Notes & Build Sheet

**Purpose:** High-fidelity mockup of a modern SharePoint Online communication-site page. After design approval, recreate in the work tenant using **native modern web parts only** (no custom HTML/SPFx required for the layout shown).

**Mockup file:** `index.html`  
**Style reference:** User Power BI homepage — light grey/white canvas, dark blue `#1a4d8c`, circular logo, large bordered square tiles, generous whitespace.

---

## Page section → native web part mapping

| # | Mockup block | SharePoint section layout | Native web part(s) | Notes |
|---|--------------|---------------------------|--------------------|-------|
| 0 | Yellow “DESIGN MOCKUP” strip | *(omit on real page)* | — | Only for the approval mockup. |
| 0b | Fake SharePoint chrome | *(omit)* | Site chrome is automatic | Do not recreate. |
| 1 | Header: logo circle + title + subtitle + “Last updated” | One-column section, vertical align center | **Image** (circular logo) or **Text** with emoji/placeholder; **Text** for title/subtitle; optional **Text** top-right for last updated | Upload a simple “G1” circle graphic (PNG). Or use **Hero** (one tile) if preferred — Hero is less “logo centered” than Image+Text. Recommended: Image (logo) + Text below. |
| 2 | Quick Links tile row | One-column section | **Quick links** → layout **Buttons** or **Tiles** | Add 7 links: G1 Power BI (external URL), MFH / Duty / Stipend / PR (anchor to page sections or list URLs), Documents, POC. Icons: upload matching PNGs or use Fluent icons if available. Border style in mockup ≈ tile with custom images. |
| 3 | “Open G1 Power BI” CTA | One-column section | **Button** web part | Link to published Power BI report URL. |
| 4 | Power BI embed area | One-column section | **Power BI** web part (preferred) or **Embed** | Select workspace/report after publish. Until ready, temporary **Text** note is fine. |
| 5 | Military Funeral Honors intro | One-column section | **Text** (section heading style) + short body | Use Heading 2 “Military Funeral Honors”. |
| 6a | MFH Duty Tracker list | Two-column section (left) | **List** web part → list “MFH Duty Tracker” | Show 5–10 items; enable “See all”. Create list first with columns below. |
| 6b | Retiree Stipend Tracker list | Two-column section (right) | **List** web part → list “Retiree Stipend Tracker” | Same. On narrow mobile, SharePoint stacks columns automatically. |
| 7 | G1 Purchase Request Tracker | One-column section | **Text** heading + **List** web part | Full-width list. |
| 8 | Documents & POC | Two-column section | Left: **Quick links** or **Text** with hyperlinks to Doc Library. Right: **Text** for POC names/roles | Replace “name TBD” with real contacts later (not in public mockup). |
| 9 | Bottom CTAs | One-column | **Button** (Back to top optional) + **Button** Open Power BI | Optional. |

### Suggested section order on the real page
1. Header (Image + Text)  
2. Quick links (Tiles)  
3. Button → Open G1 Power BI  
4. Power BI web part  
5. Text: Military Funeral Honors  
6. Two-column: List (MFH Duty) | List (Retiree Stipend)  
7. Text + List: G1 Purchase Request Tracker  
8. Two-column: Documents | Points of Contact  

---

## Lists to create (before adding List web parts)

### MFH Duty Tracker
| Column | Type | Sample values (fake) |
|--------|------|----------------------|
| Title (or Duty ID) | Single line | Auto / “MFH-001” |
| Date | Date | |
| Location / Cemetery | Single line or Choice | |
| Team Lead | Person or Single line | |
| Detail Size | Number | |
| Status | Choice: Scheduled, In Progress, Complete | |
| Notes | Multiple lines | |

### Retiree Stipend Tracker
| Column | Type |
|--------|------|
| Retiree Name | Single line (or Person if appropriate) |
| Detail Date | Date |
| Amount | Currency |
| Payment Status | Choice: Draft, Submitted, Pending, Paid |
| Submitted By | Person or Single line |
| Paid Date | Date |

### G1 Purchase Request Tracker
| Column | Type |
|--------|------|
| PR Number | Single line (or Title) |
| Description | Single line / Multiple lines |
| Requestor | Person or Single line |
| Amount | Currency |
| Funding Line | Single line or Choice |
| Status | Choice: Draft, Submitted, Approved, Obligated |
| Date Submitted | Date |

---

## Links & placeholders to replace after approval

| Item | Mockup value | Replace with |
|------|--------------|--------------|
| G1 Power BI URL | `https://app.powerbi.com/groups/me/reports/PLACEHOLDER-G1-BUDGET` | Real published report link (app.powerbi.com or Embed URL) |
| Logo | “G1” CSS circle | Unit-approved graphic (no restricted insignia in public mockup) |
| Document links | `#` placeholders | SharePoint document library file links |
| POC names | “name TBD” | Real duty titles / people on the **work** site only |
| List data | Fictional sample rows | Real lists in work tenant (CUI stays on work tenant) |

---

## Color / branding (approximate)

- Accent / headings: `#1a4d8c`
- Page background (site): light grey `#f3f2f1` (SharePoint default)
- Canvas: white
- Tile border: dark/near-black 2px (Quick links custom images help match this)

Theme tip: Set the site theme primary color close to `#1a4d8c` so Button and headings align with the mockup.

---

## Build effort estimate
- Create 3 lists + columns: ~20–30 min  
- New Site page + sections/web parts: ~20–30 min  
- Wire Power BI + Quick link icons: ~15 min  
**Total ~1 hour** once lists and report URL exist.

---

## Assumptions to confirm with Cole
1. Column sets for the three lists (especially Funding Line choices and stipend amount rules).  
2. Whether Quick links should jump to **in-page sections** or open the **full list** URLs.  
3. Power BI: embed on page **and** open-in-new-tab button (mockup has both).  
4. Two extra tiles (Documents, POC) kept — remove if unwanted.  
5. Logo: plain “G1” circle OK until an approved emblem is available.  
6. Communication site vs Team site — mockup assumes Communication site page canvas.
