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

**Where the posts came from:** These posts came from Reddit's r/stocks subreddit. The posts are all the original thread-starters and none are replies.

**How I labelled them:** All of the posts were labeled cold, manually categorized at the time of copying them into the csv.

**Counts per label:**

| Label     | Count |  Share |
|-----------|-------|--------|
| advice    |   51  |  25.5% |
| analysis  |   82  |  41.0% |
| news      |   67  |  33.5% |
| **Total** |  200  | 100.0% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:* Xiaomi shipped 30.7 million smartphones in the third quarter, down 29.2% from a year earlier, according to IDC's preliminary vendor table. Samsung and Apple between them held 45.0% of the quarter's shipments, up from 36.9% a year earlier. Both OPPO and vivo fell by larger percentages than Xiaomi. The full market came in at 255.3 million units, and IDC put the year-over-year decline at 22.0%, calling it the largest of any quarter in its tracking. IDC expects overall smartphone growth to be constrained through 2027, with any recovery pushed to 2028 at the earliest. Memory costs are still climbing, though the quarter-over-quarter increase slowed to low double digits in the third quarter. With component costs still climbing, have you or the people around you started waiting longer between phone upgrades?
>
> *Could have been:* news or advice
>
> *I chose, because:* news: The majority of the post is verbatim news, and only at the very end does a question arise with tertiary relevancy.

**2.**
> *The post:* Fed pausing today, with eyes on December. What are you trading? Ahead of today's FOMC decision, consensus points to a temporary interest rate pause, holding the benchmark steady at 3.75%–4.00% to let the market fully absorb previous tightening actions. However, with September's inflation metrics showing persistent heat, the primary focus is entirely shifted to the 2:30 PM ET press conference, where Chairman Kevin Warsh is widely expected to signal a 25bps rate hike for the December meeting.Given that a hawkish pause is effectively priced into equities, the market’s reaction will depend heavily on the tone surrounding future macro policy projections and the terminal rate outlook. Are you defensively positioning your portfolio into mega-cap tech and cash-heavy alternatives ahead of the afternoon volatility, or are you utilizing options vectors to hedge against a potentially hawkish surprise from the Fed?
>
> *Could have been:* news or advice
>
> *I chose, because:* advice: Although the post contains a good amount of news, the post is framed as a question seeking advice from the community regarding their trading strategies for the day.

**3.**
> *The post:*"Anthropic's valuation chatter just shifted. What are you watching? Anthropic IPO chatter picked up again after last week's investor day talk. Some investors are now floating something closer to 1.5 trillion, down from the earlier 2 trillion chatter. The company has only said it filed a confidential draft S 1. I still haven't seen a public prospectus on EDGAR, so I'm not trading rumor windows or valuation guesses. Before there's anything to buy, I'm watching the public names first. AMZN and GOOGL sit on both sides of this: a stake that can get marked up when private AI rounds reprice, and Anthropic cloud spend that lands on AWS / Google Cloud. That's why the IPO headline keeps pulling people into those tickers. Fair enough. But if the real thesis is cloud demand, I'd rather see the cloud segment itself keep growing with decent margins. AWS last printed about 37% growth with operating margins near 39%, which is the part I care about more than another Anthropic rumor. I've been lining that segment up against older quarters on moomoo so I'm not just reacting to the headline. Are you waiting for a public S 1, or watching AMZN / GOOGL first? If you're watching, which numbers matter most?"
>
> *Could have been:* advice or analysis
>
> *I chose, because:* analysis: The majority of the post is the user's orignal thought, and it is clear they are confident in their statements. The question at the end is not the core purpose of the post and is intended to seed a discussion rather than gain advice. 

---

## The Training Run

<!-- Your starting model, your settings, and anything you changed and why. -->

**Base model:** `distilbert-base-uncased`

**Settings:** 3 epochs, learning rate 2e-5, batch size 16, max length 128 tokens, seed 42. Trained on CPU.

**Anything I changed from the defaults, and why:**
Nothing. I kept every default so this first run is a clean starting point to compare against. One thing to note: many r/stocks posts are longer than 128 tokens, so the model only reads the first ~100 words of a long post. For `advice` posts, the question that defines the label often comes at the end.

**Split sizes:** train 139 · val 31 · test 30 (stratified 70/15/15)

