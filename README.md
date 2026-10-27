# TakeMeter

> ### 👋 Start here
>
> **New to this repo? Read [RUNNING.md](RUNNING.md) first** — setup, the
> notebook, the baseline, and what to do when something breaks.
>
> Once `python test.py` passes:
>
> ```bash
> head -5 data/practice_labels.csv     # the shape your labels.csv needs
> ```
>
> Then open `takemeter.ipynb` **in this folder** — in VS Code, or with
> `jupyter notebook` if you prefer. Pick the kernel: the `.venv` inside this
> project. Run section 1, which reports the hardware you'll be training on.
> Everything else waits until you have data.
>
> Nothing to upload, nothing to connect, no accounts and no keys. The notebook
> runs on your machine and writes next to your code.
>
> **The rest of this file is your submission.** Fill it in as you go.

---

## What This Does

TakeMeter classifies posts from r/stocks, a Reddit forum focused on the stock market, into several distinct categories. Analytical posts contain some research and analysis, typically with facts or statistics to back up the poster's claims. Advice posts are the user asking the broader community for advice or feedback about their market observations or trading positions. News posts are based upon recent news articles regarding publically traded companies as well as the market in general. TakeMeter will categorize these posts based on their content into these categories  


---

## Label Taxonomy

### `analysis`

**Definition:** analytical posts, with at least one supporting argument or fact, with the majority of the post coming from the user's original commentary and observations

**Example 1:**
13 of the last 19 midterm years had a 10% drop in them

Most midterm yrs have a scary drop in them & people act surprised every time

Vote is Nov 3 so I looked at the history.

In 13 of the last 19 midterm yrs, S&P fell 10% or more at some point during the year.

The midterm year is the weakest of a president’s 4 more often than not.

2018 is 1 people remember. It slid almost 15% between Election Day <> Christmas Eve, with the Fed raising rates at the same time.

So if your account looks bad this fall, that’s normal for a midterm year.

Not sure how it goes from here ofc.

**Example 2:**
Hayden brown is bad for Upwork

Upwork cuts off 25% of its staff sighting slower growth and AI productivity gains

Upwork doesn’t need Hayden Brown. She made the platform more expensive and worse. Her whole thing is “more AI,” while clients and freelancers leave, and Connects become a tax. We want more work, not AI experiments. they should find someone who actually runs a marketplace.

She turned upwork into a casino. Where everyone loses. Even top freelancers keep bleeding money, and clients complain about higher fees and worse results.

### `news`

**Definition:** a headline and accompanying news article, or a summary of an announcement, with the majority of content coming from the article or summary itself and only minimal commentary or analysis from the user

**Example 1:**
South Korea Current Account Surplus Surpasses Germany and Japan Combined in Q2

In the second quarter, South Korea achieved a historic current account surplus of $116.63 billion, marking the first time its surplus exceeded the combined total of Germany and Japan since joint statistical tracking began in 1996.

Ranking second globally behind China, South Korea saw its quarterly surplus expand more than fourfold compared to the previous year. This massive surge was largely driven by a boom in semiconductor exports, propelled by rising global prices and strong demand for chip products.

Driven by this momentum, forecasts project the nation's annual surplus could approach $500 billion, potentially raising its surplus-to-GDP ratio to an unprecedented 18.8 percent.

Despite these record achievements, experts warn against over-reliance on a single sector and urge South Korea to diversify its industrial landscape. Other key domestic industries, including automobiles, electric vehicle batteries, shipbuilding, and petrochemicals, continue to face challenges from slowing demand, global market volatility, and aggressive price competition from China.

Furthermore, analysts highlight that the current account boom relies heavily on elevated chip prices rather than significant volume increases, leaving the broader economy vulnerable if the semiconductor supercycle cools down or if trading partners build domestic capacity. To safeguard long-term stability, economists advise leveraging this record capital inflow to restructure underperforming sectors and fortify national economic fundamentals.

https://en.koreadaily.com/south-korea-current-account-surplus/

**Example 2:**
Trump purchased up to $5 million of SpaceX bonds days before major space order

https://www.cnn.com/2026/10/08/investing/trump-5-million-dollars-spacex-bonds

