# Credits System

<p align="center">
  <a href="https://bobina.moe/bobinas/289"><img src="https://6wf3xhuhwdy0ogdt.public.blob.vercel-storage.com/bobinas/289.png" alt="Skydive Bobina" width="130" /></a>
  <a href="https://bobina.moe/bobinas/288"><img src="https://6wf3xhuhwdy0ogdt.public.blob.vercel-storage.com/bobinas/288.png" alt="Syrup Bobina" width="130" /></a>
</p>

Power your interactions with Bobina using the credits economy.

> **Documented defaults (fallbacks):** The live page fetches `/api/credits/public-config` and can override fallback costs, earn rewards, daily cap, price, and holder tiers. Values on this page are the **static fallbacks from the official docs**, which render if the API is empty or fails. Live values on [bobina.moe](https://bobina.moe) may differ.

## 💳 What Are Credits?

Credits are the currency that powers premium features in the Bobina Council ecosystem. Credits are required for conversations with Bobina and premium features like AI market opinions and heatmap generation.

## 📋 Credit Costs

*Documented defaults — may be overridden live via `public-config`.*

| Action | Label | Cost |
| --- | --- | --- |
| `bobina.talk.text` | Text Message | 1 credit |
| `bobina.talk.voice` | Voice Message | 1 credit |
| `aiOpinion` | AI Market Opinion (`/opinion`) | 1 credit |
| `chartLookup` | Chart Lookup (`/chart`) | Free |
| `heatmapGeneration` | Heatmap Generation (`/heatmap`) | 2 credits |

Zero-cost actions display as **Free**.

## 🎁 Earning Credits

Participate in the Bobina Council ecosystem to earn credits through community contributions. Earnings are capped at **10 credits per day** (documented default) to maintain balance.

*Documented default earn rewards — may be overridden live via `public-config`:*

| Action | Label | Reward |
| --- | --- | --- |
| `vote` | Vote (Bobinas, Proposals, Articles) | +1 credit |
| `feedback` | Give Companion Feedback | +2 credits |
| `contribution` | Submit a Bobina | +3 credits |
| `proposal` | Create a Council Proposal | +5 credits |

## 🛒 Purchasing Credits

Buy credits with cryptocurrency to keep chatting with Bobina. Credits are priced at **$0.10 per credit** (documented default) with bulk discounts available.

* Pay with **$BOBINA** tokens or **fiat via Stripe**
* Instant credit delivery after payment confirmation
* Credits expire **1 year after purchase**
* Private purchases (no public notifications)

Access the Credits panel from **Terminal → Settings** ([bobina.moe/?terminal=settings](https://bobina.moe/?terminal=settings)) or the **Companion** tab ([bobina.moe/?terminal=companion](https://bobina.moe/?terminal=companion)).

## 👑 Holder Benefits

$BOBINA token holders receive exclusive benefits based on their holdings. Benefits are tiered by percentage of total supply held.

> **Tier thresholds are not documented as static fallbacks.** Tier rows are loaded from `/api/credits/public-config` (`tiers`, sorted by `minPercent`). Until that returns, the UI shows "Loading holder tiers...". Do not invent holder-tier percentages.

Each loaded tier is rendered as:

* `{emoji} {name} Tier ({minPercent}% Supply)`
* If `unlimited`: **Unlimited messages** (no daily limit)
* Else: `{dailyFreeMessages} free messages per day`
* If `discountPercent > 0`: `{discountPercent}% discount on credit purchases`

Known tier IDs and fallback emojis in the docs bundle:

| Tier ID | Emoji |
| --- | --- |
| `bronze` | 🥉 |
| `silver` | 🥈 |
| `gold` | 🥇 |
| `diamond` | 💎 |
| `bobinachad` | 👑 |

If a tier has no mapped emoji, the API `emoji` field is used.

> Source: official docs Credits System (synced 2026-09-12). Cost/earn/cap/price figures are bundle fallbacks; holder-tier numbers are API-only.

---

---

<p align="center">
  <a href="https://bobina.moe/bobinas/288"><img src="https://6wf3xhuhwdy0ogdt.public.blob.vercel-storage.com/bobinas/288.png" alt="Syrup Bobina" width="100" /></a>
</p>

<p align="center"><sub>Art from the <a href="https://bobina.moe/bobinas">Bobina gallery</a> · Back to the <a href="../../README.md">Docs index</a></sub></p>

