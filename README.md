# Infyslate Control Tower

AI-native supply chain intelligence — eight cross-linked modules across six distribution
centres, delivered as a single self-contained demo application.

**Live demo:** deployed from `index.html` (static, no build step).

---

## What's here

| Path | Description |
|---|---|
| `index.html` | The Control Tower application. Single file, no dependencies, works offline. |
| `decks/` | Client offerings deck (PPTX) and demo/architecture documents. |
| `pitch-docs/` | Source Infyslate offerings decks used as the brand/flow reference. |
| `design-docs/` | Business, technical and UI/UX plans. |
| `app/` | Next.js scaffold reserved for the Phase 1 production build. |

## The eight modules

1. **Out-of-Stock Intelligence** — days-to-stockout projection, ROP breach detection, revenue-at-risk ranking
2. **Stock Transfer Optimization** — five-constraint feasibility solver scoring every lane 0–100
3. **Reconciliation + AI Flagging** — three-way PO/GR/invoice match with contract-clause penalty attribution
4. **Salvage / Liquidation AI** — two-phase optimizer: DC absorption first, then channel liquidation
5. **Replenishment & Planning** — EOQ plus a live service-level calculator with lead-time gap detection
6. **Document AI** — seven-stage pipeline from ingestion to ERP post
7. **3PL Control** — carrier scorecards, lane-level performance, damage and claims tracking
8. **Control Tower** — unified situational view; actions in one module resolve linked alerts in another

## Running locally

No build step and no dependencies — open the file directly:

```bash
start index.html          # Windows
open index.html           # macOS
```

Or serve it over HTTP:

```bash
npx serve .
```

## Deployment

Static site. Vercel serves `index.html` at the root; `vercel.json` sets security headers
and clean URLs.

```bash
npx vercel --prod
```

## Notes

- Written in ES5 with no framework, so it runs from `file://` with no tooling.
- Charts are hand-computed inline SVG; no charting library.
- Demo data is deterministic — a seeded LCG keyed off each SKU id, so every run matches.
- The **AI Settings** dialog stores an optional API key in `localStorage` only. In demo mode
  nothing is transmitted to any server.
