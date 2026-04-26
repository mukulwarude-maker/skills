# LinkedIn Algorithm Rules, SSI Model & 30-Day Plan

Reference for the LinkedIn ranking algorithm, headline and About optimization rules, SSI scoring model, and the 30-day activity plan.

---

## How LinkedIn Search Actually Works (2024–2026)

LinkedIn's search and feed are **LLM-ranked**, not term-frequency ranked. Key points:

### The 360Brew Foundation Model
- LinkedIn deployed a 150B-parameter foundation model called **360Brew** across 30+ predictive tasks including search ranking, job matching, and feed retrieval.
- The implication: **semantic relevance beats keyword density.** A profile that uses "built zero-downtime Kubernetes rollout strategies" will rank for "Kubernetes engineer" even without the exact phrase — because the model understands context.
- Keyword stuffing (repeating "DevOps Engineer DevOps Engineer DevOps" in the About) is penalized, not rewarded.

### JUDE (Job Understanding and Discovery Engine)
- LinkedIn's LLM-based job recommendation system matches candidates to roles semantically.
- A candidate with strong contextual signal ("deployed EKS clusters for 50M-user platform") will surface for "Senior DevOps" even without that exact job title in their profile — but only if the **semantic neighbors** are present (see `references/keywords-bank.md`).

### Recruiter Spotlights
LinkedIn surfaces candidates to recruiters using **Spotlight filters**. These are not optional ranking tweaks — they're binary gates. A dead profile does not appear in Spotlight-filtered searches even with perfect keywords.

The real Spotlight names (not marketing names):
- **Active Talent** — profile updated or activity in the last 30 days
- **More Likely to Respond** — replied to InMail within the past 60 days
- **Open to Work** — has Open to Work set (recruiter-only or public)
- **Internal Candidates** — applies to internal teams only
- **Past Applicants** — applied to this company before

**Recruiters narrow searches by Spotlight first, then by keywords.** A candidate with a perfect keyword profile who hasn't been active in 6 months is invisible.

### What the Algorithm Weights (ranked by impact)

1. **Headline** — the single heaviest-weighted text field. Indexed and surfaced prominently in search snippets.
2. **Skills section** — top 3 skills are disproportionately weighted. Endorsed skills index higher than unendorsed.
3. **Current title / recent experience** — recency matters; the most recent role gets highest weight.
4. **About section** — full text is indexed; keyword diversity here feeds semantic neighbor matching.
5. **Education** — field of study and institution keywords are indexed.
6. **Connections / network graph** — 2nd-degree connections in a company boost your ranking for that company's recruiter searches.
7. **Activity signals** — profile updates, post activity, comment activity feed into Spotlight filters.

---

## Headline Optimization Rules

The headline is the most-weighted ranking field in LinkedIn search. It is also the first thing a recruiter reads after your name.

### Character limits and rendering reality

- **Total cap:** 220 characters
- **Mobile feed/search card:** renders approximately the first **60–70 characters**
- **Desktop search snippet:** renders approximately the first **100–120 characters**
- **Characters 70–220:** indexed by the algorithm but not shown to humans in most views

**Rule:** Front-load identity + value into the first 60 characters. Use characters 70–220 for keyword density.

### What the first 60 characters must communicate

The first 60 characters are the only thing a recruiter sees in a crowded search result. They must answer:
- **Who are you?** (your function + level, e.g., "Senior DevOps Engineer")
- **What's the signal?** (one specific value indicator, e.g., "| AWS · K8s · Terraform")

### Headline formulas (credit by name — don't invent a new formula)

**Austin Belcak formula:**
> "I help [WHO] achieve [WHAT] using [HOW]"

Best for: consultants, coaches, solution-focused engineers. Less effective for pure IC roles.

**Jeff Su two-part formula:**
> Part 1: keyword-stuffed identity ("Senior DevOps Engineer | AWS · Kubernetes · Terraform")
> Part 2: quantified value ("| Cut deploy times from 2 hrs → 12 min across 40 microservices")

Best for: technical professionals. The pipe separator and keyword list satisfies the algorithm; the quantified result satisfies the human.

**Justin Welsh formula:**
> "I help X do Y, and I'm different because Z"

Best for: senior ICs or leaders who have a unique angle. Requires genuine differentiation.

### What to avoid

- "Software Engineer at Company Name" — wastes the entire 220 chars on one data point recruiters already see.
- Clichés: "results-driven", "passionate", "dynamic", "detail-oriented" — these are noise, not signal.
- Emoji overload — 1–2 strategic emoji (e.g., ⚡ 🚀) are fine; 6+ looks unprofessional.
- Outdated signals: "Open to Opportunities" in headline text — use the Open to Work official field instead.
- **India users:** do NOT put "Serving Notice Period" in the headline. Use the official Notice Period field under Open to Work (launched Oct 2025, recruiter-only visibility).

