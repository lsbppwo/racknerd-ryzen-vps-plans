# RackNerd Ryzen VPS: is the $18.88/year plan the one to buy, what the 7950X changes, and what annual billing costs by year two (full plan table)

A 1.2 GB slice on a Ryzen 9 7950X with DDR5 memory and Gen4 NVMe costs **$18.88/year** on RackNerd's Ryzen line. The 512 MB plan on the older 3900X with DDR4 costs **$26.99/year**. Both are Ryzen VPS plans from the same store, and the smaller machine is the more expensive purchase.

For most people reading this, the answer is the $18.88 plan. If 1.2 GB of RAM is too tight for what you're running, the **2.5 GB at $32.98/year** doubles your cores and adds 13 GB of NVMe for $14 more. What follows is the full plan list with prices and terms, what DDR5 and Gen4 actually change in daily use, where the annual math lands once you stop comparing first-year numbers, and the limits that decide whether this is the right host at all.

## Which Ryzen plan most people should buy

> **Most readers:** 1.2 GB on a 7950X, 25 GB Gen4 NVMe, 2,500 GB/month, **$18.88/year**. Enough for a blog, a WireGuard endpoint, a DNS resolver, a monitoring box, or a small Node.js app.
>
> **Need a second core or more headroom:** 2.5 GB, 38 GB NVMe, 4,000 GB/month, **$32.98/year**.
>
> **Skip the 512 MB plan** unless you specifically want the lowest possible monthly cost and nothing else. At $26.99/year it costs more than the 1.2 GB promo and gives you less RAM and less disk.

