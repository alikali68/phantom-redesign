# Design Rationale — Phantom Redesign

The short write-ups behind each feature: the problem, what changed, and why.

---

## Feature 1 — Trade-page transparency & safety

**Problem.** Phantom's Trade flow opens leveraged positions with **10x leverage pre-selected**. The leverage sheet shows Liquidation and Distance as "—", so users can't see where they'd be liquidated. Risk disclosure is a single line ("Boost gains and losses"). Fees and price impact are never shown before confirming.

**What I changed.** (1) Added a pre-confirm summary card: you pay X → position size → each fee on its own line, liquidation price as a real number, distance to liquidation as %. (2) The leverage selector now defaults to **2x**, with plain-language labels ("2x = a 50% drop liquidates your position"). (3) Replaced the one-liner with a real risk-warning block.

**Why.** Leverage is where beginners lose money fastest. Showing the liquidation price *before* confirm turns an invisible risk into an informed choice.

---

## Feature 2 — Activity-tab address-poisoning guards

**Problem.** Attackers send tiny "dust" transactions from lookalike addresses, poisoning the Activity history. Users copy the attacker's address from history and send funds to it — one real victim lost $264K this way.

**What I changed.** (1) Dust transactions from suspicious lookalike addresses get a grey **"Suspicious"** badge and are visually dimmed. (2) Tapping "copy address" from History now shows a warning sheet — *"Verify this address. Scammers poison histories with lookalike addresses."* — with an "I verified — copy" confirm button.

**Why.** The copy button is the exact moment of danger. A 2-second check there prevents irreversible loss.

---

## Feature 3 — Token-list spam quarantine

**Problem.** Airdropped scam tokens land in the main token list, sitting side by side with real holdings with zero distinction. Users didn't buy them, can't sell them, and hiding them takes 3–4 taps deep in menus — so the list stays polluted.

**What I changed.** (1) Unknown tokens are auto-detected and moved into a **"Quarantined"** section — out of the main list. (2) Each quarantined token shows an "Unverified" badge, the reason ("Airdropped · you never bought this"), and one-tap Unhide. (3) Manual Hide from the token's ••• menu for anything the detector misses.

**Why.** The home screen is trust surface #1. If it looks like a spam folder, users stop trusting everything else.