---

## About Section Optimization Rules

### Character limits and rendering reality

- **Total cap:** 2,600 characters
- **Desktop preview** (before "See more"): approximately **300 characters**
- **Mobile preview** (before "See more"): approximately **200 characters**

**Rule:** The first 200 characters must stop the scroll on mobile. If the opening doesn't hook, no one clicks "See more."

### The mobile hook test

Before writing any About section, ask: "If a recruiter on their phone saw only these 200 characters, would they click 'See more'?"

**Fails the hook test:**
- "Hi, I'm Mukul, a passionate software engineer with 4 years of experience in cloud infrastructure…"
- "Results-driven DevOps professional with expertise in CI/CD, Kubernetes, and AWS…"
- "I am a dedicated and motivated engineer who loves solving complex problems…"

**Passes the hook test:**
- "Cut 3 hours of daily deploy time to 8 minutes. Here's how my team shipped 40 microservices without a single rollback."
- "Every major outage at my last company was my call to fix. Here's what I learned reducing MTTR from 4 hours to 22 minutes."
- "I got my team from 0 to AWS certified in 90 days — without a single paid training day."

The pattern: **concrete result → implies expertise → creates curiosity.** Not a job title. Not "Hi."

### About structure (recommended)

1. **Hook** (first 200 chars) — concrete result, counter-intuitive view, or sharp question. ≤15 words per sentence. The hook is NOT a summary of your career.
2. **Identity paragraph** — who you are, what you do, level, market. Keywords placed naturally, not dumped.
3. **Achievement highlights** — 3–5 quantified wins with context. Use scale (users, services, cost, time).
4. **Current focus / what you're building** — signals recency and ambition.
5. **Skills cluster** — a keyword-dense paragraph or formatted list organized by category (helps semantic neighbor coverage). See `references/keywords-bank.md`.
6. **Call to action** — how to reach you, what you're open to, invitation to connect.

### Sentence length rule

**First 2 sentences must each be ≤15 words.** After the second sentence, normal prose is fine.

Why: LinkedIn's preview cut point lands at roughly sentence 2 on mobile. Short sentences also perform better in LLM ranking — they are easier to parse as semantic units.

---

## SSI (Social Selling Index) — Detailed Model

### What SSI actually is

SSI is LinkedIn's proprietary 0–100 score across 4 pillars of 25 points each. It is:
- **Computed daily** over a trailing 90-day behavioral window
- **Only visible to the profile owner** — recruiters do NOT see your SSI score
- **Not a direct ranking signal** — but the behaviors that lift SSI are exactly the behaviors that feed Recruiter Spotlights and search ranking

LinkedIn provides SSI free at: **linkedin.com/sales/ssi**

### The 4 pillars

**Pillar 1: Establish Your Professional Brand (25 points)**
Driven by profile completeness, content quality, and verified credentials.
- Profile completeness (All-Star status)
- Featured section populated with strong content
- About section with substance
- Recommendations (given and received)
- Workplace verification (Microsoft Entra / work email)
- Post content published (quality > quantity)

_Estimable from the PDF export — use the profile completeness data._

**Pillar 2: Find the Right People (25 points)**
Driven by search activity and profile view activity.
- Number of profiles viewed per week
- Searches performed using LinkedIn search
- Profile views received (which is partly a lagging indicator of other behaviors)

_Cannot be estimated from PDF — ask the user: "How often do you search or browse LinkedIn profiles?"_

**Pillar 3: Engage with Insights (25 points)**
Driven by post activity, comment activity, and engagement depth.
- Posts published (sweet spot: 2–5/week per Buffer study)
- Comments on others' posts (especially depth: 3+ participant comment threads per Van der Blom)
- Reactions given and received
- Shares of relevant content

_Cannot be estimated from PDF — ask the user: "Do you post or comment? When was your last post or comment?"_

**Pillar 4: Build Relationships (25 points)**
Driven by connection growth and DM activity.
- New connection requests accepted (quality matters — decision-makers weight more)
- InMail response rate
- DM conversations initiated and completed
- Connection acceptance rate

_Cannot be estimated from PDF — ask the user about their connection activity._

### Realistic SSI estimates by profile type

| Profile Type | Estimated SSI Range |
|---|---|
| Dead profile (no recent activity, incomplete) | 15–30 |
| Incomplete + some certifications + no posting | 25–35 |
| Complete profile + no activity | 35–45 |
| Complete profile + occasional posts (1–2/month) | 45–55 |
| Complete + weekly posts + comments | 55–65 |
| Complete + 2–5x/week posts + active comments + outreach | 65–75 |
| Thought leader: daily optimized content + high engagement | 75–85+ |

