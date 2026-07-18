# Example: Startup plan reality-check

A life-path decision with real money on the line — the case the skill was built for.

Both responses below are single, unedited runs of the same prompt
(Claude Sonnet, `claude -p`) — one without the skill loaded, one with it.
Single runs, so treat differences as directional, not proof.

## Prompt

> I want your 1000% honest take. I'm 34, marketing manager, planning to hand in my notice next month to build a SaaS for restaurant inventory management. I have 14k EUR saved (about 6 months of runway), no co-founder, and I can't really code yet - I've done maybe 30 hours of tutorials and I'm using AI coding tools for the rest. I validated the idea by talking to two restaurant-owner friends who said they'd 'definitely try it'. My plan is MVP in 8 weeks, first paying customer by month 3, ramen profitability by month 6. Be honest with me.

## Without the skill

No sugar-coating, since you asked for it straight:

**The plan has a fatal flaw before we even get to the business: you can't build this yourself.** 30 hours of tutorials plus AI coding tools does not get you to a production SaaS that restaurants trust with their inventory data. AI tools accelerate someone who already knows what "good" looks like — they don't replace the judgment. You will burn weeks debugging things you don't understand, ship security/data bugs you can't see, and your "8-week MVP" will likely take 4-6 months solo. This is the single biggest risk in your plan and it's not really a maybe.

**Your validation is not validation.** "Definitely try it" from two friends costs them nothing to say and commits them to nothing. That's politeness, not market signal. Real validation looks like: they pay you money now (even a deposit) for something that doesn't exist yet, or they show you the spreadsheet/system they currently limp along with and the actual pain of using it. Restaurant inventory management is also a brutally crowded, low-margin space (MarketMan, Toast, xtraCHEF, Craftable, etc.) — you need to know why your two friends' current tools failed them specifically, not just that they said yes to you.

**The timeline is fantasy stacked on fantasy.** MVP in 8 weeks (as a non-coder) → first paying customer month 3 → ramen profit month 6, on 14k EUR / 6 months runway. Each of those milestones individually has maybe a 30-40% chance of landing on time for an experienced solo technical founder. Chained together, with a non-technical founder, you're looking at single-digit percent odds of hitting all three on schedule. And "ramen profitable by month 6" for a B2B SaaS selling to restaurants — an industry with notoriously slow sales cycles and owners who are extremely price-sensitive — is aggressive even for a founder who *can* code.

**No co-founder is a specific problem here, not a general one.** You need someone who can build fast while you sell, or you need to genuinely become a builder yourself over months, not weeks. Solo-non-technical-founder-plus-AI-tools is one of the highest-mortality combinations in early-stage SaaS right now — it's a popular narrative on Twitter, survivorship bias is doing a lot of work in the stories you've seen.

**What I'd actually recommend:** Don't quit yet. Spend the next 4-8 weeks, nights/weekends, doing two things in parallel: (1) get 5-10 restaurant owners to commit real money or a real pilot contract before you build anything, and (2) build a rough prototype with AI tools to see firsthand how far you get and how much you still don't understand. If after 2 months you have paying pilot commitments AND you've proven to yourself you can actually ship, THEN quit with a much shorter runway need and a much higher confidence number. Quitting now, on this timeline, with this validation, is the expensive way to learn what a cheap 2-month test would tell you for free.

Confidence on this take: high on the structural risks (technical capability gap, weak validation, timeline compression) — those are just math and pattern-matching against how these things usually go. Lower confidence on exact odds since I don't know your specific execution speed or the restaurant friends' actual pain level — but directionally, this isn't close.

## With zero-sugar

**Verdict:** The whole plan rests on validation that never actually happened — two friends saying "I'd definitely try it" is a social nicety, not market signal, and every date after that (8-week MVP, paying customer by month 3, ramen-profitable by month 6) is a guess stacked on that guess. That's the finding that explains the others, not just the first one.

**What's broken (worst first):**

