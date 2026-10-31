# data backup services: what actually matters when choosing one, with real pricing from Sharktech's Acronis backup and S3 storage

Outsourcing your backups comes down to three questions: what gets protected, how much it costs per month, and how painful recovery is when something breaks. Most "data backup services" articles you'll find are vendor-neutral explainers that stop right before the part you actually need — concrete prices and plan differences. This one doesn't. Below you'll find the full published pricing for Sharktech's Acronis-based backup service (starting at **$4/month with 200GB included**), their S3 object storage option at **$4.90/TB/month**, how the two differ, and the math on which billing cycle actually saves you money.

> **Quick take:** If you want a managed backup for servers, VMs, or workstations without touching backup software yourself, Sharktech's Acronis Cyber Protection service is the fit — it starts at $4/month with 200GB of cloud storage and no long-term contract. If you run your own backup software and just need cheap, compatible storage to back up into, skip ahead to the S3 section. 👉 [Open Sharktech's Acronis backup configuration page](https://portal.sharktech.net/aff.php?aff=1626&pid=648)

## Backup as a service, in one paragraph

Backup as a service (BaaS) means a third party stores copies of your data in their infrastructure, and you define what gets backed up, how often, and how far back versions go. The whole point is the off-site copy: your production data gets copied over a secure connection to the provider's servers, so a fire, ransomware attack, or deleted folder on your end doesn't take the backup down with it. Sharktech's own FAQ cites a stat worth sitting with — 70% of small businesses close after a major data loss event. That's the problem this category exists to solve.

What separates providers at the purchasing stage is usually three things: whether pricing is per user or per capacity, whether you get locked into a contract, and who's accountable when a restore doesn't work. Keep those in mind as we go through the plans.

## Sharktech's two backup routes, and the full price table

Sharktech sells two different things under the backup umbrella, and confusing them is the fastest way to buy the wrong one.

**Route 1: Managed Acronis backup.** Sharktech runs Acronis Cyber Protection as a hosted service. Acronis is the backup engine — one of the most established names in the category — and Sharktech handles the hosting, the storage, and 24/7 support. You manage everything through the Acronis web console. This is the choice if you want backup to be someone else's operational problem.

**Route 2: S3 Object Storage.** You bring your own backup software (Rclone, Cyberduck, Nextcloud, S3 Browser, or anything S3-compatible) and Sharktech provides the storage bucket. Cheaper per terabyte, but you're the one wiring it up.

Here's the published pricing across both routes:

| Plan | Billing cycle | Included storage | Overage rate | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Acronis Backup | Monthly | 200GB | $0.02/GB | **$4/mo** | [ Configure Acronis monthly](https://portal.sharktech.net/aff.php?aff=1626&pid=648) |
| Acronis Backup | Every 3 months | 200GB | $0.04/GB | $8/quarter | [ Configure Acronis quarterly](https://portal.sharktech.net/aff.php?aff=1626&pid=648) |
| Acronis Backup | Every 6 months | 200GB | $0.06/GB | $12/semi-annual | [ Configure Acronis semi-annually](https://portal.sharktech.net/aff.php?aff=1626&pid=648) |
| Acronis Backup | Annual | 200GB | $0.12/GB | $24/year | [ Configure Acronis annually](https://portal.sharktech.net/aff.php?aff=1626&pid=648) |
| S3 Object Storage | Monthly | Pay as you grow | $0.90/TB transfer beyond first 1TB | **$4.90/TB/mo** | [ View Sharktech's backup storage options](https://bit.ly/SharKtech) |

Two things to know before you click through. The four Acronis billing-cycle prices above are Sharktech's published rates for this service as announced by the company, and they remain consistent with the current $4/month starting point on the product page. That page also notes the final recurring price depends on the capacity and license options you select at checkout — the cart shows the itemized total before you confirm anything, so treat the table as the published baseline and the cart as the source of truth. File Sync & Share is available as a paid add-on, with its own capacity pricing: $0.03/GB/month, $0.06/GB/quarter, $0.12/GB/semi-annual, or $0.24/GB/year, stacked on top of the backup price.

## The real cost math nobody else shows you

The four Acronis billing cycles aren't evenly priced, and the differences are bigger than they first look. Here's what each one costs over a full year:

- Monthly: $4 × 12 = **$48/year**
- Quarterly: $8 × 4 = **$32/year**
- Semi-annual: $12 × 2 = **$24/year**
- Annual: $24 × 1 = **$24/year**

Paying month-to-month costs exactly double the annual plan for the same 200GB. The semi-annual and annual plans land at the same yearly total, so there's no penalty for preferring the shorter commitment between those two.

The overage rates follow the same pattern. Monthly billing charges $0.02 per extra GB each month, which works out to $0.24 per GB over a year; the annual plan charges $0.12 per GB for the whole year. In other words, the overage rate per year of usage is half as expensive on the annual plan — so the longer cycles win on both the base price and the overage math. If your backup set is going to outgrow 200GB, and most business backup sets do, that compounds rather than cancels out.

There's no official word on whether renewal prices differ from first-term prices, so treat the figures above as the ongoing rate rather than a first-year teaser. And a purchasing note worth flagging: third-party write-ups point out that the service ships without a money-back guarantee, and Sharktech's own pages don't advertise one either. Practically, that means the semi-annual plan is the low-risk way to get near-annual pricing — you're only ever prepaying six months while paying the same annualized rate.

## What the Acronis service actually covers

The service protects physical servers, virtual machines, and cloud workloads across Windows, Linux, and macOS. You register systems in the Acronis web console independently of your server control panel, set protection plans per system, and monitor backup activity from there — including failed jobs, which is the detail that matters, since a backup that silently fails for three months is worse than no backup.

Recovery granularity runs from a single file up to a full machine. You pick a recovery point and a target in the console, and restore time depends on data size and method. Backup schedules and retention periods are customizable per system, so a database server and an employee laptop can run on completely different plans under one account.

A couple of honest caveats from the official product page. Encryption and access controls are included in the data protection layer, but some additional security and disaster-recovery features depend on which license you select at order time — worth confirming before checkout rather than discovering later. Application-level protection (think SQL databases or Exchange) also depends on workload support and licensing, so if that's your use case, verify it covers your specific stack.

Sharktech's pitch on price is "half the cost compared to competitors" — that's their own claim, but the $4/month floor is verifiable on their own pages, and there are no long-term contracts holding you in. The company has been operating since 2003, reports 1,000+ customers across 72 countries, and claims at least 20% savings versus hyperscale public cloud pricing. All of that is their official wording; the contract-free part is the piece that actually lowers your risk, since you can walk away at the end of any billing cycle.

If that setup sounds right for your environment, 👉 [open the Acronis configuration page and price your exact setup](https://portal.sharktech.net/aff.php?aff=1626&pid=648) — the cart breaks out every option before you commit.

## When S3 Object Storage is the better call

Already run Veeam, Restic, Duplicati, or any backup tool that speaks S3? Then paying for a managed Acronis layer duplicates something you already have. Sharktech's S3 Object Storage costs **$4.90/TB/month** with no complicated tiering — their own examples: 1TB runs $4.90/month, 10TB runs $49/month, 100TB runs $490/month. The first 1TB of outbound transfer each month is included; beyond that it's $0.90/TB, which matters because egress fees are where cheap backup storage usually ambushes you during a restore.

Under the hood it's high-capacity HDD storage with an NVMe cache layer for the active data path, exposed through a standard S3-compatible API. You get object versioning, object lock for retention, lifecycle rules, and pre-signed URLs for time-limited sharing. For backups specifically, object lock is the feature worth caring about — it prevents backed-up copies from being deleted or altered during the retention window, which is exactly what you want when ransomware is the threat model.

Two limits to respect. First, this is capacity-first object storage — Sharktech explicitly says it's not a replacement for all-flash block storage, so it's for backup sets, archives, media libraries, logs, and build artifacts, not for boot volumes or anything needing consistent low latency. Second, if you exceed 100TB of storage or 300TB of monthly transfer, pricing goes through their sales team instead of the published rate.

## How this pricing compares to per-user backup services

Most backup services you'll see recommended price per user per year, which makes them cheap-looking for a five-person team and painful for anything server-heavy. A concrete data point: NetApp's SaaS Backup for Microsoft 365 starts at $45 per user per year, sold in one-to-five-year subscription terms. For a Microsoft 365-only shop, that model is fine. The moment you're protecting servers, VMs, or databases, per-user pricing stops matching what you're actually backing up — a single file server with no "users" still needs protection.

That's the structural difference with Sharktech's approach: capacity-based pricing, where a 200GB starting plan costs $4–24 a year depending on billing cycle, and you scale by buying more gigabytes rather than more seats. Big enterprise platforms like Veeam or Cohesity offer deeper ecosystem integration across AWS, Azure, and Google Cloud, and for a large multi-cloud estate they may be the right layer. But their entry cost and complexity are built for organizations with dedicated IT staff. If your situation is "a handful of servers and a budget," the comparison mostly ends at the price table above.

## What existing Acronis users report

Since Sharktech's service runs on Acronis, third-party data about Acronis itself is relevant. On SoftwareReviews, Acronis Cyber Backup scores **8.7/10** in the Backup and Availability category, with 92% positive user sentiment, an 89 out of 100 likelihood-to-recommend, and a 98 plan-to-renew score — that last number is the one worth weighing, since it reflects whether existing customers stay.

The highest-rated features in that data: automated backup testing and verification (92, meaning it verifies restore integrity rather than just reporting that a job finished), backup automation via REST API and CLI (90), and cloud data backup (87). Individual reviewers back this up — one transportation-industry user rated it 9/10 and said it "works smoothly and it is very easy to manage" with no prior knowledge required; a banking-sector user highlighted full system drive backup and cloning plus multiple encryption options. Both stated they hadn't found real downsides.

Treat all of that as feedback on the Acronis platform rather than on Sharktech's hosting of it — Sharktech's own service hasn't accumulated the same volume of independent reviews, and I won't pretend otherwise.

## FAQ

**Is there a long-term contract?** No. Sharktech states their backup services run without long-term contracts, and the billing cycles listed are prepayment periods, not lock-ins — the semi-annual plan costs the same per year as the annual one if you want the discount without a full-year commitment.

**Will it work with my operating system?** The Acronis service covers supported Windows, Linux, and macOS systems, including physical machines, VMs, and cloud workloads. If you're running something more exotic (AIX, certain Unix variants), that's a licensing and workload-support question to confirm with their team before ordering, since their support desk is available 24/7.

**What happens if I outgrow 200GB?** Extra storage bills at the overage rate for your billing cycle — $0.02/GB monthly up to $0.12/GB annually. You can also adjust capacity in the customer portal and watch your consumption in the Acronis console before you hit the limit.

**What is File Sync & Share, and do I need it?** It's an optional add-on that syncs and shares files across devices, priced at $0.03/GB/month on top of your backup plan. If your goal is purely backup, you can skip it — it's a separate use case, and the per-gigabyte cost only makes sense if you actually want the sync feature.

**Do I need backup software for the S3 option?** Yes, and that's the trade. You connect whatever S3-compatible tool you already use — the officially listed ones are Rclone, Cyberduck, Nextcloud, and S3 Browser — or integrate through the API directly.

## Which plan to pick, based on your situation

Running servers or VMs you want fully managed, with someone to call at 3am? The Acronis service is built for that. Based on the verified pricing, the **semi-annual plan at $12** is the value pick for most people: it annualizes to the same $24/year as the annual plan while only ever prepaying six months, and it avoids the $48/year month-to-month rate entirely. Choose annual instead if you'd rather handle billing once a year and the prepayment doesn't bother you. Just need durable storage for the backup tool you already run? S3 Object Storage at $4.90/TB with 1TB of included egress will undercut most hyperscale buckets, and the object lock feature handles ransomware-style retention. If you're protecting only a few Microsoft 365 mailboxes, a per-user service like NetApp's is a legitimate alternative — capacity pricing shines once servers enter the picture.

Before you order either one: check whether your backup set already exceeds 200GB (that decides your overage exposure), skip File Sync & Share unless you actually want file syncing, and confirm the license options in the cart cover the security features you actually need — since there's no advertised money-back guarantee, treat the first term as committed spend. Then 👉 [configure your Sharktech backup plan and see the exact total before checkout](https://portal.sharktech.net/aff.php?aff=1626&pid=648) — the itemized price is right there, with no annual lock-in behind it.
