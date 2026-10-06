# Hi, I'm Ali

I live in Hamburg and work in operations. I build small, real workflows with **n8n**, with **AI as my co-pilot**: reminders, follow-ups, CRM clean-up and the copy-paste jobs that quietly eat an afternoon. Each one comes with a short build story: the chore, what I built, what broke, and how I fixed it.

I trained as a biomedical engineer, and my background is health technology and operations. That's where the habit comes from: when a process keeps wasting someone's time, I want to build the fix.

Everything here is a personal learning project. The demos run on made-up data and send nothing.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ali%20Khosravi-0A66C2)](https://www.linkedin.com/in/ali-khosravi-5439a7116)
[![Email](https://img.shields.io/badge/Email-alikhosrawi%40gmail.com-555555)](mailto:alikhosrawi@gmail.com)

## Featured builds

**[Pipeline hygiene check](https://github.com/Alikhosrawi/ai-automation-portfolio/tree/main/crm-pipeline-hygiene)**: the Monday clean-up of a HubSpot export before the forecast call.

- Finds duplicate deals (exact copies by rule; messy ones like "Sandtor Spediiton GmbH" judged by AI), deals with no activity for 60+ days, and deals with no amount, close date or owner
- Shows the Q4 forecast before and after cleaning (€2.13M → €1.78M on the demo data), and writes one to-do message per rep
- AI writes the Monday note, and every number in it is checked against the computed facts before it's used
- Tested honestly: problems planted on purpose, rules written down before the test ran. In the main run it caught all 18 duplicates (the 10 messy ones judged by AI) and fell for none of the 6 look-alike traps; a rules-only version flagged 13 wrong pairs. The limits are in the [README](https://github.com/Alikhosrawi/ai-automation-portfolio/tree/main/crm-pipeline-hygiene): the cleaned forecast still came out 7 % low, and on 20 other test sets 17 of 200 messy duplicates never reached the AI.

**[Physio appointment reminders](https://github.com/Alikhosrawi/ai-automation-portfolio/tree/main/physio-appointment-reminders)**: reminders, replies and no-show follow-ups for a small physio practice.

- 15:00: a reminder to everyone booked for tomorrow ("Reply 1 = See you tomorrow, 2 = I need to move it")
- Every 15 minutes: "1" gets a thank-you, "2" gets three open slots, anything else is flagged for a person
- 18:30: a kind rebook note to anyone who missed today's appointment
- Built in n8n. Fake data. Nothing is sent: every message goes to a "would send" log.
- Includes the [build story](https://github.com/Alikhosrawi/ai-automation-portfolio/blob/main/physio-appointment-reminders/build-story.md) with the real bug: replies were answered again on every check.

**[Expat onboarding autopilot](https://github.com/Alikhosrawi/ai-automation-portfolio/tree/main/expat-onboarding-autopilot)**: document checklists, gentle chasing and weekly updates for a relocation agency's new clients.

- Builds each client's document checklist from their permit type and nationality
- Chases missing documents at most once every 7 days, so nobody gets nagged
- Sends a weekly update to the client and a progress-only one to their HR contact

**[Physio supplies reorder agent](https://github.com/Alikhosrawi/ai-automation-portfolio/tree/main/physio-supplies-reorder)**: the Friday supply order, prepared for the practice manager to approve.

- Forecasts next week's usage from the bookings, prefills each supplier's cart and explains every change ("2 boxes instead of 1, because taping sessions doubled")
- The manager approves, edits or removes each line before anything is final
- Tested honestly: a pre-registered backtest on 50 weeks of synthetic history (41 scored), with the losses reported next to the wins

More demos will go into the [portfolio repo](https://github.com/Alikhosrawi/ai-automation-portfolio).

## One chore, gone

That's the name of the series: pick one repetitive admin chore, build the smallest workflow that removes it, and write up what broke along the way. No big platform, just one fix for one job, explained step by step.

## Tools I use

- **n8n**: workflows you can see as a picture on a canvas
- **AI**: prompts and agent logic for AI-powered steps
- **Python**: small helper scripts
- **Spreadsheets and CSV files**: where most small-business data actually lives
- **Salesforce**: reports, dashboards, flows and data cleanup
- **HubSpot**: CRM

## Writing

I post the build stories on [LinkedIn](https://www.linkedin.com/in/ali-khosravi-5439a7116), one chore at a time.

## Background

- **Biomedical engineering** (MSc): health technology, data and how systems behave in real life
- **Operations** at a multi-site food company in Hamburg: processes, reporting, customer accounts and the tools that hold them together
- **What I bring to a build:** I start from the boring chore people actually do, keep the fix small, and test it on fake data before it touches anything real

## Contact

- LinkedIn: [linkedin.com/in/ali-khosravi-5439a7116](https://www.linkedin.com/in/ali-khosravi-5439a7116)
- Email: [alikhosrawi@gmail.com](mailto:alikhosrawi@gmail.com)