| Label    | Train | Val | Test |
|----------|-------|-----|------|
| advice   |  35   | 8   |  8   |
| analysis |  57   | 13  |  12  |
| news     |  47   | 10  |  10  |

`advice` is my smallest label and has exactly 8 posts in test, right at the line where F1 starts to swing between seeds. Each `advice` post in test is worth 12.5 points of recall.

Validation loss went down each epoch (1.043 → 0.997 → 0.973), but it was still falling at epoch 3. Training stopped before the model converged.


---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:* I asked Claude to stress-test my label definitions and decision rule against 8 made-up r/stocks posts, several of them built to sit on a boundary between labels.
- *What came back:* Several posts didn't get exactly one label. Examples: an article followed by "should I sell my shares?" (news or advice?), an article with heavy commentary (news or analysis?), a bare gain post and a one-line opinion that fit no label. It also pointed out that my `advice` definition covered general questions while my decision rule didn't.
- *What I changed:* I added "majority of the post" wording to all three definitions. I gave `analysis` a minimum bar of "at least one supporting argument or fact". I changed `advice` to cover questions "on the market", and widened `news` to include "a summary of an announcement". I rejected the gain-post and one-liner cases, because r/stocks moderation removes low-effort posts and they wouldn't appear in my data, so I didn't add a label for them.

**Moment 2**

- *What I asked for:* I asked for help writing five acceptance criteria, then had Claude review my drafts.
- *What came back:* Five draft criteria (accuracy, per-label F1, balance, staff agreement, confidence) plus an alternative criterion on the analysis/advice boundary. On review, it pointed out that my consistency criterion ("if someone else labeled this dataset") couldn't be measured, and that my balance reason blamed lopsided labels for the F1 swings that small labels actually cause.
- *What I changed:* I raised the balance cap from 45% to 50%. I dropped the confidence criterion and used the analysis/advice boundary criterion instead, since that's my hardest boundary. I rewrote #4 against the 30 staff posts so it can be measured, and rewrote my reasons to refer to my own test split size and labels.

**Pre-labelling disclosure:**
None. I labelled all 200 posts myself by hand as I collected them, with no AI pre-labelling. AI was used only to review my taxonomy and criteria, as described above. I did not pre-label any of the posts. All 200 were manually labeled.

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

| Measure          | Baseline | Trained | Difference |
|------------------|----------|---------|------------|
| Overall accuracy | 0.600    | 0.567   | -0.033     |
| Macro F1         | 0.556    | 0.425   | -0.131     |
| F1 — `advice`    | 0.667    | 0.000   | -0.667     |
| F1 — `analysis`  | 0.667    | 0.686   | +0.019     |
| F1 — `news`      | 0.333    | 0.588   | +0.255     |

**What I predicted before I looked:**
I predict my trained model will beat baseline on news and analysis.

**What the gap actually means:**
News and Analysis were more accurate with the trained model, but advice came out worse bringing down the overall accuracy to below the baseline. The advice definition or manual labeling were not explicit enough, or sample size was too small.



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1. Overall accuracy | ≥ 0.80 | 0.567 | 0.400 | 0.633 | MISSED |
| 2. Per-label F1 (news / analysis / advice) | news ≥ 0.85; analysis, advice ≥ 0.70 | 0.588 / 0.686 / 0.000 | 0.000 / 0.571 / 0.000 | 0.842 / 0.667 / 0.000 | MISSED |
| 3. Label balance in labels.csv | No label > 50%, none < 50 posts | Max 41% (analysis), min 51 (advice) | Same (dataset, not seed-dependent) | Same | MET |
| 4. Agreement with staff labels | ≥ 21/30 (70%) | 29/30 (97%) | Same (not seed-dependent) | Same | MET |
| 5. Analysis↔advice cross-errors | ≤ 20% of true analysis + advice | 6/20 (30%) | 8/20 (40%) | 8/20 (40%) | MISSED |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

| true \ predicted | advice | analysis | news |
|------------------|--------|----------|------|
| **advice**       | 0      | 6        |    2 |
| **analysis**     | 0      | 12       |    0 |
| **news**         | 0      | 5        |    5 |

**My biggest off-diagonal number, and what it means:** 6 advice posts were labeled as analysis while 0 analysis posts were labeled as advice. This lopsided result may be because the posts were truncated due to token limitation and the distinguishing advice portion of the post typically comes at the end. 

