# Deel Jobs Scraper & API - All Deel ATS Career Pages with Pay

Deel jobs scraper and API: search every company's career page on Deel ATS (jobs.deel.com) at once, live, and get each job's title, company, location, remote or onsite, job type, department, team, pay, posting date and link, newest first. Turn on full details for the description, pay as numbers and the country.

Use it as a Deel jobs API, a jobs.deel.com scraper or a daily job feed from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. It is the `site:jobs.deel.com` Google dork done at the source, with the fields a search result cannot give you. Available as an [Apify Actor](https://apify.com/anshumanatrey/deel-jobs-search). $0.0025 per job, $0.0035 with full details, no start fee, no login, no API key.

## What does it do?

- **Searches 161 career pages of 159 companies at once**, in about 4 seconds. 1,300+ open jobs in 112 countries, at companies such as Deel itself, Klarna, ExpressVPN, OffSec, Kushki, Holafly, Ledn, dott, Zema Global and Cochrane.
- **Pay on the plain row.** When a company publishes pay, about a third of the jobs, it comes with every row at no extra price.
- **One keyword is enough.** Type a job title and press Start. Leave the form empty for the newest jobs of every kind.
- **Newest first, read live.** Every job comes from Deel at the moment of your run, not from a stored copy.
- **Filters that take what people type.** Germany, EMEA, Remote, contract, last 24 hours, or a pasted Google dork such as `site:jobs.deel.com/klarna intext:engineer`.
- **Checks job links.** Paste links and each comes back open, closed or not found.

## How is it different from other Deel scrapers?

- **You do not need to know the companies.** Deel publishes no list of the companies on its ATS, so a live reader normally needs the name, link or domain from you. This actor carries a list built from web archives and search engines, so one search covers all of them and a job title finds companies you had never heard of.
- **It is the only actor made for Deel alone.** Others treat it as one platform among dozens. This one reads what Deel really stores: work type, job type, department, team, pay and every location.
- **The real posting date.** Deel keeps two dates: when a draft was made and when it was published. This actor gives the published one, the date Deel's own job page hands to Google (10 of 10 pages checked). In a sample of 1,033 jobs, 175 had them more than a week apart.
- **Full text at no extra time.** Deel sends each description with the job list, so matching your words inside descriptions costs no extra requests: python finds 6 jobs by title and 167 by description.
- **A failed read costs nothing.** You pay per delivered row.

## When should I use it?

- **Job seekers and job boards:** remote and international jobs at startups and fintechs, many with pay, on a daily schedule.
- **Recruiters and sourcing teams:** see who is hiring for a role across every company on Deel, and at what pay.
- **Sales and market research:** companies on Deel hire across borders, which makes them a ready list for anyone selling to remote-first and global teams.
- **Data teams and AI agents:** one clean, stable feed of Deel jobs through the API or MCP.

## How much does it cost to scrape Deel jobs?

Pay per event. Platform usage is included, and there is no start fee or monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.0025 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.0035 | One saved job with full details on |

On paid Apify plans these are 10% less on Scale ($0.00225 and $0.00315) and 20% less on Business and above ($0.002 and $0.0028).

| Job (Free and Starter price) | Cost |
|---|---|
| 100 newest jobs | $0.25 |
| 100 jobs with full details | $0.35 |
| Every job on the list, about 1,300 | $3.25 |
| Every job with full details | $4.55 |

Apify's free $5 monthly credit covers about 2,000 jobs, more than every open job on the list. Number of jobs (`maxJobs`) sets the most a run can cost, and a run stops at its spending limit with a message saying so.

## How does the price compare with other Deel scrapers?

Every actor on the Apify Store that lists Deel among the platforms it reads, found by reading the listings of 563 job actors on 2026-10-30, ordered by users in the last 30 days. Free-plan prices from each listing.

| Actor | Users, 30 days | Per job | Start fee | Covers |
|---|---|---|---|---|
| fantastic-jobs/career-site-job-listing-api | 1,668 | $0.012 | $0.01 | 58 ATS from its own database; `deel` is one filter |
| fantastic-jobs/career-site-job-listing-feed | 284 | $0.0025 | $0.10 | The same database as a feed |
| memo23/career-site-ats-jobs-api | 85 | $0.004 | $0.03 | 116 ATS, the boards or company names you give it |
| parseforge/career-site-jobs-scraper | 7 | $0.004 | $0.002 | 21 ATS and feeds, the companies you name |
| hydrafetch/company-jobs-scraper | 2 | $0.003 | $0.00005 | The domains you give it, plus $0.01 a company |
| om_kh/ats-jobs-api | 1 | $0.0015 | none | 77 ATS, the domains you give it |
| This actor | new | $0.0025 | none | Deel only, every company on the list with no links needed |

Where others are cheaper: om_kh costs less per job when you already know the company's domain. Where others do more: the multi-ATS actors cover many platforms in one run.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word: frontend also finds Front-End. A pasted Google dork or Deel link works too |
| Where the job is (`location`) | A city, state, country or region: London, United States, EMEA, LatAm. Worldwide finds jobs open everywhere, and Remote asks for remote jobs |
| Remote or onsite (`workType`) | remote, hybrid or onsite, as the company set it on Deel |
| Posted in the last (`postedWithin`) | 24 hours, 3 days, 7 days, 30 days, any time, or your own period such as 48 hours |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description as text and HTML, pay as numbers with its currency, country and country code |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or intern |
| Job type (`employmentType`) | full-time, part-time, contract, intern or temporary |
| Match descriptions (`searchDescriptions`) | Finds your words in the description too, not only the title |
| Only these companies (`companies`) | A name (Klarna), the name in the address (klarna) or a Deel link. Empty searches everyone |
| Job links to check (`jobUrls`) | Paste job links to check whether they are still open, instead of searching |

Example input:

```json
{
  "searchTerms": ["software engineer"],
  "location": ["Germany", "United States"],
  "postedWithin": "30 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. These rows are from a run on 2026-10-30, build 1.0.2, searching every company for software engineer in 3 seconds (28 jobs at 14 companies):

| Job title (`title`) | Company name (`company`) | Main location (`location`) | Remote or onsite (`workType`) | Pay summary (`salary`) | Posted on (`postedAt`) |
|---|---|---|---|---|---|
| Staff Software Engineer | Offsec Services | Remote | remote |  | 2026-10-21 |
| Software Engineer (Python/AWS) | Zema Global | London, United Kingdom | hybrid |  | 2026-10-12 |
| Senior Frontend Software Engineer | Arcadian Consulting | SPE Culver City - Hybrid, United States | hybrid | USD 79 - 85.50 | 2026-09-28 |
| Founding Software Engineer | Percept | RescueSight Inc., United States | hybrid | USD 150,000 - 300,000 | 2026-08-14 |

One row as JSON:

```json
{
  "title": "Senior Frontend Software Engineer",
  "company": "Arcadian Consulting",
  "location": "SPE Culver City - Hybrid, United States",
  "otherLocations": [],
  "workType": "hybrid",
  "employmentType": "full-time",
  "department": "Department",
  "team": "Sony Staff Aug",
  "salary": "USD 79 - 85.50",
  "postedAt": "2026-09-28T23:49:12.188Z",
  "jobUrl": "https://jobs.deel.com/arcadian-consulting/job-details/fa835a29-a136-46e0-a259-0857e6db86ad/overview",
  "applyUrl": "https://jobs.deel.com/arcadian-consulting/job-details/fa835a29-a136-46e0-a259-0857e6db86ad/application",
  "status": "open",
  "platform": "deel",
  "companySlug": "arcadian-consulting",
  "jobId": "fa835a29-a136-46e0-a259-0857e6db86ad",
  "checkedAt": "2026-10-30T15:41:01+00:00"
}
```

Full details add `description`, `descriptionHtml`, `salaryMin`, `salaryMax`, `salaryCurrency`, `country` and `countryCode`. A run also writes an `OUTPUT` record: how many career pages were read, how many jobs matched and were saved, and any notes on how your input was read.

## How fast is it?

Every career page in 4 seconds at the default 1 GB of memory (run Fivfgrlt0o9s0dnek, 2026-10-30, 100 newest jobs). Deel returns a whole company in one answer, so full details and matching descriptions add no time.

## Common questions

### Why does some pay look small?

Deel stores an amount and a currency with no period, and companies use it for hourly, monthly and yearly pay alike: USD 17 - 18, PLN 5,500 - 6,500 and USD 160,000 - 210,000 are all real rows. This actor shows what the company wrote and never guesses the period, so read the amount with the job. Some jobs give only one amount.

### How does it find every company?

Deel has no list, so the list is built the way the `site:jobs.deel.com` dork works: the Wayback Machine, Common Crawl's index, search engines and public GitHub files gave 184 candidates, and 161 of those pages answer. Testing 31,728 other company names found only 9 more. That list cannot be proven complete, so to search a company that is not on it, paste its link or type its name into Only these companies.

### Does it need a login or an API key?

No. Deel's official ATS API needs a customer's own token and reads only that customer's jobs. This actor reads what each career page shows any visitor. You need only an Apify account.

### How do I run it from Python or an AI agent?

Through the Apify API, with your Apify token:

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/deel-jobs-search").call(run_input={"searchTerms": ["software engineer"]})
for row in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(row["title"], row["company"], row["location"], row["salary"], row["jobUrl"])
```

AI agents can call it through the Apify MCP server at https://mcp.apify.com, and n8n and Make have Apify nodes.

### Am I charged for closed jobs?

A search returns open jobs only. A pasted link that turns out closed or not found is one Job row, because it was checked and answered.

### Is it legal to use?

It reads public job postings. You are responsible for how you use the data, including each site's terms and the privacy laws that apply to you.

## Limitations

- Deel is a small ATS: about 1,300 open jobs, and Deel and Klarna hold a quarter of them. For a wide search across many employers, use a multi-ATS actor or a bigger platform.
- Pay has no period, and about two thirds of jobs show no pay.
- Titles and descriptions come in the company's own language.
- A job can list dozens of countries: the first is `location`, the rest are in `otherLocations`.
- Some postings are open applications, such as "Work With Us", because Deel lists them as jobs.
- The same job on a copied career page is delivered once, matched by company, title and place.
- The list of career pages was built on 2026-10-30. A company that joined later is searched only when you name it.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | Use case |
|---|---|
| [ashby-jobs-search](https://apify.com/anshumanatrey/ashby-jobs-search) | Every job on every Ashby board, searched live |
| [workday-job-search](https://apify.com/anshumanatrey/workday-job-search) | Every job at 1,688 Workday employers, searched live |
| [cornerstone-jobs-search](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Every job on every Cornerstone career site |
| [linkedin-harvester](https://apify.com/anshumanatrey/linkedin-harvester) | Email to LinkedIn profile, for the people behind a company |

## Documentation

- Apify Store: https://apify.com/anshumanatrey/deel-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/deel-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-10-30 (version 1.0)
