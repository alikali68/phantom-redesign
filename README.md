# Phantom Redesign — Trust & Clarity

A UX concept case study: redesigning three Phantom wallet flows around one theme — **trust & clarity**. Designed in Figma in 2 days, from real app screenshots.

> Built for Superteam Earn's [_Redesign Your Favourite App on Solana_](https://superteam.fun/earn/listing/redesign-your-favourite-app-on-solana) bounty (1,500 USDC). The listing turned out to be a regional (India-only) listing, so this lives on as a portfolio case study.

🔗 **[Open the Figma file](https://www.figma.com/design/c2gu4QmGVCGGuOY4xGgeSV/Phantom-Redesign-%E2%80%94-Redesign-Bounty)** — before/after screens for every feature, mobile + desktop variations, with the design rationale written under each.

## The three features

### 1. Trade-page transparency & safety
Phantom's Trade flow opens leveraged positions with **10x leverage pre-selected**, while Liquidation and Distance show "—" and fees are never itemized. The redesign adds a pre-confirm **order summary card** (you pay → position size → each fee → liquidation price as a real number → distance %), defaults leverage to **2x** with plain-language labels ("2x = a 50% drop liquidates your position"), and replaces the one-line risk disclaimer with a real warning block.

### 2. Activity-tab address-poisoning guards
Attackers poison transaction history with dust from lookalike addresses; victims copy the wrong address and lose funds (one real case: $264K). The redesign badges suspicious dust transactions as **"Suspicious"**, and tapping copy on any address from History opens a **"Verify this address"** sheet forcing a 2-second check before the copy happens.

### 3. Token-list spam quarantine
Airdropped scam tokens sit in the main list next to real holdings with zero distinction. The redesign auto-detects unknown tokens and moves them into a **"Quarantined"** section — each with an "Unverified" badge, the reason ("Airdropped · you never bought this"), and one-tap Unhide. The real list stays clean.

Full write-ups: [docs/design-rationale.md](docs/design-rationale.md).

## Process

- **Before-states** are real screenshots captured from the Phantom app (Android).
- **After-states** designed in Figma, mobile-first, with desktop variations of each screen.
- Every feature ships with a short write-up: the problem, the design decisions, and the why.

## Assets

After-state frame exports (PNG) from Figma will be added under `assets/`.
