# Project Wishbox (working title)

**Status:** Discovery / prototype  
**Audience:** Young adults, initially students, job seekers, and people early in their careers in China  
**Format for first test:** Mobile web prototype, Chinese-language experience  
**One-line idea:** Open a small surprise, leave a wish, and make a stranger's day a little warmer.

> This is a project hypothesis, not a claim that a product-market fit has been found. The first release exists to learn whether the unknown contents of another person's wish can create repeat use, alongside or beyond a personal reading.

## 1. Why this exists

People sometimes want a playful way to approach a real uncertainty: a presentation tomorrow, a job interview, a difficult conversation, a date. A lucky draw offers anticipation and a gentle prompt. Writing a wish turns vague anxiety into a concrete hope. Discovering another person's wish may create surprise, recognition, and a small opportunity to care.

The desired feeling is **fun first, human warmth after**. This is an entertainment and peer-support experience, not a prediction service, therapy, or a substitute for professional help.

## 2. Product thesis

**User job:** “When something is on my mind, give me a brief, enjoyable ritual that helps me express it, and occasionally reminds me that other real people are going through things too.”

**Core loop (candidate, to be tested):**

1. Choose a topic or write a short question.
2. Open a personal reading or a sealed stranger wish.
3. Optionally post a wish and/or send one thoughtful response.
4. Return when a wish receives a response, when someone updates their outcome, or when a new concern arises.

The first experiment deliberately offers the two reveal types as peers. It does **not** require a user to post a wish before reading someone else's, nor require a reply to unlock a reading. Forced reciprocity would make preference data hard to interpret.

### Positioning hypothesis

“A small mystery containing a real human moment.” The card or envelope is the ritual; a real person's wish is the potentially distinctive surprise. This is a hypothesis to validate, not a proven gap in existing products.

## 3. Competitive context

