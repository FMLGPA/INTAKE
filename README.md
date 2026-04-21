# FMLG Client Intake Form
**Family Matters Law Group, P.A.**
`index.html` — Single-file, no backend, no login required.

---

## What This Is

A branded, interactive client intake form that replaces the multiple Smokeball intake forms staff previously had to select and send manually. Clients access it from any browser, answer questions in a single guided flow, and get a structured intake summary at the end. Staff copy that summary directly into Smokeball.

No app. No database. No server. One HTML file.

---

## What It Covers

Six case types, each with its own conditional question set:

| Case Type | Triggers |
|---|---|
| Dissolution – Petitioner | Filing for divorce |
| Dissolution – Respondent | Served with divorce papers |
| Paternity – Petitioner | Filing a paternity action |
| Paternity – Respondent | Served with paternity papers |
| Modification | Changing existing child support or parenting plan |
| Other Matter | Name change, adoption, or other |

### Questions that appear conditionally based on answers:
- **Divorce petitioner only** — Florida residency / long-arm jurisdiction checkboxes
- **Name restoration** — maiden name field appears only if Yes
- **Other party's attorney** — firm details expand only if Yes
- **Other party employed** — employer fields expand only if Yes
- **Real estate** — property details appear only if they owned a home together
- **Children: Yes** — unlocks timesharing section, 50/50 deviation factors, schedule options, child support, DOR, prior order details
- **Sole parental responsibility** — required justification field appears
- **Child support prior order: Yes** — case number, amount, type, DOR involvement
- **Income concerns** — detail field appears only if Yes
- **Alimony** — position question appears only if at issue
- **Attorney fees** — appears for paternity and modification only
- **Divorce sentiment** — appears for dissolution only

---

## How to Deploy

### Option 1 — Tiiny.host (fastest, no account needed)
1. Go to [tiiny.host](https://tiiny.host)
2. Click **Upload**
3. Drop `index.html` directly
4. Get a live link instantly — example: `fmlg-intake.tiiny.site`

### Option 2 — Cloudflare Pages (free, permanent, recommended)
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Create a free account
3. Click **Create a project → Direct Upload**
4. Create a folder, put `index.html` inside, upload the folder
5. Your link: `fmlg-intake.pages.dev` (customizable)

### Option 3 — GitHub Pages
1. Create a free account at [github.com](https://github.com)
2. New repository → name it `fmlg-intake`
3. Upload `index.html`
4. Go to **Settings → Pages** → set source to main branch
5. Your link: `yourusername.github.io/fmlg-intake`

> **Important:** The file must be named `index.html` for all three options to work. It is already named correctly in this package.

---

## How Clients Use It

1. Client receives the link (text, email, or portal message)
2. Client opens it on any device — phone, tablet, or computer
3. Client selects their case type
4. Form walks them through 7 steps, showing only questions relevant to their situation
5. Client submits — summary appears on screen
6. Client copies the summary **or** staff use the Copy Summary button to grab it

---

## How Staff Use the Output

When a client submits:

1. The completed intake summary displays on screen
2. Click **Copy Summary** — copies a clean plain-text version to clipboard
3. Paste into Smokeball notes or the relevant intake fields
4. Proceed with the normal new matter workflow

The summary is organized by section (Client Personal, Client Employment, Spouse/Other Party, Marriage & Property, Children & Timesharing, Goals & Preferences) and maps directly to Smokeball field groupings.

---

## What This Does NOT Do

- It does not email results automatically (no backend)
- It does not save data between sessions — if the client closes the tab, they start over
- It does not push directly into Smokeball — staff copy/paste the summary
- It does not replace the UCCJEA form or Children's Preferences form — those are still sent separately after intake

### Future upgrades (if needed):
- Add email submission using [Formspree](https://formspree.io) — free tier, no backend required, results go to any email address
- Add auto-save using browser localStorage so clients can resume
- Connect directly to Smokeball API if/when available

---

## Technical Notes

- **Single file** — all HTML, CSS, and JavaScript in one `index.html`
- **No dependencies** — no npm, no build step, no framework
- **Fonts** — loaded from Google Fonts (requires internet connection)
- **No data storage** — nothing is saved to any server; all data lives in the browser session only
- **Mobile responsive** — tested at 380px width and up
- **Browsers** — works in Chrome, Safari, Firefox, Edge

---

## Brand Standards Applied

| Element | Spec |
|---|---|
| Display font | Black Han Sans |
| Label / button font | Oswald |
| Body font | Nunito |
| Primary CTA color | Signature Pink `#FF1F8E` |
| Submit button | Power Orange `#FF6B00` |
| Section labels | Clarity Teal `#00B5B8` |
| Child repeater accent | Electric Lime `#C8D400` |
| Background | Paper White `#F7F5F0` |
| Header / footer | Firm Black `#0D0D0D` |
| Color bar | Pink → Orange → Lime → Teal |

---

## File Structure

```
fmlg-intake/
└── index.html       ← the entire application
└── README.md        ← this file
```

That's it.

---

## Questions / Changes

To modify questions, add a case type, or update the form, contact whoever manages your Claude project. The entire form is editable in one file — no developer environment required.

---

*Family Matters Law Group, P.A. — FL Bar No. 64399 — familymatterslawgroup.com*
*Clarity. Options. Control.*
