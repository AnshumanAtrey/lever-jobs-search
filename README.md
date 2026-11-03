# Lever Jobs Scraper & API - Salary, Remote, Last 24 Hours

Lever jobs scraper and API: search the job sites of 2,300+ companies on Lever (jobs.lever.co and jobs.eu.lever.co) at once, live, and get each job's title, company, location, remote or onsite, job type, department, team, salary with its period, posting date and link, newest first. Turn on full details for the description as text and HTML, pay as numbers and the country.

Use it as a Lever jobs API with no Lever API key, a jobs.lever.co scraper or a daily job feed from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. It reads the public Lever Postings API and is the `site:jobs.lever.co` Google dork done at the source, with the fields a search result cannot give you. Available as an [Apify Actor](https://apify.com/anshumanatrey/lever-jobs-search). $0.0022 per job, $0.0023 with full details, $0.01 per run start at the default memory, no login, no API key.

## What does it do?

- **Searches 2,396 Lever job sites of 2,392 companies at once.** On 2026-11-03 they held 76,330 open jobs at 2,056 companies in 140 countries, at employers such as Palantir, Shield AI, Veeva Systems, Gopuff, Lyra Health, Zoox, Spotify, Engel & Völkers and Paytm.
- **Salary on the plain row, with its period.** When a company publishes pay, a third of the jobs and almost half of the US jobs, it comes with every row at no extra price, with the period Lever states: per year, per hour or per month.
- **One keyword is enough.** Type a job title and press Start. Leave the form empty for the newest jobs of every kind.
- **Newest first, read live.** Every job comes from Lever at the moment of your run, sorted by the time it was created.
- **Filters that take what people type.** London, Germany, EMEA, Remote, contract, internship, last 24 hours, or a pasted Google dork such as `site:jobs.lever.co/palantir intext:engineer`.
- **Checks job links.** Paste links from jobs.lever.co or jobs.eu.lever.co and each comes back open, closed or not found.

## How is it different from other Lever scrapers?

- **Every company on the list, read live.** Lever publishes no list of its customers, so a live reader normally needs a company name or link from you, and most actors that search every company read a stored copy. This one carries a list of 2,396 job sites built from the Wayback Machine, Common Crawl, freehire and GitHub lists, and reads all of them at the moment of your run. Of the 13 most used actors that name Lever (the table below), 8 search a stored copy, 3 need company names, links or a preset list, and 2 read a list of companies live across Greenhouse, Lever and Ashby: yugenox/ats-jobs-search and viridian_layout_ea2/company-career-site-jobs.
- **The real posting date.** Lever's own job page tells Google the day a job was created, and this actor sorts and filters by that moment, to the second (33 of 33 job pages checked on 19 sites agree). Jobs stay open for years on Lever, so Posted in the last is how to see only the new ones.
- **Pay with its period, never guessed.** Lever stores pay with its interval, so the period comes from Lever: per year on 15,379 jobs, per hour on 8,939 and per month on 801 on 2026-11-03. Ranges of 0 to 0 or 1 to 1, which companies set where they keep pay hidden, are not shown as pay.
- **Lever's EU sites too.** Companies on Lever's EU instance live only on jobs.eu.lever.co: 85 job sites on the list, with 2,968 open jobs on 2026-11-03, are read there.
- **Job type from the company's own words.** Lever leaves the job type to each company's words (Full-time, CDI, Contract: Part-Time, Werkstudent), and this actor reads them into five types where they name one: 82% of jobs.
- **You pay for what you get.** One charge per delivered row, plus the run start, and a spending limit stops the run cleanly with the jobs it paid for.

## When should I use it?

- **Job seekers and job boards:** new jobs by title, country and date across 2,300+ companies, with pay where it is published, on a daily schedule.
- **Recruiters and sourcing teams:** see who is hiring for a role right now, anywhere on Lever, and at what pay.
- **Sales and market research:** companies hiring for a function, by country and date, as a buying signal, and a list of the companies that hire through Lever.
- **Data teams and AI agents:** one clean, stable feed of Lever jobs through the API or MCP.

## How much does it cost to scrape Lever jobs?

Pay per event. Platform usage is included, and there is no monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.0022 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.0023 | One saved job with full details on |
| Run start | $0.005 per GB of memory | Charged by Apify when a run starts: once up to 1 GB and once more for each extra GB, so $0.01 at the default 2 GB |

On paid Apify plans the job prices are 10% less on Scale ($0.00198 and $0.00207) and 20% less on Business and above ($0.00176 and $0.00184); the run start stays $0.005 per GB.

| Run (Free and Starter price, default memory) | Cost |
|---|---|
| 100 newest jobs | $0.23 |
| 100 jobs with full details | $0.24 |
| 1,000 jobs | $2.21 |
| Every open Palantir job, 305 on 2026-11-03 | $0.68 |
| Every job on the list, 76,330 on 2026-11-03 | $167.94 |

Why a run start: Lever has no search, so the run start covers the fixed work of reading all 2,396 job sites on every search, whatever it finds. Apify's free $5 monthly credit covers about 2,100 jobs in runs of 100. Number of jobs (`maxJobs`) and the run start set the most a run can cost, and a run stops at its spending limit with a message saying so.

## How does the price compare with other Lever scrapers?

Every actor on the Apify Store that names Lever in its title, slug or description and had 50 or more users in the last 30 days, found by searching the Store for 12 Lever terms and 20 job terms on 2026-11-02 (3,631 actors read), ordered by users. Free-plan prices from each actor's current pricing.

| Actor | Users, 30 days | Per job | Start fee | Input |
|---|---|---|---|---|
| fantastic-jobs/career-site-job-listing-api | 1,632 | $0.012 | $0.01 | Keyword, from its own database of 58 ATS |
| fantastic-jobs/career-site-job-listing-feed | 282 | $0.0025 | $0.10 | The same database as a feed |
| hirebase/job-search | 137 | $0.005 | $0.001 | Keyword, from its own database of 20+ ATS |
| jobo.world/ats-jobs-api | 134 | $0.004 | $0.00005 | Keyword, from its own database of 75+ ATS |
| bovi/greenhouse-lever-ashby-job-scraper | 100 | $0.0015 | $0.00005 | Company names or preset lists, 6 ATS |
| factpipe/ats-jobs-feed | 98 | $0.003, $0.005 from 2026-11-06 | none | Keyword, from its feed of 19,000+ companies |
| yugenox/ats-jobs-search | 86 | $0.002 | none | Keyword across Greenhouse, Lever and Ashby boards, live |
| memo23/career-site-ats-jobs-api | 81 | $0.004 | $0.03 | Board links or company names, live |
| fantastic-jobs/lever-co-jobs-api | 76 | $0.0025 | none | Keyword, from its own database of Lever jobs of the last 6 months |
| jobspipe/jobspipe-job-search | 61 | $0.00196 | none | Keyword, from its index of 30+ job boards |
| jtpalms/ats-jobs-index | 60 | $0.003 | $0.00005 | Keyword, from its index refreshed twice a day |
| conserving_celerytop/live-career-page-jobs-api | 55 | $0.045 a company, up to 1,000 jobs | $0.00005 | Company names, websites or job board links, live |
| viridian_layout_ea2/company-career-site-jobs | 53 | $0.0015 | $0.00005 | Its list of 3,500+ Greenhouse, Lever and Ashby companies, or the ones you name, live |
| This actor | new | $0.0022, $0.0023 with details | $0.005 per GB, $0.01 at 2 GB | One keyword, all 2,396 Lever job sites, live |

Besides these 13, 1,547 listings name Lever, each with fewer than 50 users. Of those made for Lever alone, the two with the most users are lergassy/lever-jobs-scraper (11 users, $0.0012 a job, the companies you list) and jobo.world/lever-jobs-scraper-api (6 users, $0.004, its own index of Lever jobs).

Where others are cheaper: yugenox costs $0.002 a job with no start fee and reads Greenhouse, Lever and Ashby live; fantastic-jobs/lever-co-jobs-api, with no start fee, is also cheaper on the free plan for runs under 34 jobs (under 50 with details); bovi and viridian cost $0.0015 a job when you name the companies or use their own lists; jobspipe $0.00196 from its index; conserving_celerytop about $0.0005 a job at 100 jobs a company, and openclawai/career-site-ats-jobs-scraper (47 users) $0.0005 a job, when you know the companies. On paid plans fantastic-jobs/lever-co-jobs-api costs $0.002 on Starter, $0.0012 on Scale and $0.0008 on Business, against this actor's $0.0022, $0.00198 and $0.00176, and the fantastic-jobs feed the same plus its start fee; on Business, jobo.world ($0.0013) and jtpalms ($0.0015) are cheaper too. Most of these charge no start fee or Apify's default $0.00005. Where others do more: the database actors add fields extracted by AI and LinkedIn company data, and the multi-ATS ones cover many platforms in one run.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word: frontend also finds Front-End. A pasted Google dork or Lever link works too |
| Where the job is (`location`) | A city, state, country or region: London, United States, EMEA, LatAm. Worldwide finds jobs marked worldwide, global or anywhere, and Remote asks for remote jobs |
| Remote or onsite (`workType`) | remote, hybrid or onsite, as the company set it on Lever (99% of jobs); else Remote in a location or the title, or Hybrid in the title |
| Posted in the last (`postedWithin`) | 24 hours, 3 days, 7 days, 30 days, any time, or your own period such as 48 hours |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description as text and HTML, pay as numbers with its currency and period, country and country code |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or intern |
| Job type (`employmentType`) | full-time, part-time, contract, intern or temporary, where the company's own words name one |
| Match descriptions (`searchDescriptions`) | Finds your words in the description too, not only the title |
| Only these companies (`companies`) | A name (Palantir), the name in the address (palantir) or a Lever link. Empty searches everyone |
| Job links to check (`jobUrls`) | Paste job links to check whether they are still open, instead of searching |

Example input:

```json
{
  "searchTerms": ["software engineer"],
  "location": ["United States", "Canada"],
  "postedWithin": "7 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. These rows are from a run on 2026-11-03, build 1.0.1, searching every job site for software engineer in 58 seconds (run yBoCIZDTtcAkjBI1E): 2,022 jobs at 505 companies, the 100 newest saved; shown are rows 22, 24, 25, 28 and 73. 85 of the 100 were Jobgether's copies of 30 jobs, one per country, so the 100 rows held 45 different jobs (see Common questions).

| Job title (`title`) | Company name (`company`) | Main location (`location`) | Remote or onsite (`workType`) | Pay summary (`salary`) | Posted on (`postedAt`) |
|---|---|---|---|---|---|
| Staff Software Engineer ML Platform (6244) | Shield AI | San Diego, California | onsite | USD 200,000 - 300,000 per year | 2026-11-02 |
| Senior Software Engineer, Backend & AI Platform - Sureel AI | Warner Music Group | Munich | onsite |  | 2026-11-02 |
| Staff Software Engineer - Cloud Services | Agiloft | United States | remote |  | 2026-11-02 |
| Software Engineer | Intropic | London UK | hybrid |  | 2026-11-02 |
| Principal Software Quality Engineer | Weekday | Bengaluru | remote | INR 4,000,000 - 7,000,000 per year | 2026-11-02 |

One row as JSON:

```json
{
  "title": "Staff Software Engineer ML Platform (6244)",
  "company": "Shield AI",
  "location": "San Diego, California",
  "otherLocations": ["San Mateo, California"],
  "workType": "onsite",
  "employmentType": "full-time",
  "department": "Hivemind Enterprise Division",
  "team": "Engineering",
  "salary": "USD 200,000 - 300,000 per year",
  "postedAt": "2026-11-02T22:20:42Z",
  "jobUrl": "https://jobs.lever.co/shieldai/82e0ffd1-3887-4253-b458-00f39e0a387f",
  "applyUrl": "https://jobs.lever.co/shieldai/82e0ffd1-3887-4253-b458-00f39e0a387f/apply",
  "status": "open",
  "platform": "lever",
  "companySlug": "shieldai",
  "jobId": "82e0ffd1-3887-4253-b458-00f39e0a387f",
  "checkedAt": "2026-11-03T09:17:18+00:00"
}
```

Full details add `description`, `descriptionHtml`, `salaryMin`, `salaryMax`, `salaryCurrency`, `salaryPeriod`, `country` and `countryCode`. A checked link that is closed or not found comes back with its `status`, company and link, and the other fields empty. A run also writes an `OUTPUT` record: how many job sites were read, how many jobs matched and were saved, the job sites that could not be read, and any notes on how your input was read.

## How fast is it?

About 1 minute at the default 2 GB of memory: the empty form took 57 seconds and a search for software engineer 58 seconds (build 1.0.1, runs FxhK3ledZa4kIpTMl and yBoCIZDTtcAkjBI1E, 2026-11-03). Lever's Postings API has no word search, no date filter and no sort, so every search reads all 2,396 job sites, one call each for all but the 4 biggest, and a keyword takes about as long as the empty form. Full details and matching descriptions add no requests, because Lever sends each description with the job list. Naming companies or checking links reads only those sites.

## Common questions

### Which posting date does it use?

The moment the job was created on Lever. Lever's own job page gives Google that day as its date posted (33 of 33 job pages checked on 19 sites agree), and this actor sorts and filters by it, to the second. Lever's XML feed carries a later time, which is not used. Jobs stay open for years: on 2026-11-03, 17,792 open jobs (23.3%) had been created more than a year before, the oldest in 2009, so pick Posted in the last to see only new ones.

### Why does a keyword search take as long as an empty form?

The Lever Postings API answers with every open job of one job site, with no word search, date filter or sort. So every search reads all 2,396 job sites and matches your words itself. Naming companies in Only these companies reads only those sites, which is much faster.

### Why does the same job show up in many countries?

Some companies post one copy of a job per place. The biggest is Jobgether, a job-matching platform that posts jobs on Lever for the companies it shortlists candidates for, one copy per country: 4,298 of the 76,330 jobs (5.6%) on 2026-11-03, but because it posts many each day, it held 88 of the 100 newest jobs of any kind, 85 of the 100 newest software engineer jobs and 90 of the 100 newest product manager jobs that day. Each copy names a different place, so each is its own row, and there is no field yet to leave one company out.

### Why is the job type empty on some jobs?

Lever has no fixed job type: each company writes its own words (Full-time, CDI, Contract: Part-Time, PRN). This actor reads them into full-time, part-time, contract, intern or temporary where they name one type, 82% of jobs on 2026-11-03. The rest is empty: 5% of jobs have no job type words, and on 13% the words name no single type, such as Full-time or Part-time, Remote or Employee. A Job type filter leaves those jobs out.

### Is the pay yearly or hourly?

Lever stores pay with its period, and the row shows it: per year on 15,379 jobs, per hour on 8,939, per month on 801, per day on 119 and per week on 51 on 2026-11-03. Pay every two weeks, twice a month, every two months or one time keeps those words in the text and has no `salaryPeriod` (159 jobs). Ranges of 0 to 0 or 1 to 1, which companies set where they keep pay hidden, are not shown as pay.

### What about Lever's EU job sites?

Lever runs a separate EU instance, and its companies' job sites live only on jobs.eu.lever.co. 85 job sites on the list are EU sites, with 2,968 open jobs on 2026-11-03. Their job site name in `companySlug` ends in /eu, as in engelvoelkers/eu, and a jobs.lever.co link to one of them is found on the EU host too. One exception: a job link you paste to check, typed with jobs.lever.co, keeps the site name without /eu in `companySlug`, while its `jobUrl` is on jobs.eu.lever.co.

### How does it find every company?

Lever has no public list of its customers, so the list is built the way the `site:jobs.lever.co` dork works, from the web's own memory: the Wayback Machine's index of both hosts, Common Crawl's index, freehire's public job API and 11 company and job lists on GitHub gave 9,431 candidate names, each checked live with Lever's API. 2,396 job sites answer and their job pages open; left out are 467 sites whose job pages all answer 404 (their 1,412 links would be dead) and 12 demo and test sites. Of the job sites on the list, the Wayback Machine names 93%, Common Crawl 83%, the GitHub lists 75% and freehire 69%. An estimate from how often the sources overlap puts the job sites they can see at 2,468 or more, so the list holds at most about 97% of them; Lever's vendor listings say over 5,000 companies use it, and an account needs no public job site. To search a company that is not on the list, paste its link or type its name into Only these companies.

### Does it need a login or an API key?

No. The Lever Postings API is public and documented (github.com/lever/postings-api): it serves what each company's job site shows any visitor. Lever's other APIs need a customer's own key and read only that customer's data. You need only an Apify account.

### How do I run it from Python or an AI agent?

Through the Apify API, with your Apify token:

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/lever-jobs-search").call(run_input={"searchTerms": ["software engineer"]})
for row in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(row["title"], row["company"], row["location"], row["salary"], row["jobUrl"])
```

AI agents can call it through the Apify MCP server at https://mcp.apify.com, and n8n and Make have Apify nodes.

### Am I charged for closed jobs?

A search returns open jobs only. A pasted link that turns out closed or not found is one Job row, because it was checked and answered.

### Is it legal to use?

It reads public job postings. You are responsible for how you use the data, including each site's terms and the privacy laws that apply to you.

## Limitations

- Every search reads every job site, so a keyword takes about as long as the empty form, and every run pays the run start.
- Jobgether's copies of one job per country fill most of the newest results of many searches (see above), and there is no field yet to leave one company out.
- Jobs stay open for years: 23.3% of the open jobs on 2026-11-03 were created more than a year before.
- The job type is empty on 18% of jobs: 5% have no job type words and 13% have words that name no single type, such as Full-time or Part-time. The work type is empty on 0.6%.
- Pay is on 33% of jobs (47.4% of US jobs).
- `country` and `countryCode` belong to the job's main place; `otherLocations` lists the others as text (8.2% of jobs name more than one place).
- A US place named after a country can match that country: on 2026-11-03 a search for Mexico also found 123 jobs in New Mexico, Panama 37 in Panama City, FL, Jordan 16 in South and West Jordan, Utah, and Lebanon 23 in US towns named Lebanon.
- Lever answers a closed job and a job ID that never existed the same way, so both come back closed.
- Lever reads job site names in their own case (jobs.lever.co/AIFund answers, /aifund does not). Names on the list are found in any case; others are tried as typed and in lower case.
- A typed company name is matched to the list whole and with its accents: Engel & Völkers is found, Engel & Volkers is not, and Hot Topic finds the hottopic site, not the stores listed as BoxLunch & Hot Topic. The name in the address (engelvoelkers, boxlunch) always works.
- A few postings are not real openings and come back like any other: on 2026-11-03, 12 of 76,330 were test postings left open on real employers' job sites, such as "Test Job", and one was an "Our Jobs Site has Moved!" notice. Lever's own EU job site still lists 6 jobs from 2020.
- A job a company lists twice at one place, with the same team, department, job type, work type and pay, is delivered once (747 such copies on 2026-11-03). One title at one place for two stores, teams or pay ranges stays two rows.
- Titles and descriptions come in the company's own language.
- A job site Lever does not answer after the retries is counted in the run message and listed in the `OUTPUT` record (`boardsWithErrors`), and the run ends partial; when no job site could be read at all, the run fails with the reason.
- The list of job sites was built on 2026-11-03. A company that joined later is searched only when you name it.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | Use case |
|---|---|
| [ashby-jobs-search](https://apify.com/anshumanatrey/ashby-jobs-search) | Every job on every Ashby board, searched live |
| [workday-job-search](https://apify.com/anshumanatrey/workday-job-search) | Every job at 1,688 Workday employers, searched live |
| [cornerstone-jobs-search](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Every job on every Cornerstone career site |
| [deel-jobs-search](https://apify.com/anshumanatrey/deel-jobs-search) | Every job on every Deel ATS career page, with pay |
| [greenhouse-jobs-search](https://apify.com/anshumanatrey/greenhouse-jobs-search) | Jobs on Greenhouse job boards, searched live |
| [smartrecruiters-jobs-search](https://apify.com/anshumanatrey/smartrecruiters-jobs-search) | Jobs at SmartRecruiters companies, searched live |
| [workable-job-search](https://apify.com/anshumanatrey/workable-job-search) | Jobs on Workable job boards, searched live |
| [linkedin-harvester](https://apify.com/anshumanatrey/linkedin-harvester) | Email to LinkedIn profile, for the people behind a company |

## Documentation

- Apify Store: https://apify.com/anshumanatrey/lever-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/lever-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-11-03 (version 1.0)
