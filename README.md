# Second Sales Brain

A way for a BDR or account executive to keep what they learn from outreach, research and calls in one place, and to use it with AI when they write the next email or prep the next call.

Most reps send hundreds of emails a month and keep almost nothing from them. The good ones sit in a sent folder. Research on an account gets done once and is lost. Second Sales Brain is a simple system for saving that work, tagging what worked and why, and drawing on it every time you write or prep.

It is a method, not an app. It runs on tools most sales teams already have: Google Workspace with Gemini, Microsoft 365, ChatGPT, or Claude with Notion.

---

## What changes when you use it

| Without it | With it |
|---|---|
| Message 500 is written like message 1 | Message 500 draws on the 499 before it |
| "What worked last quarter?" is a guess | You can search for the answer |
| Your best emails sit in the sent folder | They are saved, tagged and scored |
| Research on an account is done once | It carries over to the next account in that industry |
| Call prep starts from nothing | Call prep pulls from your past outreach and research |
| AI drafts sound generic | AI drafts start from emails that worked for you |

---

## The four parts

### 1. Outreach library
Every email, LinkedIn message or video script worth learning from goes into one searchable place.
- AI tags and scores each message, with what worked, what didn't, and why.
- Before you write something new, you pull up your best past messages for the same kind of buyer.
- Once a week, a 15-minute review looks for patterns and adds what you learned to your own playbook.

### 2. Account and industry research
Each account you research makes the next one in that industry faster.
- Research on a target account covers funding, leadership changes, competitors and regulation.
- You keep notes on which pain points, wording and timing work in each industry.
- Before an email or a call, you get a short brief built from your CRM history and new web research.
- What you find goes back into your outreach and call prep, instead of a folder nobody opens.

### 3. Automation
The jobs that don't need judgment run on their own.
- Prospect lists built from your ideal customer profile.
- Clean import files that are ready for your CRM.
- Outreach saved to the library with as little typing as possible.
- Scheduled summaries and follow-up reminders.

### 4. Cold calling
Your research and past outreach are in front of you before and during a call.
- Call lists with talking points from your research, instead of a generic script.
- Objection prep for each type of buyer, based on what has worked for you.
- After the call, you log the outcome and what you learned, so the next call starts further ahead.

---

## Pick your setup

The method is the same in each one. Pick the setup that fits the tools your company allows.

- **[Google Workspace with Gemini](implementations/gemini-enterprise.md)**, my recommendation for most teams. It uses the Gmail side panel, NotebookLM as the knowledge base and Workspace Studio for automation, at no extra cost when Gemini is already part of your company's plan.
- **[Microsoft, or a company with strict IT rules](implementations/constrained-enterprise.md)**, for teams with no paid AI seats. It uses SharePoint or OneNote for storage, the free Copilot for low-risk tasks, and a local AI model for reading emails.
- **[ChatGPT Team or Enterprise](implementations/openai-enterprise.md)**. Custom GPTs are the front end, uploaded files are the knowledge base, and the API handles automation.
- **[Claude with Notion](implementations/high-autonomy.md)**, for freelancers, consultants and startups without IT limits. Claude reads and writes to your Notion directly, so the most work can be automated.

### Side by side (my estimates)

| | Gemini | Strict IT | ChatGPT | Claude with Notion |
|---|---|---|---|---|
| **Extra cost** | $0 (included) | $0 | $20-60 a month | $20-50 a month |
| **Setup time** | 1-2 hours | 1 hour | 2 hours | 3-4 hours |
| **Effort to save a message** | Lowest (automatic) | High (manual) | Medium | Low |
| **AI quality** | Strong | Basic | Strong | Strongest |
| **Data security** | Company-grade | Highest (stays local) | High | Medium |
| **Automation** | Full | None | Some | Full |
| **Answers grounded in your files** | NotebookLM | No | Partly | Claude Projects |
| **Audio and video summaries** | Yes | No | No | No |
| **Switching between apps** | None (side panel) | A lot | Some | A little |

---

## Start in 30 minutes

You don't need any of the setups to start.

1. Make a spreadsheet with these columns: Subject line, Score, Outcome, Tags, Persona, Industry, Channel, Sequence, Notes. (10 minutes)
2. Add the tags. Success tags are Sharp personalization, Pain point hit, Social proof, Pattern interrupt, Clear call to action, Good timing, Brevity and Value first. Failure tags are Generic, Too long, Wrong persona, No clear call to action, Feature dump and Weak subject line. (5 minutes)
3. Add your 3 best and 2 worst recent messages. (10 minutes)
4. Tag all five. (5 minutes)

Use it for a week before you add anything else.

---

## Rules that work in any setup

1. Saving a message has to take less than a minute, or you'll stop doing it.
2. Tag why it worked, not what it was. "Good email" can't be searched. "Sharp personalization, clear call to action" can.
3. Score honestly. If every message is your best, the scores stop meaning anything.
4. Review once a week. Daily is too often to see a pattern.
5. Use three tags at most on a message, so you have to name what mattered most.
6. Search the library before you write. That's where each email gets better than the last.
7. Keep your data separate from the AI tool, so you can switch tools without losing anything.
8. Start with your next 10 messages. Don't go back and fill in old ones.

---

## Also in this repository

- **[Editing CLAUDE.md and skill files](docs/editing-claude-md-and-skills.md)**, a guide to keeping the instructions an AI agent follows short and correct.

