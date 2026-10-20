# ilyahov-info-style

A Claude skill that edits text by Maxim Ilyahov's info-style method. It cuts words that carry no information, replaces adjectives with facts, and keeps your voice.

I built it for weekly updates to leadership. It works on any text a reader didn't ask for: posts, emails, CVs, product copy. Russian and English.

## Before and after

Before:
> This month the team made significant progress across key initiatives. We continued to drive alignment with stakeholders and leveraged AI to streamline workflows.

Congratulations to the team, I guess. What exactly did they make progress on?

After:
> Payroll Onboarding: new customers now reach their first payroll in 6 days, down from 9. We removed the manual bank-detail check, which caused 40% of the delays.

## How it works

The test for every word: can the reader check it, picture it, or act on it? If not, it goes.

1. Asks for 2–3 of your recent texts to learn your voice.
2. Cuts filler without rewriting.
3. Replaces abstractions with numbers, names and dates. Where a fact is missing, it writes [needs a fact] instead of inventing one.
4. Rebuilds sentences in subject, verb, object order and active voice, and breaks up runs of short, same-length sentences.
5. Checks the result against your samples and puts back what made it yours.

## What you get

- The edited text
- What was cut, by category
- What was kept for your voice, and why
- Word count before and after

If the text is already tight, it says so and stops.

## Install

**Claude.ai:** download this repo (Code → Download ZIP), zip the `ilyahov-info-style` folder on its own, and upload it under Skills in Claude's settings.

**Claude Code:** copy the `ilyahov-info-style` folder to `~/.claude/skills/`.

Then say "Ilyahov" or "strip the filler" and paste your text.

## Credit

Method from "Write, Shorten" ("Пиши, сокращай") by Maxim Ilyahov and Lyudmila Sarycheva.

## License

MIT