---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 | Overall accuracy | ≥ 0.80 on all three seeds | MISSED | Best seed was 0.633 (2024), worst 0.400 (7). No seed came within 0.15 of the target. |
| 2 | Per-label F1 | news ≥ 0.85; analysis, advice ≥ 0.70, every seed | MISSED | Advice F1 was 0.000 on all three seeds. News peaked at 0.842 (2024) and was 0.000 on seed 7. Analysis never reached 0.70 (best 0.686). |
| 3 | Label balance | No label > 50%, none < 50 posts | MET | Counted labels.csv: analysis 82 (41%), news 67 (33.5%), advice 51 (25.5%). This is a property of the dataset, so it holds on every seed. |
| 4 | Staff agreement | ≥ 21/30 | MET | agreement_results.json: 29/30 agreed (97%). Not seed-dependent. |
| 5 | Analysis↔advice cross-errors | ≤ 20% of true analysis + advice, every seed | MISSED | From each seed's confusion matrix, (advice→analysis + analysis→advice) / 20: 6/20, 8/20, 8/20. All 22 errors went advice→analysis; none went the other way. |

**Diagnoses**

**The agreement report rules out labelling as the main cause.** I agreed with staff on 29 of 30 posts (97%), and the one disagreement was a single pile (a) slip about what counts as a verifiable fact. I apply written rules consistently, so if my labels were inconsistent I'd expect errors in both directions across the analysis/advice boundary. Instead, every error goes one way and the model never predicts advice. That points to a model/data problem, not a labelling problem. One caveat: the staff set tests the staff taxonomy, not my own advice/analysis rule, so it's strong but indirect evidence.

**#1 Overall accuracy: missed because the model is undertrained and collapses toward `analysis`.** On seed 7 it predicted `analysis` for all 30 test posts (accuracy 0.400 = 12/30, the analysis share). Mean confidence was about 0.42 whether the model was right or wrong, barely above the 0.33 of a three-way coin flip, so it hasn't separated the classes. Validation loss was still falling at epoch 3 (1.043 → 0.997 → 0.973). Cause: **a task the model can't reach from this much data/training**: 139 training posts and 3 epochs isn't enough for it to move off the majority label.

**#2 Per-label F1: missed mainly because advice gets zero predictions.** Advice F1 is 0.000 on every seed because the model never predicts advice even once. Two causes stack:
- **Too few examples:** advice is my smallest label, with only 35 training posts.
- **Truncation:** 75% of advice posts in labels.csv are longer than the 128-token limit (median 154 tokens). The question that makes a post advice usually comes at the end, so the model is cut off before it sees it.

The zero-shot baseline reached 0.667 F1 on advice, which shows the advice signal is in the text. News swings from 0.000 to 0.842 across seeds, the same instability as #1: when training happens to separate news, it does well.

**#5 Analysis↔advice boundary: missed for the same reason as advice in #2.** All 22 boundary errors across the three seeds are advice→analysis, with 0 analysis→advice. If I'd drawn the boundary inconsistently, the errors would go both ways. A one-way pile-up means the model can't see what makes a post advice: the truncated opening of an advice post (context, a position, some numbers) looks like analysis. Cause: **a genuinely hard label pair made harder by truncation and too few advice examples**, not inconsistent labelling.

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

**Agreement rate:** 29 / 30 = 97%

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
> *The post:* "Three of us ran the same session on the same day, different shoes, within 10 seconds of each other over 5 miles. I'm not saying shoes do nothing, but whatever they do was smaller than the noise between three people."
      "staff": "analysis",
      "mine": "hot_take"
>
> *Staff said / I said:* analysis, hot_take
>
> *My call, and why:* I did not think the statement about the 3 people running on the same day within 10 seconds of each other was a verifiable fact, and therfore labeled this as hot_take instead of analysis. 
>
> *Which pile:* a


**What the pattern in my disagreements tells me:** My labeling method is applied more loosely than the staff labeling methodology.

---

## The Improvement

**What I changed:** I raised `MAX_LENGTH` from 128 to 256 tokens in the notebook's settings cell. Nothing else changed: same 200 labels, same seeds (42, 7, 2024), same 3 epochs, learning rate 2e-5, batch size 16. Changing only this one setting means any difference in the after run comes from the model reading more of each post.