👉 [Check the current price and datacenter options for the 1.2 GB Ryzen plan](https://bit.ly/RacKnerd)

## All RackNerd Ryzen plans in one table

The Ryzen line runs on two hardware generations. The 7950X nodes carry DDR5 RAM and PCIe Gen4 NVMe. The 3900X nodes carry DDR4 and standard NVMe. Every plan below includes a 1 Gbps port, one dedicated IPv4, full root access, KVM virtualization, and RackNerd's control panel for reboots, reinstalls, console access and rDNS.

The three 7950X prices come from RackNerd's March 2024 promotion announcement. The 3900X annual specials are limited-stock offers tracked by third-party deal pages and sell out regularly. The standard monthly plans are the everyday catalog. Confirm the cart total before you pay, since promo stock changes.

| Plan | CPU / RAM | NVMe | Bandwidth | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 1.2 GB (7950X promo) | 1× 7950X, 1.2 GB DDR5 | 25 GB Gen4 | 2,500 GB/mo | **$18.88/yr** | [Order](https://bit.ly/RacKnerd) |
| 2.5 GB (7950X promo) | 2× 7950X, 2.5 GB DDR5 | 38 GB Gen4 | 4,000 GB/mo | **$32.98/yr** | [Order](https://bit.ly/RacKnerd) |
| 4 GB (7950X promo) | 2× 7950X, 4 GB DDR5 | 65 GB Gen4 | 6,000 GB/mo | **$55.88/yr** | [Order](https://bit.ly/RacKnerd) |
| 1 GB (3900X annual special) | 1× 3900X, 1 GB DDR4 | 24 GB | 2.5 TB/mo | ~$18.18/yr | [Order](https://bit.ly/RacKnerd) |
| 2 GB (3900X annual special) | 2× 3900X, 2 GB DDR4 | 38 GB | 4 TB/mo | ~$31.88/yr | [Order](https://bit.ly/RacKnerd) |
| 3 GB (3900X annual special) | 2× 3900X, 3 GB DDR4 | 55 GB | 5 TB/mo | ~$48.79/yr | [Order](https://bit.ly/RacKnerd) |
| 512 MB (standard, annual) | 1 vCore, 512 MB DDR4 | 10 GB | 500 GB/mo | $26.99/yr | [Order](https://bit.ly/RacKnerd) |
| 1 GB (standard) | 1 vCore | 15 GB | 1 TB/mo | $17.99/mo | [Order](https://bit.ly/RacKnerd) |
| 2 GB (standard) | 2 vCores | 20 GB | 2 TB/mo | $20.59/mo | [Order](https://bit.ly/RacKnerd) |
| 4 GB (standard) | 2 vCores | 30 GB | 3 TB/mo | $24.59/mo | [Order](https://bit.ly/RacKnerd) |
| 6 GB (standard) | 3 vCores | 45 GB | 4 TB/mo | $27.59/mo | [Order](https://bit.ly/RacKnerd) |
| 8 GB (standard) | 3 vCores | 75 GB | 5 TB/mo | $36.59/mo | [Order](https://bit.ly/RacKnerd) |
| 12 GB (standard) | 4 vCores | 90 GB | 6 TB/mo | $55.99/mo | [Order](https://bit.ly/RacKnerd) |

Windows runs on the 3900X platform with Windows Server 2012, 2016 or 2022 and costs meaningfully more per month at similar specs:

| Plan | vCores | NVMe | Bandwidth | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 2 GB Windows | 1 | 35 GB | 2 TB/mo | $27.59/mo | [Order](https://bit.ly/RacKnerd) |
| 4 GB Windows | 2 | 60 GB | 2 TB/mo | $30.59/mo | [Order](https://bit.ly/RacKnerd) |
| 6 GB Windows | 2 | 85 GB | 3 TB/mo | $35.59/mo | [Order](https://bit.ly/RacKnerd) |
| 8 GB Windows | 3 | 110 GB | 5 TB/mo | $44.59/mo | [Order](https://bit.ly/RacKnerd) |
| 12 GB Windows | 4 | 160 GB | 6 TB/mo | $64.59/mo | [Order](https://bit.ly/RacKnerd) |

## 3900X vs 7950X: what the newer chip actually changes

Three things, and only one of them shows up in a spec sheet you'd notice.

**Memory generation.** The 7950X plans ship DDR5, the 3900X plans DDR4. Higher bandwidth helps databases, caching layers and anything holding a working set in RAM.

**Storage interface.** 7950X instances use PCIe Gen4 NVMe; 3900X instances use NVMe without the Gen4 designation. Both beat SATA SSD by a wide margin.

**Single-core speed.** This is the one that matters for a small VPS. RackNerd's own wording is that in many workloads a single Ryzen core outperforms multiple Intel Xeon cores, and that single-threaded performance is where the platform wins. Independent testing backs the clock speed: VPSBenchmarks provisioned a 2 vCore / 4 GB instance on a Ryzen 9 7950X running at 4.5 GHz in California in December 2025.

Read the table with that in mind and the annual specials look strange. The 1 GB 3900X special at ~$18.18/year and the 1.2 GB 7950X promo at $18.88/year are 70 cents apart. The 7950X plan gives you more RAM, more disk, and the newer platform. The 2 GB special (~$31.88) versus the 2.5 GB promo ($32.98) repeats the pattern. The 3900X annual plans are worth buying only when the 7950X promos are out of stock.

## What annual billing saves, and where the 30% code fits

The standard monthly plans are not the cheap way in. Run the year:

- 1 GB standard at $17.99/month is **$215.88 for twelve months**. The 1.2 GB 7950X promo is $18.88 for the same period.
- 2 GB standard at $20.59/month is **$247.08 per year**. The 2.5 GB promo is $32.98.
- 4 GB standard at $24.59/month is **$295.08 per year**. The 4 GB promo is $55.88.

Monthly billing on this line exists for people who need the plan for six weeks and then want out. If you're keeping the box for a year, the promo annual plans cost less than a tenth of the monthly equivalent at comparable RAM.

Third-party deal trackers list a coupon code, `DRWOOKIEE`, as a **30% recurring discount** on VPS plans for both monthly and annual orders, verified active as of August 2026. Two things follow from "recurring." First, it applies to every billing cycle, not just the first one, so the discount repeats on renewal. Second, the savings compound over time: 30% off $18.88/year is about **$13.22/year**, and 30% off a $17.99 monthly plan is about $12.59/month, or roughly $151 over a year. The gap between annual and monthly widens with each renewal instead of resetting.

Whether the code stacks on top of an already-discounted promo plan is something the checkout total will tell you. Enter it in the cart and compare the number before you pay.

👉 [Open an order and test the coupon against the annual price](https://bit.ly/RacKnerd)

## The independent benchmark: Web B, Disk I/O C

VPSBenchmarks ran a full trial on the 2 vCore / 4 GB plan in December 2025, provisioned on a Ryzen 9 7950X at 4.5 GHz in California. The results:

- **Web Performance: grade B.** Good response times for serving web applications.
- **Disk I/O: grade C.** Measured as real-world NVMe throughput inside the VM, not peak drive specification.
- **Provisioning: 1 minute 50 seconds** from order to live SSH access.
- The newer Los Angeles and San Jose nodes were confirmed as 7950X hardware, not 3900X.

The disk grade deserves context because three different numbers float around this product. RackNerd's own copy describes disk I/O "topping 1 GB/s." Vendor comparison tables put Gen4 NVMe peak sequential reads near 7,000 MB/s and random IOPS near 1,000,000. The independent test inside a running VM gave a C. All three can be true at once: you are renting a slice of a RAID-protected array shared with other tenants, and what your instance gets under load is not the drive's peak. Plan for database performance that's good for the price, not for numbers off a hardware spec sheet.

## Limits to check before you pay

**IPv6 exists in exactly one location.** RackNerd provides up to 100 free IPv6 addresses, and only for instances deployed in Los Angeles DC-02. You have to open a support ticket after ordering to request them. Choose New York or Chicago and IPv6 is off the table.

**Upgrades go one direction, one step.** You can move to the next plan up later, and the migration needs about a minute of downtime for a reboot. RackNerd's documentation covers upgrades; nothing published describes downgrading.

**It's unmanaged.** You get root, a control panel, and the hardware. No managed backup service, no DDoS protection tier, and no formal uptime SLA advertised on these plans. Budget accordingly or bring your own snapshot routine.

**The annual commitment is final-ish.** RackNerd's knowledgebase states plainly that the company does not offer refunds or a money-back guarantee. A $18.88 annual plan is a small risk; a $55.88 one is still a commitment, so test with the cheap plan first if you're unsure about the platform.

**Datacenter choice affects latency.** The Ryzen line has historically been available in Los Angeles (DC-02), New York, Chicago, Seattle, Dallas and San Jose, with stock varying by location on any given day. For North American traffic, LA and Dallas are the safer picks.

**Windows costs more for less.** The 4 GB Windows plan at $30.59/month has fewer monthly transfer gigabytes than the 4 GB Linux promo that costs $55.88 for an entire year. Only pay the Windows premium if you actually need a Windows Server license.

## FAQ

**Are the $18.88 / $32.98 / $55.88 promos still available?**
RackNerd's rule, from the original announcement: if the order links are live and working, the promotion is still active. Sold-out configurations are normal on limited-stock deals and come back.

**How fast is setup?**
Instant. The service is activated after payment and usable within minutes; the independent benchmark measured 1 minute 50 seconds to SSH access.

**Can I change the operating system later?**
Yes. The control panel lets you reinstall and switch Linux distributions at any time. If you need something not in the template list, support can mount your own ISO on request.

**Can I upgrade my plan later?**
Yes, to the next plan up, with roughly one minute of downtime for the reboot.

**What payment methods work?**
PayPal, major credit cards, Alipay, Bitcoin, Ethereum, USDT and UnionPay.

**Is the 512 MB plan enough for anything?**
A DNS resolver, a lightweight proxy, uptime monitoring, a personal page. But at $26.99/year it costs $8 more than a 1.2 GB 7950X instance with 2.5× the RAM and 2.5× the disk. Buy it only if the 7950X promo is sold out.

## How to choose, in one pass

- **VPN, proxy, DNS, monitoring, one small site:** 1.2 GB 7950X, $18.88/year.
- **Node.js or Django app, a handful of Docker containers, a Minecraft server for a few players:** 2.5 GB 7950X, $32.98/year.
- **A real database with a working set in RAM, or several containers plus a web server:** 4 GB 7950X, $55.88/year.
- **Windows Server:** the 4 GB Windows plan at $30.59/month, and only if the license is the point.
- **6 GB of RAM or more:** the standard monthly Linux plans, since no annual promo exists at that size.
- **Sustained CPU work (transcoding, inference, long compiles):** none of these. The benchmark's grade-B web score and grade-C disk score describe a budget box that performs well for its price, not a compute node.

Two things to confirm in the cart before paying: whether your workload needs IPv6, in which case Los Angeles DC-02 is the only qualifying location, and what the total looks like after entering `DRWOOKIEE`.

👉 [Pick a Ryzen plan and datacenter on RackNerd's order page](https://bit.ly/RacKnerd)
