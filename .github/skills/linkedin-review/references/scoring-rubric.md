# LinkedIn Profile Scoring Rubric

The total score is 100 points across 6 dimensions. Use this rubric for every review — same issue = same deduction.

---

## Dimension 1: Completeness (15 points)

Measures whether the profile is set up to achieve LinkedIn "All-Star" status and is using the platform's visibility tools.

**Start at 15 and subtract:**

| Issue | Deduction |
|-------|-----------|
| No profile photo | -4 |
| Default grey/blue banner (no custom banner image) | -2 |
| About/Summary section missing or fewer than 50 words | -3 |
| Featured section not used (no pinned posts, media, links, or certificates) | -2 |
| No Open to Work signal set (recruiter-only OR public) — for active job seekers only | -2 |
| Fewer than 5 sections with content (incomplete profile) | -2 |
| Custom profile URL not set (still has random numbers) | -1 |
| No verified workplace (Microsoft Entra or work-email verification) | -1 |

Floor at 0.

**Note on Open to Work:**
- **Freshers / juniors:** public #OpenToWork banner is fine (more visibility, less stigma at entry level).
- **Mid / senior candidates:** recruiter-only mode strongly preferred (~3× InMail response lift per LinkedIn data). Public banner at senior level can signal desperation to some hiring managers.

---

## Dimension 2: Discoverability & Keywords (25 points)

Measures how well the profile is indexed by LinkedIn's LLM-powered search for the target role.

**Scoring approach:**

1. Extract 15–25 keywords from the target JD (tools, technologies, methodologies, soft skills, seniority terms).
2. Count how many appear in the LinkedIn profile (headline + about + experience + skills).
3. Compute match rate: `keywords_matched / total_keywords`.

| Match rate | Points |
|------------|--------|
| ≥90% | 25 |
| 80–89% | 22 |
| 70–79% | 18 |
| 60–69% | 14 |
| 50–59% | 10 |
| 40–49% | 6 |
| <40% | 3 |

**Additional deductions (applied after tier):**
- Fewer than 15 skills listed (out of 100 available slots): -4
- Top 3 skills not aligned with the JD's primary requirements: -4
- Skills section is blank: -8
- Only abbreviations OR only full names (not both — e.g., only "K8s", never "Kubernetes"): -2
- Critical JD keyword appears nowhere in the profile (not headline, not about, not experience, not skills): -2 per missing critical keyword (cap -6)
- Keywords only in skills section, never in bullets (search algorithm weights contextual use): -2

Floor at 0.

---

## Dimension 3: Headline & About Hook (20 points)

Measures the quality and impact of the two highest-visibility profile sections.

### Headline (10 points)

**Start at 10 and subtract:**

| Issue | Deduction |
|-------|-----------|
| Default / job-title-only headline ("Software Engineer at Company X") | -6 |
| First ~60 characters show no value proposition (just title + company name) | -4 |
| No keywords in the headline at all | -3 |
| Headline under 80 characters (leaving indexable keyword space unused) | -2 |
| Clichés without substance ("results-driven", "passionate about", "dynamic") | -1 |
| Headline includes outdated signals ("Skill Assessment badge", etc.) | -1 |

Floor at 0.

### About Section (10 points)

**Start at 10 and subtract:**