Just two days before launching an effort to slash red tape for commercial space transportation, President Donald Trump last month purchased up to $5 million of bonds issued by SpaceX, a major federal contractor run by Elon Musk, according to ethics filings made public on Thursday.

Beyond SpaceX debt, Trump purchased up to $25 million of Meta shares, up to $6 million of Microsoft stock and a smaller amount of Oracle shares, filings show.

Those trades occurred weeks before Trump convened Musk, Meta CEO Mark Zuckerberg and other AI leaders for a White House summit. Notably, Trump forcefully pushed back on calls for a regulatory crackdown to address safety fears, opting for a lighter touch instead.

Looks like administration is going to continue to support SPCX for a long time. It seems insane and awful but at the same time, don't bet against this stock seems like.


### `advice`

**Definition:** a user's post asking the broader community for their advice and opinions on the market or their own holdings or trading pattern, with the majority of the post being the user's original content geared toward a question

**Example 1:**
Question about selling a small but profitable position.
Hi,
Trying to learn best practices. I have 10 shares of Apple that I have not added to in over a year. But I noticed that this small number is up 102% in my dashboard.

Even if I did not expect a change in the remainder of the year… is it always a good idea to cash this out for doubling the worth?
Full disclosure: I’m asking because I am finally committing to ETF positions. Not against Apple, but don’t want to waste an opportunity at more than 100% increase.
Thanks in advance!

**Example 2:**
Looking for some honest feedback

Fairly new (Europan) investor here, about two years in now. My plan was originally to have a 90/10 split between an all world ETF and some individual stock on the side. Unfortunately, that rather spiraled out of control and the split is rather 60/30 at this point (with 10% in cash currently), and I'm looking to bring that average back up in favor of the ETF.

That said, I'm looking for some honest (can be brutal) feedback on my individual stock. I'm down on most of them, mainly because the last few months have been quite brutal for tech. Currently holding:

CRDO: 5% of my overall portfolio, 26% down
SE: 5% of my portfolio, 18% down
MDA: 4% of my portfolio, 31% down
PGY: 3% of my portfolio: 5% up
GTLB: 2,5% of my portfolio, 3% up
PL: 2% of my portfolio, 46% down
NBIS: 2% of my portfolio, 17% down
DRTS: 2% of my portfolio, 5% down
FSLR: 2% of my portfolio, 6% down
RDW: 1,5% of my portfolio, 37% down
RTX: 1% of my portfolio, 12% down

What I've learnt so far:

That I was too agressive when it came to opening new positions. Bought (too) heavily into PL for example when it was about 50% down from ATH, and I should have opened with a way smaller position.

Keep the dabbling in biotech to a minimum. Was (heavily) involved in SLS for about 6 months, first made quite a bit of money on that, then lost all of that profit and probably record a very narrow loss before I got out. The DRTS position is enough I think.

For the record, I'm not worried about short term. I don't need the money and I've got a plenty long horizon of 10+ years if need be. I can also stomach the volatility. I guess I'm just curious if I could have done something different, or if there's anything on this list that I should just cut loose.

### The hardest boundary

**Which two labels:** analysis and advice

**The decision rule I used every time:**

If most of the content is based on the user's own situation (holdings, P/L, goals, history) and asks for the community's input, then the post is asking for advice. If the majority of the post is general market analysis, discussion and diligence, with the user merely asking for feedback on their research, then the post is analysis.

---

## The Dataset

<!-- Where you collected from, how you labelled, your counts, and three hard
     cases. -->

**Where the posts came from:**

**How I labelled them:** <!-- Cold first? Pre-labelled with AI and corrected?
Say so plainly — the disclosure is required, not penalised. -->

**Counts per label:**

| Label | Count | Share |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |
| **Total** |  | 100% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**2.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**3.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

---

## The Training Run

<!-- Your starting model, your settings, and anything you changed and why. -->

**Base model:**

**Settings:** <!-- epochs, learning rate, batch size, seed -->

**Anything I changed from the defaults, and why:**

**Split sizes:** <!-- train / val / test, and per-label counts in the test
split. If a label had fewer than about 8 in test, say so — it explains a lot
of next unit's variance. -->



---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Moment 2**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Pre-labelling disclosure:**

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy |  |  |  |
| Macro F1 |  |  |  |
| F1 — `label_one` |  |  |  |
| F1 — `label_two` |  |  |  |