| Reference | Useful observation | Implication for this project |
| --- | --- | --- |
| [测测](https://www.cece.com/product/) | Personal questions, wisdom cards, AI interpretations, community, and emotional support already coexist. The screenshots reviewed show a three-card reading for a relationship question. | “Draw a card + meet strangers” is insufficient differentiation. Test the *main loop* and emotional outcome. |
| [Co–Star](https://www.costarastrology.com/) / [The Pattern](https://www.thepattern.com/app-features) | Personal interpretation and relationships make readings feel relevant. | A reading needs a clear connection to the user's own situation; avoid generic slogans. |
| [Kind Words](https://popcannibal.com/kindwords/) | Strangers anonymously request and send kind letters. | Thoughtful human responses can be the product, but supply and moderation are core operations. |
| [PostSecret](https://postsecret.com/) | A changing collection of real, anonymous disclosures creates curiosity without fortune telling. | Test whether another person's true story is itself a reason to open. |
| [Pokémon TCG Pocket](https://tcgpocket.pokemon.com/) / [Mark印](https://apps.apple.com/cn/app/id6495973653) | Physical-feeling reveal and a card that opens a larger story. | Borrow the anticipation and sense of discovery; do not assume an original mascot or live AI character is needed. |

These are design references, not evidence that this idea will retain users.

## 4. Who to start with

**Initial segment:** 18–26-year-old Chinese-speaking students, job seekers, and early-career workers who face small, near-term events they care about. Examples: an interview, presentation, exam, or awkward conversation.

**Reason for focus:** Their wishes can be specific and revisited within a week. “Gen Z” alone is too broad for a useful first test.

**Not the initial focus:** Users seeking definitive predictions, emergency mental-health support, dating or open-ended anonymous chat. Adults only for the first prototype; age-appropriate design for minors would require separate work.

## 5. MVP experience

### A. Entry

Prompt: **“今天你心里装着什么？”**  
Choices: **工作/学业 · 关系 · 自己 · 随便看看**. A short optional free-text field lets someone add context without asking for sensitive details.

Present two equally prominent, unopened options, with randomized left/right order:

- **给我的一张签** — a short, authored reading or reframing prompt relevant to the topic.
- **来自陌生人的一个愿望** — a real, reviewed, anonymous wish from a consenting participant.

Both remain accessible. The instrumented choice is **which one they open first**. On the first day, invite the person to try both so they know what each means.

### B. Personal reading

Use a small authored content bank, not a live model. A reading contains (1) a playful title, (2) one or two concise sentences, (3) a question that may lead to a wish. Avoid claims of certainty or invented predictions.

Example, for a presentation: **“开场顺利签：投影仪或许有自己的想法，但第一句话你可以先准备好。明天你最希望哪一刻顺利？”**

### C. Stranger wish

Reveal one short, moderated wish. Offer **skip**, **send a short reply**, **report**, and **hide this topic**. Responses should be free text with light prompts such as “我想对你说……”; canned emoji alone should not count as a meaningful reply. Do not expose profiles, location, or direct messaging in the test.

Example: **“希望明天第一次独立做汇报时，不要紧张到忘词。”**

### D. My wish and outcome

Writing a wish is optional. Before submission, show whether it is private or anonymously shared, and ask for explicit consent to share. Let the author delete it. A next-day prompt may ask **“后来怎么样了？”** with options **顺利了 / 还在继续 / 不太顺利 / 不想说** and an optional sentence. Never imply a positive outcome is required.

### Experience rules

- A visit should take 2–3 minutes; no infinite feed.
- The reading cannot promise an outcome; the stranger wish cannot promise a reply.
- Do not manufacture “real” wishes, replies, or outcomes using AI. Seed only with real submissions whose authors consented to this use.
- Show clear authorship: “预先撰写的签文” versus “一位真实用户匿名分享”.
- Offer a low-pressure exit after every reveal.

## 6. Seven-day validation study

### Main question

**After trying both, do people repeatedly choose to open a stranger's wish before another personal reading?**

The broader product question is whether that preference also creates thoughtful interaction and return behavior. A first click by itself does not establish retention.

### Study design

1. Recruit a directional sample of **30–50** people from the initial segment. Start with 20–30 to check the prototype and operations; expand if it works.
2. Day 1: give every participant one free opening of each type. Randomize which is shown first in the introduction.
3. Days 2–7: display both choices at the same time, with matched visual prominence and randomized position. Let them open either or both, or leave.
4. Do not change price, content length, notification frequency, or unlock rules between the two options. Use comparable care in writing and visual treatment.
5. Send at most the same neutral study reminder to everyone if reminders are needed; record reminded and unprompted visits separately.
6. At the end, ask: **“你打开时期待看到什么？”** and **“哪一次内容让你想回来？为什么？”** Do not ask only which concept they say they prefer.

### Events to record

`participant_id` (pseudonymous), `study_day`, `visit_source` (organic/reminder), `choice_position`, `first_open` (reading/wish/none), `second_open`, `topic`, `wish_posted`, `wish_reply_sent`, `wish_reply_received`, `outcome_updated`, `report`, `skip`, and timestamps. Keep free-text wishes and responses separate from analytics; minimize identifying information.

### Measures and interpretation

| Measure | Interpretation |
| --- | --- |
| First-open share on days 2–7, by person as well as by visit | Revealed preference after both options are familiar; compare later days to early days. |
| Organic return rate and days active | Whether the experience attracts return without a study reminder. |
| Wish-open → substantive reply rate | Whether curiosity becomes care rather than passive browsing. Review reply quality manually. |
| Posted wish → outcome check-in / reply revisit | Whether participants care about the continuing story. |
| Reports, skips, unanswered wishes, and feeling worse after use | Quality and safety guardrails; a high click rate cannot offset harm or disappointment. |

**Decision guidance, set before seeing results:**

- **Promising human-wish direction:** later-day first opens favor wishes, with repeat organic visits and a meaningful share of considerate replies or outcome revisits.
- **Reading as hook, wish as depth:** readings win first opens, while wishes drive more replies and return visits.
- **Rework:** wishes get day-one curiosity but little later-day choice or interaction.
- **Stop or redesign the exchange:** many wishes go unanswered or participants report feeling exposed, pressured, or worse.

There is no magic percentage for this small sample. Report counts and person-level patterns, not a false claim of statistical proof. A larger randomized test can follow if the signal is strong. Consider novelty: a lift concentrated only in the first days is not a durable loop.

## 7. Recruitment and incentives

Recruit where the initial segment already gathers: university communities, career groups, relevant social posts, and second-degree referrals. Friends may distribute the invitation but should not dominate the sample. Screen for age (18+), current stage, and a near-term event or concern. Avoid revealing the exact comparison in the screener.

**Sample invitation:**

> 招募一项 7 天的手机产品体验测试：每天约 2–3 分钟，主题是生活中的小期待与惊喜。适合正在上学、求职或初入职场的朋友。完成体验有感谢费。感兴趣请填写 1 分钟问卷：[链接]

Pay fairly for time spent, including partial participation; an additional amount may cover the final interview. Do not pay per wish or reply. Recruit a few reserves for attrition. Tell people in plain language what is collected, who can see submitted text, and how to withdraw.

## 8. Trust, moderation, and boundaries

The main operational risk is a vulnerable wish receiving no response or an unkind response. For the study:

- Review wishes and replies before they are delivered; remove names, employers, contact details, and location clues. Obtain consent before editing a user's words or ask them to revise.
- Provide reporting, deletion, blocking of content themes, and a way to leave without posting.
- Do not rank people by vulnerability or reward dramatic disclosures.
- Limit exposure per wish so a small number of posts does not absorb all replies. Track unanswered wishes; a researcher may check in, clearly as a researcher, without pretending to be a stranger.
- Keep an escalation protocol for self-harm, threats, or acute distress: pause publication, show local support resources appropriate to the participant's location, and follow a documented human review procedure. Do not position the app as a crisis service.
- State the retention and deletion schedule before recruiting; delete raw study data after the agreed period.

If these operations cannot be staffed, test only the reading and *read-only* wish reveal until they can.

## 9. Scope and implementation

**Visual interaction prototype:** [Open the static mobile prototype](prototype/index.html). Its [design notes](prototype/README.md) capture the pale forest and water palette, slowly appearing water fortune, and a wish slip posted to a mailbox. This is a demonstration with authored sample content, not a live study or real stranger submissions.

**Build now:** mobile-first web page; two equal reveal choices; content bank; reviewed real-wish pool; optional wish submission and short reply; lightweight admin review; pseudonymous event log; consent and deletion controls; outcome check-in; simple export for analysis.

**Defer:** live AI character, AI-generated fortune, complex tarot rules, original character IP, physical cards, open-ended DM, social graph, paid readings, streaks, endless feed, recommendation algorithm, native app.

**Low-tech implementation:** a static mobile page plus a small database and password-protected review screen is enough. The first pilot can even use a form and manual matching if the user-facing choice and event logging remain consistent. Select the stack based on the builder's existing skills; do not let infrastructure become the first experiment.

### Minimal data entities

`Participant` (pseudonymous ID, consent, eligibility), `Reading` (topic, text, version), `Wish` (author ID, text, visibility, moderation state, expiry), `Reply` (wish ID, responder ID, text, moderation state), `Outcome` (wish ID, status, optional text), `Event` (participant ID, action, timestamp, study day, experiment position). Restrict researcher access and avoid storing real names with wish text.

## 10. Build and research checklist

- [ ] Write a one-page consent notice, content rules, privacy/deletion policy, and escalation procedure.
- [ ] Draft and quality-review 20–30 short readings across the starting topics.
- [ ] Collect a small, consenting pool of real wishes before launch; check coverage by topic and recency.
- [ ] Design two equally attractive reveal tiles and verify position randomization.
- [ ] Implement first-open logging, organic versus reminded visits, and moderation queue.
- [ ] Test submission, skip, report, deletion, and the no-reply state with a few pilot users.
- [ ] Recruit, screen, and onboard an initial 20–30 participants; set the seven-day dates.
- [ ] Run daily moderation and supply checks without changing the study rules midstream.
- [ ] Review participant-level behavior and conduct short follow-up interviews.
- [ ] Publish a concise decision memo: evidence, counterevidence, limitations, and next experiment.

## 11. Open questions

1. Does a wish need to be matched by situation, mood, or pure randomness to feel surprising *and* relevant?
2. Is the stronger hook a daily ritual or an event-driven visit before something important?
3. Does offering three wishes improve agency, or dilute the emotional weight of one reveal?
4. Do people want a one-time reply, an outcome update, or an ongoing relationship? Start with the smallest safe option.
5. What proportion of wishes can receive a timely, thoughtful response at the expected community size?

## 12. Working principle

**Make the reveal delightful, make the people real, and let behavior decide which part deserves to become the product.**
