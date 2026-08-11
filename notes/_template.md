---
title: "<Claim with the verdict in it, not a topic label>"
slug: YYYY-MM-DD_short-kebab-slug
date: YYYY-MM-DD
project: <the origin project this came out of>
stack: <dbt · DuckDB · Snowflake · ...>
verdict: <Prediction held | Prediction failed | Mixed | Inconclusive>
kind: <experiment | migration | workflow | benchmark | postmortem>
status: <draft | published>
source_records: <paths in the origin repo that back this up>
---

<!--
DRAFTING NOTES — delete before publishing.

Two tiers, same as the lab:
  - The origin repo holds the raw records. That is the vault.
  - This file is the derived, curated view. Write it later, deliberately.
  Never write a notebook entry knowing it will be published. The moment the
  notebook performs, it stops being a usable instrument.

TITLE RULE. Most people read only titles, so the title carries the finding.
  yes: "Porting 65 dbt models to Snowflake: zero model changes, parity proven"
  no:  "Notes on the Snowflake migration"

WHAT MAKES IT A WHITE PAPER RATHER THAN A POST. Five things, all of which
expose the work to being wrong:
  1. The prediction, stated before the result, in falsifiable form.
  2. Numbers with the method that produced them attached.
  3. Scope limits, named. What was NOT tested is the separator between a
     report and a pitch.
  4. Negative results kept in. Publish the failures at equal fidelity.
  5. Cost accounted for. Time, iterations, money.

ANTI-TELLS. Cut on sight:
  - Opening with an industry trend sentence.
  - Round numbers with no method ("10x faster").
  - Screenshots standing in as evidence.
  - A conclusion broader than what was measured.
  - Any sentence grading the significance of your own result.
  - Announcing candor ("worth noting", "to be honest", "worth stating").
    See the voice guide, principle 3 — it is a pattern rule, not a phrase
    blocklist, because a blocklist just teaches the next synonym.
-->

# <title>

<Standfirst: two or three sentences. What the experiment tested, and the shape
of the answer. No suspense, no throat-clearing.

REGISTER RULE for this paragraph specifically: make the EXPERIMENT the subject,
not yourself. First person belongs in the body, where "what I predicted" and
"the number that surprised me" are doing honest work. In the opening it turns
into setup-and-payoff — "I did X to find out Y. The answer:" — which is feature-
article voice against a lab-report body, and the mismatch reads as bragging even
when every word is factual. Lead with the question. Land on a fact.>

| | |
|---|---|
| Date | |
| Project | |
| Stack | |
| Verdict | |

## What I predicted, before running it

<The hypothesis as written at the time, not reconstructed afterward. State it
so it could have failed. Then say what failure would have looked like.>

## Method

<What was actually done, in enough detail that someone could repeat it.
Include what was deliberately left out of scope and why.>

## Results

<Table. Numbers with their measurement method. Then prose on the one or two
results that were not what you expected.>

## <The interesting middle section>

<The gap inventory, the failure analysis, the thing that surprised you. This
is usually where the real content is. Include the problems your own first fix
caused.>

## What it cost

<Wall clock, money, and where the effort actually went. If the expensive part
was not the part everyone assumes, say which part it was.>

## What this does not prove

<The scope limits, itemized. Be specific about what you did not test rather
than gesturing at "further work needed".>

## What I would do differently

<Concrete. One or two things.>

## Receipts

<Where the underlying records live. Link the public surface; name the private
artifacts without linking them.>
