# RackNerd 黑五 (Black Friday) VPS Deals: $21.99/Year KVM Plans Compared — Which Package to Pick, How to Order, What Locations to Choose (Full Specs & Buying Guide)

A friend texted me last week: "RackNerd 黑五 is coming up — should I grab one?" He'd been running his blog on a $5/month shared host that kept crawling during traffic spikes, and he'd heard the Chinese VPS crowd treats the annual Black Friday drop like a holiday. I told him yes, but also told him to slow down, because the "which plan" question matters more than the "should I buy" question.

So this is the post I wish someone had written for him.

RackNerd 黑五 — short for "RackNerd Black Friday" — is the once-a-year window when this US-based hosting provider releases deeply discounted KVM VPS plans, usually priced well below their normal specials, with annual-only billing and limited stock that tends to sell out within hours. The community refers to it casually as "黑五," and the deals typically start somewhere in the $10–$22 per year range depending on the configuration and the year. 👉 [See current RackNerd VPS specials](https://my.racknerd.com/aff.php?aff=11397&pid=952)

## What the RackNerd 黑五 Deals Actually Look Like

The Black Friday lineup is almost always five KVM VPS tiers, ranging from a 1 GB entry box to an 8 GB workhorse. The same structure carries over to the year-round specials page, which is what you can actually order today if you're reading this outside the Black Friday window. Here's the full current RackNerd VPS specials table:

| Plan | CPU | RAM | SSD Storage | Monthly Transfer | Network Port | Price | Order |
|------|-----|-----|-------------|-----------------|--------------|-------|-------|
| 1 GB KVM VPS | 1 vCPU Core | 1 GB | 20 GB | 3 TB | 1 Gbps | $21.99/yr |  [Grab the 1 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=952) |
| 2 GB KVM VPS (Most Popular) | 2 vCPU Cores | 2 GB | 35 GB | 5 TB | 1 Gbps | $35.99/yr |  [Grab the 2 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=953) |
| 4 GB KVM VPS | 3 vCPU Cores | 4 GB | 60 GB | 7 TB | 1 Gbps | $59.99/yr |  [Grab the 4 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=954) |
| 6 GB KVM VPS | 6 vCPU Cores | 6 GB | 100 GB | 12 TB | 1 Gbps | $89.99/yr |  [Grab the 6 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=955) |
| 8 GB KVM VPS | 7 vCPU Cores | 8 GB | 150 GB | 20 TB | 1 Gbps | $119.99/yr |  [Grab the 8 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=956) |

Every plan ships with the same baseline: one dedicated IPv4 address, full root admin access, KVM virtualization, SolusVM control panel, RAID-10 SSD storage, and a choice of datacenter location at checkout.

The 2 GB plan is the one RackNerd themselves badge as "Most Popular" — and honestly, for most personal projects, that's the sweet spot. The price gap to the 1 GB is small enough that you won't regret the headroom, and the extra vCPU core makes a real difference the first time you run a backup or a software update while the site is still serving traffic.

## Which RackNerd 黑五 Plan Fits Your Use Case

Picking a plan isn't about grabbing the biggest number. It's about matching the box to what you actually run. Here's how I'd break it down:

- **Personal blog or a tiny static site:** the 1 GB plan is enough. WordPress with a caching plugin and a low-traffic site will idle at 300–500 MB of RAM. You'll have headroom.
- **Small business site, a forum, or a modest Docker setup:** the 2 GB plan. This is where you stop worrying about OOM kills during backups or plugin updates. I've run a Ghost blog plus a Plausible analytics instance on a 2 GB box for over a year without a hiccup.
- **Real web app, multiple Docker containers, or a dev environment with databases:** 4 GB. Once you add Postgres, Redis, and the app itself, 2 GB gets tight fast.
- **Hosting multiple sites, running CI runners, or heavier workloads:** 6 GB or 8 GB. At this tier you're basically running a small server, and the CPU cores matter as much as the RAM.

Quick summary: when in doubt, get the 2 GB. It's the most versatile plan in the lineup, and it's the one RackNerd's own team marks as the default recommendation.

## How to Order a RackNerd VPS, Step by Step

The ordering flow is short. Here's the whole thing:

1. Click any of the plan links in the table above to land directly on the order page for that specific configuration.
2. Pick your datacenter location from the dropdown. Los Angeles DC-02 and San Jose are the usual picks for Asia-facing traffic; New York and Chicago for Europe; Seattle for Pacific Northwest.
3. Choose an operating system — CentOS, Rocky Linux, AlmaLinux, Fedora, Debian, and Ubuntu are all one-click options. Custom ISOs are available via support ticket if you need something else.
4. Pick a billing cycle. The specials price is locked in for annual billing, and renewals are at the same price — not a teaser that jumps later.
5. Checkout. You'll get a SolusVM login and root credentials in your welcome email within minutes.

That's it. No phone verification, no setup fee, no minimum commitment beyond the year you're paying for.

## Locations, Network Specs, and What You're Really Paying For

RackNerd operates 20 datacenter locations across North America, Europe, and Asia. The full list includes Los Angeles (multiple DCs), San Jose, Seattle, Dallas, Chicago, New York, Ashburn, Atlanta, Tampa, Toronto, Amsterdam, London, Dublin, and Strasbourg. Coverage is genuinely global for a budget provider — most competitors at this price point offer maybe three or four locations, not twenty.

The network runs at 1 Gbps on every plan. There's no "upgrade to fast network" upsell hidden in the cart. Bandwidth is metered (the "Monthly Transfer" column in the table), but in practice the limits are generous enough that you'd have to be running a media-heavy site or getting DDOS'd to come close to them — and even if you do cross the line, the box doesn't get cut off, it just gets throttled to 10 Mbps until the next billing cycle.

Storage is RAID-10 SSD across the VPS specials. That's the part that matters more than people realize — RAID-10 means both striping for speed and mirroring for redundancy, so a single drive failure doesn't take your box down and your data doesn't vanish because one disk died.

One honest caveat: RackNerd's network is "premium but unoptimized." Translation — there's no CN2 GIA or similar China-routed magic. For users in China, ping to Los Angeles DC-02 typically lands somewhere in the 150–180ms range, which is fine for hosting a site that visitors load in a browser, but not ideal for latency-sensitive tasks like real-time game servers or SSH-heavy development work where every keystroke round-trips across the Pacific.

## What's Actually Included (and What Isn't)

People get burned on VPS purchases when they assume "cheap VPS" means "cheap managed hosting." It doesn't. Here's the honest breakdown of what comes in the box and what you're on your own for.

**What's included:**
- One dedicated IPv4 address (you can buy more IPs as add-ons)
- Full root access via SSH
- SolusVM control panel for reboots, OS reinstalls, rDNS management
- KVM virtualization (not OpenVZ — this matters, because KVM gives you a real kernel and lets you run Docker, custom kernels, VPN software, anything that needs full virtualization)
- Choice of Linux OS from the one-click installer
- Free Clientexec license (billing system, normally $11.95/month — genuinely a freebie, not a teaser)
- 24/7 support ticket access for infrastructure issues

**What's not included:**
- No cPanel by default (it's available as a paid add-on if you really want it)
- No one-click WordPress installer (you'll install WordPress yourself, which takes about 10 minutes once you've done it once)
- No managed support for your application — RackNerd's team keeps the box online, but they don't fix your broken WordPress plugin or debug your Docker compose file
- No automatic backups (you set up your own cron + rsync, or use a service like restic)

If you've never SSH'd into a server before, you'll either need to learn or stick with shared hosting. The good news: the learning curve for "keep a small Linux box running" is maybe a weekend of reading, and once you've got it, you've got it forever.

## Is the RackNerd 黑五 Hype Justified? My Honest Take

Short version: yes, with one condition.

The prices are genuinely cheap. $21.99/year for a 1 GB KVM box works out to under $1.83/month — that's less than a cup of coffee in most cities. The 2 GB at $35.99/year is $3/month even. For anyone who's been paying $5–10/month for shared hosting that falls over on the second visitor, the math is brutal in favor of switching.

The condition: know what you're buying. This is unmanaged VPS. There's no cPanel by default, no one-click WordPress installer, no "support will fix your site" safety net. You get root, you get the box, and you're responsible for keeping it patched and backed up. If you've never SSH'd into a server before, you'll either need to learn or stick with shared hosting.

I've had a RackNerd box in Los Angeles DC-02 for the better part of two years. Uptime has been solid — I've had maybe two reboots in that span, both for planned maintenance that came with advance notice. Support tickets get answered within a few hours, even on weekends. Nothing to write home about, but nothing to complain about either.

The renewal price matches the purchase price. This is the part that actually sold me — a lot of hosts run "$X for the first year, 3X on renewal" traps that look cheap until you get the second-year invoice. RackNerd doesn't. What you pay year one is what you pay year five.

If you're not sure whether the platform is right for you, the practical move is to grab the 2 GB plan, spend a weekend setting it up, and if it doesn't work for you, just let it lapse at the end of the year. You're out $36. That's a cheaper experiment than almost any other tech purchase I can think of.

## What to Do If You're Reading This Outside Black Friday

The actual Black Friday drop tends to be a flash event — the deepest discounts sell out within hours, sometimes within the first hour, and once the stock is gone it's gone until the next year. If you're reading this in, say, July, you've got a few options:

**Option one:** grab one of the year-round specials from the table above. The pricing is higher than the Black Friday flash deals, but it's still aggressive compared to almost any other VPS provider in the same spec tier, and the box is available right now instead of "maybe in November."

**Option two:** wait for Black Friday and set a calendar reminder. RackNerd historically announces the drop a few days ahead on their site and through their community channels. The flash deals usually start somewhere around 10–18% below the year-round specials for the same tier, with the entry-level 1 GB occasionally dipping into the $10–11/year range.

**Option three:** do both. Grab a year-round special now so you've got a working box, then pick up a second Black Friday box in November for whatever new project you're cooking up. At these prices, running two small VPS boxes is still cheaper than one mid-tier shared hosting plan from a lot of mainstream providers.

## Frequently Asked Questions

**Q: Is the RackNerd Black Friday price a one-time teaser or the real recurring price?**
A: The Black Friday price is locked for the life of the account. Renewals are billed at the same rate you paid initially — no jump, no surprise, no "first-year discount" that vanishes on invoice two.

**Q: Can I upgrade my plan later without losing my data?**
A: Yes. RackNerd supports in-place upgrades via support ticket. You pay the prorated difference between your current plan and the new one, and they bump your RAM and CPU allocation without wiping the disk or reinstalling the OS.

**Q: Which location should I pick if most of my visitors are in China?**
A: Los Angeles DC-02 and San Jose are the two West Coast locations that consistently give the best routes to China. Neither is "optimized" in the CN2 GIA sense, but they're the best of what's available on the RackNerd network, and the ping difference between them and the East Coast locations is significant.

**Q: Does RackNerd offer Windows VPS?**
A: The standard specials listed in the table above are Linux-only (CentOS, Rocky, AlmaLinux, Fedora, Debian, Ubuntu). Windows is available on other RackNerd plans — if you specifically need Windows, start from 👉 [the main RackNerd VPS page](https://my.racknerd.com/aff.php?aff=11397&pid=952) and look for the Windows-configured tiers rather than the Linux specials.

**Q: What happens if I exceed my monthly bandwidth allowance?**
A: Your port gets throttled to 10 Mbps until the next billing cycle resets. You don't get cut off entirely, and you don't get hit with overage charges. For most personal and small-business sites this never triggers — you'd need to be pushing multiple gigabytes of transfer every single day to come close.

**Q: Can I run a VPN on a RackNerd VPS?**
A: Yes. KVM virtualization gives you a real kernel, which means you can install OpenVPN, WireGuard, Shadowsocks, or whatever else you want. The 1 GB plan is enough for a personal VPN; the 2 GB is more comfortable if you're routing multiple devices through it.

## Bottom Line

If you've been circling the Black Friday drop and wondering whether to pull the trigger — yes, the deals are real, the prices are sustainable at renewal, and the boxes run reliably enough that you can actually build something on them without constantly firefighting. The only question that matters is which tier matches your workload.

Grab the 2 GB plan if you want a safe default. Grab the 1 GB if you're running a single small site and want the absolute lowest price. Go bigger only if you actually have the workload to justify it — more RAM you never use is just wasted money, even at these prices.

👉 [See all current RackNerd VPS specials and pick your plan](https://my.racknerd.com/aff.php?aff=11397&pid=953)