**Industry benchmark heuristics** (from sales-tooling vendors; LinkedIn does not publish official tiers):
- Average user: 40–50
- Active: 60–70
- Top 25%: ~65+ (industry-dependent)
- Top 10% / thought-leader band: 75–80+

### Realistic 30-day SSI lift

From an inactive baseline (SSI ~30–40), a sustained 30-day effort can lift SSI by **15–25 points**. Reaching 70+ from a dead baseline takes **30–45 days of consistent daily activity**, not a one-week sprint.

Do not promise overnight transformation. "Here's the 30-day arc" is more helpful than "just post more."

---

## 30-Day Activity Plan Details

### Why activity matters as much as content

A great profile with no activity loses to a decent profile with consistent activity. Here's why:
- **Active Talent Spotlight** requires profile update or activity within 30 days
- **More Likely to Respond Spotlight** requires InMail response within 60 days
- **Feed algorithm** surfaces active profiles in followers' feeds, which drives profile views, which lifts Pillar 2
- **Comment threads** with 3+ participants generate the most organic reach per Van der Blom 2024/2025 research

### Daily habits (15–20 min)

1. **View 10–15 profiles** of people at target companies (recruiters at these companies see you in their "who viewed" feed — this is a warm signal, not an intrusion). Feeds Pillar 2.
2. **Comment substantively on 3–5 posts** from peers, hiring managers, or industry voices. "Great post!" = algorithmic dead weight. A genuine 2–3 sentence comment that adds perspective = reach multiplier, especially if the thread reaches 3+ participants. Feeds Pillar 3.
3. **Respond to DMs within 24 hours.** LinkedIn's InMail response rate is tracked and feeds Pillar 4. Recruiters also screen for this.

### Weekly habits (1–2 hours)

1. **Post 2–5 times per week.** Buffer's 4.8M-post study found 2–5/week is the sweet spot — daily posting shows diminishing returns. Quality > frequency.
2. **Post format guidance:**
   - **Carousels (PDF slides):** still the highest organic reach format for thought leadership
   - **Polls:** ~1.64× reach multiplier per Van der Blom 2025 data. Use for genuine questions, not engagement bait.
   - **Text posts with a strong hook:** second most effective if the opening line stops the scroll
   - **Video:** high reach but high production barrier — only recommend if the candidate already does this
3. **Avoid external links in the post body.** Practitioner data (Van der Blom, Richard van der Blom 2025 Algorithm Report) shows ~25–50% reach reduction for posts with links in the body — even though LinkedIn's Sr. Director publicly stated in Aug 2025 that there's no intentional penalty. Put links in comments instead.
4. **1–3 hashtags max.** LinkedIn drastically reduced hashtag weight in 2024–2025. Creator Mode and "Talks About" topics were retired early 2025. More than 3 hashtags looks dated.
5. **Send 2–3 personalized connection requests** to decision-makers, hiring managers, or peers at target companies. Personalized note = higher acceptance rate. Generic "I'd like to add you to my network" = mostly ignored.

### Monthly habits

1. **Request 1–2 new recommendations** from current or past managers, direct reports, or senior peers. 5–10 recommendations is the credible band for mid-senior professionals.
2. **Sync new certifications** (AWS, GCP, Microsoft Learn, CKA/CKAD, Terraform Associate, etc.) into Licenses & Certifications and tag them to relevant skills. This is the modern **Verified Skills** mechanic — the replacement for the discontinued Skill Assessment badges.
3. **Complete workplace verification** via Microsoft Entra Verified ID or work email if not done yet. LinkedIn's own data: verified members see ~60% more profile views.

### One-time setup (do this week)

1. **Set Open to Work** — recruiter-only mode for mid/senior; public banner for freshers/juniors.
   - LinkedIn data: 14.5% positive InMail response WITH the recruiter-only signal vs 4.6% WITHOUT (~3× lift)
2. **Custom LinkedIn URL** — `linkedin.com/in/firstname-lastname`. Doesn't affect LinkedIn's own search but improves Google SEO when recruiters search the candidate's name.
3. **India users only:** Fill the official **Notice Period** and **Expected Annual Salary** fields under Open to Work settings (launched October 2025, recruiter-only visibility). Do NOT put this information in the headline.

---

## What LinkedIn Does NOT Penalize (Common Myths)

- **AI-assisted writing:** LinkedIn does not ban AI content. It down-ranks unedited, generic AI output that triggers low engagement. Edit the AI draft to sound like you.
- **Multiple posts per day:** not penalized, but typically wastes organic reach. 2–5/week performs better.
- **Hashtags:** not penalized, but weight is negligible. Stop obsessing.
- **Engagement pods (coordinated inauthentic engagement):** LinkedIn's 2025 enforcement produced documented shadow-bans (60–90 day reach collapse). **Never recommend engagement pods under any circumstance.** This is a real career risk.