**What I predicted before I looked:**
<!-- Milestone 1 asks you to write this BEFORE seeing the trained numbers. A
     prediction made afterwards isn't one. -->

**What the gap actually means:**
<!-- If the baseline matched your trained model, your fine-tuning added
     nothing — and that is a real finding, not a failure. Say it plainly. -->



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

| true \ predicted |  |  |  |
|---|---|---|---|
| **** |  |  |  |
| **** |  |  |  |
| **** |  |  |  |

**My biggest off-diagonal number, and what it means:**
<!-- Not "the model made mistakes" — WHICH boundary it didn't learn, and which
     direction. "7 real analysis posts were called hot_take and only 3 went the
     other way" is a direction, not just an error rate. -->



---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |

**Diagnoses**

<!-- For each miss: the cause, and how you know. The four common causes are:
     too few examples for a label, a boundary you applied inconsistently, a
     genuinely hard label pair, and a task the model can't reach from this
     much data.

     ⚠️ Use your agreement report as evidence. It is the only instrument you
     have that can tell a LABELLING problem from a MODEL problem, and this
     section is graded on whether you used it that way. -->



---

## Agreement Report

<!-- Your rate against the staff set, and every disagreement adjudicated.

     Remember you labelled these 30 under the STAFF taxonomy in
     data/staff_taxonomy.md, not your own — so every argument below is made
     from those definitions and those decision rules. -->

**Agreement rate:** ___ / 30 = ___%

<!-- Nobody grades this number. A 60% who argues every disagreement from the
     stated rules beats a 95% who wrote "staff was right" nine times. Several
     of the 30 were chosen because they're genuinely ambiguous — you should be
     winning some of these. -->

**Disagreements**

<!-- Three lines each: the post, both labels, and who you think is right and
     why — grounded in the staff definitions you were both applying.

     Then sort each into one of three piles:
       (a) the rule covered it and I applied it loosely → a consistency problem
       (b) the rule genuinely doesn't say               → a gap in the definitions
       (c) the rule is ambiguous here and my reading is defensible → argue it.
           This is a legitimate win.

     Pile (a) is the one that matters most for your diagnosis: if you applied a
     written rule two different ways on 30 posts, that is direct evidence about
     what you did across your own 200. -->

**1.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**2.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**What the pattern in my disagreements tells me:**



---

## The Improvement

**What I changed:**

**Which diagnosis pointed at it:**

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->



---

## What's Still Broken

<!-- For each criterion still missed: what you'd do, and why you stopped. -->



**The gap between what I meant my labels to capture and what the model
learned:**
<!-- Two sentences. Your confusion matrix is the evidence. -->



<!-- ═════════════════════════════════════════════════════════════════════

     SUBMISSION CHECKLIST — unit 5

       [ ] criteria.md has five numbered criteria, each naming a NUMBER
       [ ] Each has a reason underneath tied to your data or taxonomy
       [ ] labels.csv: at least 150 rows, text/label/note, ONE file not split
       [ ] No label above 70%
       [ ] All five unit 5 sections have real content
       [ ] Label Taxonomy includes the decision rule for your hardest boundary
       [ ] The Dataset includes three hard cases
       [ ] results.json and test_split.csv committed (the notebook does this)
       [ ] At least four new commits
       [ ] Repository URL submitted — WRITE IT DOWN

     SUBMISSION CHECKLIST — unit 6

       [ ] Baseline vs. Trained table, with your prediction written beforehand
       [ ] Run Log — Before, five criteria across three seeds
       [ ] Confusion matrix TYPED AS A MARKDOWN TABLE
       [ ] A verdict on every criterion
       [ ] A diagnosis for every miss, using the agreement report as evidence
       [ ] Agreement Report with every disagreement adjudicated
       [ ] One improvement, with Run Log — After
       [ ] What's Still Broken
       [ ] results_three_seeds_before.json, results_three_seeds_after.json,
           baseline_results.json and
           agreement_results.json committed
       [ ] At least four new commits
       [ ] The SAME repository URL as last unit

     Do not delete and recreate this repository.
     ═════════════════════════════════════════════════════════════════════ -->

---

📖 **How to run this project: [RUNNING.md](RUNNING.md)**
