# Internship & New Grad Jobs Scraper API + H-1B Sponsors: examples

Internships, co-ops, new-grad and entry-level jobs from official public ATS APIs (Greenhouse, Lever, Ashby and more), with season, graduation year, visa sponsorship statements and DOL H-1B LCA sponsor history. Incremental: only new jobs.

This repo shows how to call the [Internship & New Grad Jobs Feed](https://apify.com/clearfeedlabs/entry-jobs-feed) Apify Actor from JavaScript or Python, and what the output looks like.

## What's new
- Small runs stop as soon as `maxItems` is filled: a default 8-job run takes ~5 s (was ~100 s).

## Use cases
- Students and new grads tracking early-career openings
- International students looking for likely visa sponsors
- University career centers and job newsletters
- Early-career job boards that need clean data

## Quick start
1. Create a free Apify account and copy your API token from Settings > Integrations.
2. Set it as an environment variable: `export APIFY_TOKEN=...` (never commit it).
3. Edit `input.json`, then run one of:
   - JavaScript: `npm i apify-client && node run.mjs`
   - Python: `pip install apify-client && python run.py`

## Output fields (first of many)
`atsJobId`, `ats`, `company`, `companySlug`, `title`, `department`, `team`, `locations`, `workplaceType`, `isRemote`, `employmentType`, `salary`, `descriptionHtml`, `applyUrl`, `jobUrl`, `postedAt`, `updatedAt`, `sourceUrl`

See `sample-output.json` for one trimmed record.

## Ready-made example tasks
- [Internships h1b employer details](https://apify.com/clearfeedlabs/entry-jobs-feed/examples/internships-h1b-employer-details)
- [New grad jobs h1b sponsors](https://apify.com/clearfeedlabs/entry-jobs-feed/examples/new-grad-jobs-h1b-sponsors)
- [Summer 2027 tech internships](https://apify.com/clearfeedlabs/entry-jobs-feed/examples/summer-2027-tech-internships)

## Pricing
Pay per result: **$2.50 per 1,000 jobs**, with no subscription. The [Store page](https://apify.com/clearfeedlabs/entry-jobs-feed) always shows current prices and every optional add-on event.

## FAQ
**Is this data official?** Yes. It comes from the public source named above, and each record links back to it.
**Do I need a login or proxy?** No. It uses documented public endpoints only.
**Can I schedule it?** Yes. Use Apify Schedules, the API or integrations (Zapier, Make, webhooks, MCP-compatible AI agents).

## Links
- Actor on the Apify Store: https://apify.com/clearfeedlabs/entry-jobs-feed
- Details & pricing: https://clearfeedlabs.com/actors/entry-jobs-feed/
- Clearfeed Labs: https://clearfeedlabs.com
- Bugs or questions: open an issue on the Actor's Issues tab on Apify.

Data comes from public sources and is provided as-is. Check the original source before relying on it. Not legal, financial or investment advice.

License: MIT
