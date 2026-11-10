# Product brief: invoicR

- **What it is:** A web app for issuing invoices, built for a Serbian flat-rate entrepreneur (paušalac) who bills clients at home and abroad.
- **Source:** github.com/themikegit/invoicer (private). Next.js 16 App Router, React 19, Clerk auth, Supabase Postgres + Storage, @react-pdf/renderer, deployed on Vercel (region cdg1).
- **Core objects:** companies (one active), clients, invoices (immutable after issue except status), item templates.
- **Serbia-specific features:** KPO book PDF (Obrazac KPO), NBS middle exchange rates via kurs.resenje.org, turnover limits (6M RSD calendar year bookkeeping, 8M RSD rolling 365 days VAT), Serbian/English invoices and UI.
- **Audiences:** (1) the person using the app, (2) a developer running or deploying it.
- **No public API.** Only two authenticated GET routes: /invoices/[id]/pdf and /kpo.