1. **Your validation isn't validation.** "Friends said they'd try it" costs the responder nothing — no money, no time, no switching cost from whatever they use now (probably a spreadsheet, or nothing). Real validation looks like: a non-friend restaurant owner paying a deposit, signing a letter of intent, or actively using a scrappy prototype for two weeks. You have zero data points on whether anyone will *pay*, which is the only number that matters for month 3 and month 6. This is fact, not opinion: "would try" and "will pay" are different behaviors, and the gap between them is where most B2B SaaS ideas die.

2. **You're entering a market with real, entrenched competitors, and you likely don't know the ones that matter.** Restaurant inventory/back-of-house software already has established players (MarketMan, Apicbase, Toast xtraCHEF, Restaurant365, Craftable) that integrate with POS systems, suppliers, and accounting. Restaurant owners' actual pain isn't "no inventory tool exists" — it's "the tool needs to talk to my POS and my supplier ordering, or it's just another spreadsheet with extra steps." If your MVP doesn't do that, it competes with a free spreadsheet, not with a $200/month category leader. I'm confident this competitive landscape exists; I'm less certain exactly which integration is make-or-break for your specific wedge — that depends on positioning you haven't described.

3. **The technical gap is the load-bearing risk, and you're underpricing it.** 30 hours of tutorials plus AI coding tools gets you a working CRUD prototype for a demo. It does not reliably get you: POS integrations, multi-user permissions, reliable auth, payment processing, and the debugging skill to fix it when the AI-generated code breaks in a way that isn't a simple prompt-fix (race conditions, security holes, data integrity bugs). When you hit that wall — and with no coding background, you will — you have no fallback except stalling or paying for help you can't afford. This is where "8 weeks" quietly becomes "5 months," and by then a third of your runway is already gone.

4. **Your runway is thinner than "6 months" implies.** €14k / 6 months = ~€2,300/month. That figure has to cover personal living costs *and* business costs (hosting, AI tool subscriptions, any paid tools, possibly incorporation) *and*, if you're in Germany, self-employed health insurance, which is a real, mandatory monthly cost that isn't optional and isn't small. I don't know your exact number here — you should check it precisely before quitting — but if it eats a few hundred euros a month, your real runway is closer to 4-5 months than 6. That's less time than your own plan needs even if everything goes right.

5. **No co-founder means no one catches the two failure modes you're most exposed to** — technical (see #3) and the fact that you'll be doing product, engineering, sales, and support alone. That's not automatically fatal, but it means every delay compounds instead of getting absorbed by a second person.

6. **Three optimistic milestones stacked in sequence multiply the odds of missing all of them.** MVP-in-8-weeks, paying-customer-by-month-3, and profitable-by-month-6 each individually have maybe reasonable odds for a strong solo technical founder. You're not that yet. Stacked together, the probability of hitting all three isn't the average of the three — it's closer to the product, which is much lower.

**What actually holds up:**
Marketing skill is a genuinely rare and useful edge — most solo-founder SaaS attempts fail at customer acquisition, not at building something, and you're coming at this from the acquisition side. Picking a specific, painful, recurring problem (inventory) instead of a vague idea is also smarter than average. That's real, not consolation.

**If you fix only three things:**
1. **Don't quit yet.** Get 2-3 real commitments first — paid pilots, deposits, or LOIs from restaurant owners who are not your friends — before you touch your notice period. This is the single highest-leverage move: it turns your biggest unknown into a known before you burn runway on it.
2. **Test the technical risk cheaply, before quitting.** Build the ugliest possible version (even a form + spreadsheet backend) and get it in front of a real (non-friend) restaurant owner for two weeks. If it breaks or nobody uses it, you've learned that for €0 and zero notice period instead of month 4.
3. **Recalculate real runway with actual numbers** — German self-employed health insurance, tools, and business costs subtracted from the €2,300/month, not folded into it. If that number gets ugly, keep freelance/part-time marketing income running alongside this for the first few months instead of a clean break.

Confidence check: the runway math and competitive landscape are close to fact. The "8 weeks becomes 5 months" claim is my calibrated read based on how these timelines usually go for non-technical solo founders using AI tools — not a guarantee, but not a wild guess either. Whether to quit outright vs. build nights/weekends first is a risk-tolerance call, not something I can call "correct" for you — but the plan as stated doesn't earn the "quit now" version of that call yet.
