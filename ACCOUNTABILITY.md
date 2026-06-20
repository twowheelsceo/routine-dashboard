# Accountability & Reminders — the "stay on track" engine

Built from a web-research pass on what actually changes behavior. The whole system rewards **showing up daily** and makes **missing cost something real**. Synced across devices via Supabase.

## The 5 proven mechanics (and the evidence)
1. **Consequences that bite — stakes to your rival.** Miss any 🔒 non-negotiable by **midnight** → you auto-owe your rival **$5** (escalates on repeat misses). Fuses the three strongest levers: loss aversion + "anti-charity" (money to someone you don't want to give it to = your rival) + head-to-head. *StickK financial-stakes goals succeed far more than stakeless (~3×+); anti-charity beats neutral; Beeminder's escalating pledge calibrates the sting.*
2. **If-then cue reminders, not time-only pings.** Every habit shows its cue ("after coffee → train"). *Gollwitzer & Sheeran meta-analysis, ~94 studies: d ≈ 0.65 — the best-supported reminder design there is.*
3. **A subscribed `.ics` calendar** (`routine.ics`) — the one reminder method that **reliably fires on a locked phone with the app closed**, no backend. 8 daily events with alarms. *ICS RRULE+VALARM fires locally regardless of refresh lag; the most reliable no-infrastructure option vs. flaky iOS web-push.*
4. **Side-by-side streaks + a forgiveness budget.** 2 **streak-freezes per month** absorb the first slips so one miss doesn't trigger the "what-the-hell, I quit" spiral. *Duolingo found adding limited freezes measurably raised retention; capped small so the net doesn't kill the pressure.*
5. **Weekly mutual settlement.** Each verifies the other and the tally settles — a scheduled human check-in. *Matthews (Dominican U.): weekly progress report to a person = ~76% success vs ~43% for goals merely thought about.*

## How it works in the app
- **Non-negotiables (🔒):** Train · Protein · Deep-work block · Study/skill · Evening review. Miss any one = the day is a miss.
- **Today tab** shows "🔒 Non-negotiables · X/5 · $Y on the line · finish all 5 before midnight or you owe [rival] $Y."
- **At midnight** the day locks. The app reconciles past days on open: a missed day spends a freeze if you have one, otherwise adds the stake to what you owe your rival.
- **Arena tab** shows the live tally (Aidan owes / Dante owes), freezes left, and an **"I paid up — reset my tally"** button (each person settles their own).
- **Reminders:** Today → "Turn on phone reminders" → subscribe to `routine.ics` once → OS alarms fire all day even with the app closed.

## What we deliberately did NOT do (it backfires)
- **No hard zero-reset streaks** → triggers the what-the-hell effect. (Hence the freeze budget.)
- **No notification spam / sleep-hour pings** → #1 cause of opt-out. The .ics fires only at the scheduled blocks.
- **No shallow badge-spam** → overjustification erodes intrinsic motivation (Deci/Koestner/Ryan, 128 studies). Points stay *informational* (head-to-head signal), not the point.
- **No self-report-only honesty hole** → your rival is the referee (mutual weekly verify).

## Tunables
- Stake amount (default **$5/missed day**) and the stake description live in the shared synced settings.
- Freezes refill to **2 at the start of each month**.
- Edit the daily reminder times in `routine.ics`.

Source of truth: the live dashboard. Full habit science → [[HABITS]].
