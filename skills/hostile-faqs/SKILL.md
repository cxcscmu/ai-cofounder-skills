---
name: hostile-faqs
description: Generates a 10-question hostile FAQ battlecard for live sales, investor, and buyer Q&A — with question type taxonomy, recommended response techniques, short and expanded answers, risk analysis, and coaching notes.
disable-model-invocation: true
---

Use the company information below and generate a hostile FAQ battlecard for live sales, investor, and buyer Q&A.

## INPUTS

Fill these in first. Do not skip them.

Company name / description: [INSERT COMPANY NAME AND 1 TO 3 SENTENCE DESCRIPTION]

ICP: [INSERT THE TITLE, FUNCTION, SENIORITY, INDUSTRY, AND BUYER MOTIVES OF THE IDEAL CUSTOMER PROFILE]

## YOUR JOB

Generate exactly 10 of the most hostile questions a real buyer from this ICP is most likely to ask.

Do not generate soft objections. Generate sharp, skeptical, high-stakes questions that could stall or kill momentum.

## IMPORTANT FRAMING

- Assume the buyer may sound polite while still testing for weakness.
- Prioritize questions that expose risk, lack of proof, weak differentiation, timing concerns, ROI skepticism, adoption issues, integration fears, pricing resistance, security/compliance concerns, and strategic doubt.
- Make the questions sound like something a smart operator, executive, or cross-functional buyer would actually say in a meeting.

## QUESTION TYPE TAXONOMY

Use these hostile FAQ types and assign one primary type to each question:

1. Closed / Yes-No
2. Open-Ended
3. Leading
4. Clarifying
5. Probing
6. Hypothetical

## APPROVED RESPONSE TECHNIQUES BY TYPE

- **Closed / Yes-No:** Expand, Redirect, Reframe, Partial Agreement, Follow Up
- **Open-Ended:** Focus, Highlight, Reflect
- **Leading:** Acknowledge, Redirect, Expand, Convert
- **Clarifying:** Appreciate, Be Direct, Add Context, Reinforce, Confirm
- **Probing:** Recognize Importance, Respond with Intention, Share Evidence, Invite Follow On
- **Hypothetical:** Stroke Ego, Ground, Clarify

## PERSONA GUIDANCE

When choosing the hostile questions and answers, assume the buyer may resemble one of these patterns:

- Big-picture executive who is superficially positive but tests for strategic weakness
- New business unit leader who digs into the value model and wants to feel like one team
- Recently hired executive who tests speed, rigor, technical differentiation, and your depth

Write for the ICP first, but use these patterns when relevant.

## OUTPUT REQUIREMENTS

Return the result as a markdown table with exactly these columns and in exactly this order:

| Rank | Hostile FAQ Type | Hostile Question | Why This Buyer Would Ask It | Recommended Technique | Why This Technique Fits This ICP | Answer Short | Answer Expanded | Risk If Answered Poorly | Priority (1-5) | Frequency (1-5) | Likelihood (1-5) |

### Instructions for filling the table

- Rank from 1 to 10, with 1 being the most dangerous question.
- Hostile FAQ Type must be one of the six allowed types.
- Recommended Technique must be one of the approved techniques for that type.
- Why This Buyer Would Ask It must explain the buyer psychology, political context, or decision risk behind the question.
- Why This Technique Fits This ICP must explain why that tactic is the most effective answer style for this specific buyer.
- Answer Short must be a crisp spoken response of 1 to 3 sentences.
- Answer Expanded must be a stronger version of the same answer for a longer live discussion.
- Risk If Answered Poorly must state what bad outcome the seller risks causing.
- Priority, Frequency, and Likelihood must each be integers from 1 to 5.
- Make the answers credible, specific, and commercially intelligent. Do not use generic fluff.
- Do not invent fake customer names, fake metrics, or fake certifications unless they were provided in the company description.
- If evidence is missing, answer honestly and strategically without sounding weak.
- Use plain English. No emojis. No hype.

## QUALITY BAR

- The questions should feel uncomfortable but realistic.
- The answers should protect credibility, preserve momentum, and move the conversation back toward business value.
- Choose the technique that best fits the question and the ICP. Do not rotate techniques mechanically.
- Vary the question types. Do not put all 10 in one type.
- Prefer answers that keep control without sounding defensive.
- If the ICP is executive, bias toward strategic and financial objections.
- If the ICP is technical, bias toward architecture, integration, data, security, and proof.
- If the ICP is operational, bias toward adoption, workflow disruption, implementation risk, and measurable ROI.

## TOP COACHING NOTES

After the table, add a short section titled **Top coaching notes**.

In that section, provide:

- 3 recurring patterns across the hostile questions
- 3 mistakes to avoid in live Q&A with this ICP
- 3 coaching reminders on tone, pacing, and control
