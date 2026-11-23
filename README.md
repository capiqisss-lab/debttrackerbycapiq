# Verdelo — screenshot-based React recreation

## Setup

```bash
npm install
npm run dev
```

Open the Vite URL and navigate to `/#/overview`.

## Stack
Vite, React 18, TypeScript, React Router HashRouter, Recharts, lucide-react, plain CSS variables. No backend. Data is in `src/mockData.ts`.

## Design tokens (estimated from screenshots)

- Background: `#0b1711`; dark base: `#07110d`
- Card surface: `#17251c`; sidebar gradient: `#26372d` → `#101c15`
- Border: `#405348`; mint accent: `#68dca1`
- Text: `#eaf1eb`; secondary: `#a9bbb0`; chart gray: `#829189`
- Chart mint: `#67dba0`; teal: `#64c5c2`; gold: `#edc56f`; blue: `#9ac5e9`
- Font: DM Sans (Google Fonts), approximate visual match
- Sidebar width: 285px; topbar height: 82px; page padding: 30px
- Panel radius: 26px; panel padding: 23px; card grid gap: 18–20px
- Main heading: 45px / 700; panel heading: 18px / 700; body: 15px

## Routes
`/#/overview`, `/#/cards`, `/#/payments/activity`, `/#/payments/send`, `/#/payments/bills`, `/#/insights`, `/#/budgets`, `/#/goals`, `/#/household`, `/#/settings`, `/#/help`.

## Assumptions and limitations

- Screenshots show partial sections of Overview, Insights, Goals, Household, and Payments Activity. Other pages and unseen sections are inferred from the shared visual language.
- Some chart datapoints, tooltips, card-back design, navigation behavior, and unseen controls are approximations; visible summary figures and names are transcribed.
- Card freeze, savings pot adjustments, quick send, filters, and household permissions are local UI simulations; they do not persist or move real money.
- The bright orange “BUY THIS TEMPLATE” element appears to be a demo-site overlay and is deliberately excluded from the product UI.
- Screenshot-specific viewport differences and source-site assets prevent a verified pixel-for-pixel comparison. This is a faithful starting implementation, not a certified exact match.


## Cinematic animation update
- Dashboard numbers count from zero on every route entry and animate to new values.
- Bar charts rise from the baseline; area charts reveal progressively. Range changes restart the chart animation.
- Bank cards use actual two-sided 3D flips and swipe transitions.
- Savings pot liquid height smoothly changes when money is added or removed.
- Background money particles reduced to 10 for performance.
- All motion respects reduced-motion preferences.
- Supabase was intentionally not added. Existing local data features remain.