| Issue | Deduction |
|-------|-----------|
| Opens with "Hi, I'm…" or "I am a results-driven professional…" (scroll-stopper failure) | -4 |
| First 2 sentences are > 15 words each (hook fails before "See more" on mobile) | -3 |
| About is under 200 words (major opportunity loss) | -3 |
| No quantified achievements (no numbers, percentages, or scale anywhere) | -2 |
| No call to action (how to reach you, what you're open to) | -1 |
| No skills cluster / keyword paragraph near the end | -1 |
| Reads as a resume summary (responsibilities) rather than a story (impact) | -2 |

Floor at 0.

---

## Dimension 4: Experience Quality (15 points)

Measures whether the experience section tells a story of impact with the specificity needed to rank and impress.

**Sample the experience section.** For each bullet, classify:
- **Strong (STAR)** — Action verb + context + measurable outcome. E.g., "Migrated 20 microservices to EKS, reducing deploy time from 45 min to 8 min"
- **Partial** — Action verb + context, no outcome. E.g., "Built CI/CD pipelines using GitHub Actions"
- **Weak** — Passive voice or pure responsibility. E.g., "Responsible for infrastructure monitoring"

Compute: `(strong × 1.0 + partial × 0.5) / total_bullets`

| Ratio | Points |
|-------|--------|
| ≥0.80 | 15 |
| 0.65–0.79 | 12 |
| 0.50–0.64 | 9 |
| 0.35–0.49 | 6 |
| 0.20–0.34 | 3 |
| <0.20 | 1 |

**Additional deductions:**
- Uses "Responsible for…" or "Worked on…" opener: -1 per occurrence (cap -3)
- No numbers/percentages/scale anywhere in experience section: -3
- Any single role has 0 bullets (just dates and title): -2 per role (cap -4)
- Roles listed in non-reverse-chronological order: -2
- Most recent role has fewer bullets than older roles: -2

**Level adjustment:**
- **Freshers:** lenient. Internship/project bullets that are Partial but honest are acceptable.
- **Seniors:** strict. No scale metrics = failing the role. A senior engineer without numbers looks like they're hiding something.

---

## Dimension 5: Social Proof & Verified Credentials (15 points)

Measures trust signals that tell recruiters this is a credible, active professional.

**Start at 15 and subtract:**

| Issue | Deduction |
|-------|-----------|
| 0 recommendations | -5 |
| 1–2 recommendations only | -3 |
| 3–4 recommendations (for senior candidates — 5–10 is the credible band) | -1 |
| Top 3 skills have 0 endorsements | -3 |
| No verified workplace (via Microsoft Entra Verified ID or work email) | -3 |
| Certifications listed but not synced to LinkedIn (so no verified badge) | -1 |
| Certifications are outdated or from discontinued programs (e.g., LinkedIn Skill Assessments) | -1 |
| Publications, honors, or patents exist but are not listed | -1 |

Floor at 0.

**Note:** LinkedIn Skill Assessments were discontinued and badges purged in 2024. Do NOT recommend them. The replacement is **Verified Skills** — certifications synced from AWS, Microsoft Learn, Google Cloud, CKA/CKAD, etc., or workplace verified via Microsoft Entra or work email.

---

## Dimension 6: Resume Consistency (10 points)

**Only scored if a resume PDF is also provided.** If no resume, redistribute these 10 points proportionally across the other 5 dimensions when presenting the total.

**Start at 10 and subtract:**

| Issue | Deduction |
|-------|-----------|
| Role title on LinkedIn differs from resume (not just formatting difference) | -2 per mismatch (cap -6) |
| Date range mismatch (>1 month discrepancy) | -2 per mismatch (cap -4) |
| Company name mismatch | -2 per mismatch (cap -4) |
| Role present on resume but missing from LinkedIn (or vice versa) | -3 per missing entry |
| Skills on resume not reflected in LinkedIn Skills section | -2 |
| Summary/About tone is completely inconsistent (one is humble, one is grandiose) | -1 |

Floor at 0.

**Why this matters:** Recruiters cross-check LinkedIn vs resume vs GitHub for tech roles. A title mismatch (even if explainable) creates a trust deficit. Date mismatches trigger background check flags.

---

## Final Grade Mapping

| Total | Grade | Verdict |
|-------|-------|---------|
| 90–100 | A | Recruiter-magnet profile. You're showing up and getting clicked. |
| 80–89 | B | Strong profile, minor tweaks push it to A. |
| 70–79 | C | Solid foundation — real gaps in discoverability or social proof. |
| 60–69 | D | Major gaps. Low recruiter visibility, likely missing Spotlight filters. |
| <60 | F | Mostly invisible to recruiter search. Rewrite before applying anywhere. |

---

## Calibration Reminders

- **Don't inflate.** A 75 should feel like "solid foundation, real gaps." Not "pretty good."
- **Don't crush.** A 60 should feel like a 2–3 week rewrite project, not a catastrophe.
- **Adjust for level** on Dimensions 4 and 5. A fresher without recommendations is expected; a senior with 0 recommendations is a yellow flag.
- **Adjust for market** on Dimensions 1 and 5. Photo is near-mandatory in India (pass-through); no photo is fine internationally.
- **Quote the profile directly** for every finding. "Your headline says X" beats "your headline is generic."
- **Content-strong, signal-dead:** When Dimensions 2–4 score well (75+) but SSI / activity is clearly low, don't recommend a rewrite. The text is fine. The signal is dead. Focus the action plan on activity, not rewrites.