**Which diagnosis pointed at it:** The diagnoses for #2 and #5. Advice had F1 0.000 on all three seeds, and all 22 analysis/advice boundary errors went advice→analysis. The agreement report (29/30) suggested my labelling wasn't the cause. Checking labels.csv showed that 75% of advice posts are longer than 128 tokens (median 154), and the part that makes a post advice (the question asking the community what to do) usually comes at the end. At 128 tokens the model mostly saw the opening context, which looks like analysis. At 256 tokens it covers the median advice post. The zero-shot baseline, which reads the whole post, got 0.667 F1 on advice, so the signal is in the text when the model can see it.

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1. Overall accuracy | ≥ 0.80 | 0.633 | 0.500 | 0.533 | MISSED |
| 2. Per-label F1 (news / analysis / advice) | news ≥ 0.85; analysis, advice ≥ 0.70 | 0.737 / 0.727 / 0.000 | 0.462 / 0.615 / 0.000 | 0.571 / 0.632 / 0.000 | MISSED |
| 3. Label balance in labels.csv | No label > 50%, none < 50 posts | Max 41% (analysis), min 51 (advice) | Same (dataset unchanged) | Same | MET |
| 4. Agreement with staff labels | ≥ 21/30 (70%) | 29/30 (97%) | Same (labels unchanged) | Same | MET |
| 5. Analysis↔advice cross-errors | ≤ 20% of true analysis + advice | 6/20 (30%) | 8/20 (40%) | 8/20 (40%) | MISSED |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->

No. It didn't fix the problem it was aimed at. Advice F1 is still 0.000 on all three seeds, the model still never predicts advice, and the analysis/advice cross-errors are exactly the same as before (6/20, 8/20, 8/20, all advice→analysis). If truncation were the cause, letting the model read the median advice post in full should have produced at least a few correct advice predictions. It produced none, so truncation wasn't the bottleneck.

Overall accuracy moved (0.567 / 0.400 / 0.633 → 0.633 / 0.500 / 0.533), but the mean only went from 0.533 to 0.556, and seed 2024 got worse. That's within the seed-to-seed spread, so I can't call it a real improvement. The one consistent change is that the model now predicts news more often on seed 7 (0 → 3 correct). That's still news being separated sometimes, not advice being learned.

Ruling out truncation leaves the other two causes from my diagnosis. Advice has only 35 training posts, and the model is undertrained: validation loss was still falling at epoch 3, and mean confidence is still about 0.43 whether the model is right or wrong, barely above the 0.33 of a random three-way guess. The model hasn't learned enough to move off the majority label, and showing it more of each post doesn't change that.


---

## What's Still Broken

<!-- For each criterion still missed: what you'd do, and why you stopped. -->

**#2 Per-label F1 and #5 Analysis↔advice boundary (same root cause).** Advice is still never predicted, so both stay missed. Next I'd train longer, raising `EPOCHS` from 3 to around 8–10, because validation loss was still falling at epoch 3 (1.043 → 0.997 → 0.973). If advice still didn't appear, I'd label more advice posts to bring it from 35 training examples up to roughly the size of analysis (57). Training longer is the cheaper test, and it tells me whether the issue is training time or data. I stopped because this unit allows one improvement. Changing epochs at the same time as `MAX_LENGTH` would have made it impossible to tell which change did what.

**#1 Overall accuracy.** This should rise once advice is fixed: advice is 8 of the 30 test posts, and the model gets every one wrong. Even a perfect advice fix wouldn't guarantee 0.80, though. News still swings between seeds (0.462–0.737 F1 after), which is the same undertraining problem. I'd expect longer training to help both, and I'd re-run all three seeds to check the result isn't a lucky split.

**The gap between what I meant my labels to capture and what the model
learned:**
<!-- Two sentences. Your confusion matrix is the evidence. -->

I meant advice to mean "a post whose main purpose is asking the community what to do," but the model learned nothing about advice. All 8 advice test posts went to analysis or news on every seed, before and after the fix. What it actually learned is closer to "default to analysis unless the post clearly reads like a news article," which is why the advice row of the confusion matrix is empty and almost everything piles into the analysis column.


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
