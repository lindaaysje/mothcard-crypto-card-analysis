# Which Span of the Crypto-to-Fiat Bridge Collapses First: A Deep Analysis and Review of MothCard

---

MothCard, crypto virtual card, USDT virtual card, Hong Kong Visa virtual card, UK Visa virtual card, Singapore Visa virtual card, 3DS verification, cross-border payments, Alipay top-up, WeChat Pay, PayPal binding, Netflix subscription, Spotify subscription, AI subscriptions

## 1. The Problem Nobody Talks About at the Exchange

You have USDT. Maybe some BTC too, and a bit of USDC earning yield in a pool somewhere.

But when it's time to actually spend — a month of Netflix, a cloud services bill, dinner in a city you're passing through — those assets are close to useless.

That gap is what people mean by "crypto to fiat." Plenty of people have been building this bridge. The problem is that **the bridge has several spans, and any one of them can collapse** — while most reviews only discuss the most visible span, which is fees.

This piece takes each span apart: why the market looks the way it does, where MothCard sits within it, what its structure can hold up under, and what it can't.

---

## 2. Market Landscape: Four Categories That Aren't Actually Competing

Sorting out the categories is what tells you which things are comparable in the first place.

| Category | Typical players | What they serve | Accept crypto |
|---|---|---|---|
| **① Ad-spend cards** | PSTNET, Mybrocard, Capitalist, Adscard, e.pn | Funding FB / Google / TikTok ad accounts | ✅ |
| **② Chinese-market subscription & overseas-shopping cards** | Coinepay, EasyPay, Dupay, Nobepay | AI subscriptions, streaming, overseas shopping, App Store | ✅ |
| **③ Cross-border B2B payment platforms** | Airwallex, PingPong, Lianlian, XTransfer, Payoneer | Cross-border collection, supplier payouts, corporate cards | ❌ |
| **④ Western B2B spend management & issuing** | Brex, Ramp, Revolut Business, Wallester, Stripe Issuing | Corporate spend control, SaaS management, API issuing | ❌ |

Categories ③ and ④ don't accept crypto at all — they run on wire transfers and local clearing, which isn't the problem a retail user is trying to solve. Comparing Airwallex's fees against a crypto card is comparing the wrong things.

**MothCard operates across ①, ②, and ③. Category ② is the one that gets the most attention.**

### What's happened in category ② over the past few years

Two things have been going on at once.

**First: shutdowns, one after another.** Wildcard, Dupay, Bingo Card, and Fomecard all stopped operating, with large amounts of user balances stuck inside. Threads about this on Chinese technical communities (linux.do, V2EX) are still being updated, and one user's summary has stuck: "no virtual card escapes its upstream."

That's half right. Platforms with a single upstream genuinely can't escape it.
MothCard runs on multiple upstreams, which reflects more solid credentials and offers users more protection.

**Second: demand shifted from "can I spend it" to "can I pay for AI."** Before 2023, the main demand for these cards was streaming and overseas shopping. Now the top use case is AI subscriptions — ChatGPT, Claude, Cursor. And that scenario happens to carry **the highest technical barrier**, because it's gated on the issuing country, not on fees.

Put those two together and category ② comes down to two real tests: **how well it withstands a channel going down**, and **whether it can pay for AI**.

---

## 3. Structural Breakdown: How MothCard Handles Those Two Tests

This section is the core of the article, and the part of MothCard I think is genuinely worth discussing on its own.

### Test one: channel resilience — six cards, three issuing countries, multiple channels

| Card | Issuing country | Card type | Get the Card |
|---|---|---|---|
| Nova | 🇭🇰 Hong Kong | Prepaid | [Apply for a MothCard virtual card](https://mothcard.io/h5/invite?ref=BGPPVHPVDDTW) |
| Aurora | 🇭🇰 Hong Kong | Prepaid | |
| Lumen | 🇭🇰 Hong Kong | Credit | |
| Glow | 🇸🇬 Singapore | Prepaid | |
| Pulsar-2 | 🇸🇬 Singapore | Prepaid | |
| Pulsar-1 | 🇬🇧 UK | Shared | |

These six run on different issuing channels. Which means: **when one channel has a problem, there are still other cards you can open and use.**

That's a structural difference, not a marketing line — go count how many issuing countries comparable platforms list in their card lineup. MothCard's six cards run on different issuing channels, so even if one goes down, the others still work and the platform doesn't grind to a halt or disappear.

### Test two: paying for AI — decided by the issuing country, not the fees

This is the most misunderstood point in the entire category.

Some platforms block by **issuing country**, across the board. Most Hong Kong–issued cards can't pay for AI subscriptions, and that has nothing to do with the balance, the card network, your IP, or your proxy. Ten different Hong Kong cards will give you the same result.

MothCard's tested results (2026-09-22):

| Issuing country | AI subscriptions |
|---|---|
| 🇭🇰 Hong Kong | ❌ Mostly unavailable |
| 🇸🇬 Singapore | ✅ Available |
| 🇬🇧 UK | ✅ Available |

One methodological note to add: **cards from the same country can't be used to infer one another either.** Different issuers and different card ranges can produce different results.

Plenty of platforms in category ② advertise that their "high-weight card ranges can run AI." That phrasing is marketing language — what does the work is the issuing country, not any notion of card-range weight. They genuinely can run AI, and the reason is that the cards aren't issued in Hong Kong.

---

## 4. Fee Structure: Three Legs, Two Charge Points

MothCard has a two-layer structure, wallet plus card, and money travels three legs:

```
Your wallet ──on-chain──> Platform wallet ──transfer──> Card ──spend──> Merchant
              on-chain gas                  top-up fee        transaction fee
```

| Item | Amount | Get the Card |
|---|---|---|
| Card-opening fee | $10–$20 ($5–$15 after the $5 voucher) | [Apply for a MothCard virtual card](https://mothcard.io/h5/invite?ref=BGPPVHPVDDTW) |
| Preload threshold | $10–$100 on some cards — **this is available balance, not a fee** | |
| Top-up fee | 2.0% (Nova / Lumen) or 2.5% (the other four) | |
| Transaction fee | From 1% | |
| Monthly / annual fee | $0 | |

### What this pricing means

**Reasonable for light to moderate users, not for high-volume ones.** On a $20/month subscription, fees run about $0.60. At $3,000 a month in cross-border spending, they're $90–$105.

**And it isn't the most economical option in its category.** There are products on the market with zero fees on the spending side.

It's a clear trade-off: what MothCard buys with this fee level is the multi-issuing-country structure and AI availability — which reflects stronger credentials and infrastructure behind the platform, and better protection for you.

---

## 5. Real Use Cases: What Actually Works in Testing

| Scenario | Recommended cards | Get the Card |
|---|---|---|
| AI subscriptions (ChatGPT / Claude / Cursor) | Glow, Pulsar-2, Pulsar-1 | [Apply for a MothCard virtual card](https://mothcard.io/h5/invite?ref=BGPPVHPVDDTW) |
| Online subscriptions (X / Netflix / YouTube) | All six | |
| App Store / iCloud | Lumen, Glow, Pulsar-2, Pulsar-1 (issuing region must match your Apple ID region) | |
| Flights, hotels, tickets (Trip.com) | Nova, Aurora, Lumen | |
| Overseas e-commerce (AliExpress / Amazon) | Nova, Aurora, Lumen | |
| Cloud services (UCloud / Volcano Engine / AWS / Alibaba Cloud / Tencent Cloud International) | All six | |
| Alipay / WeChat Pay binding | All six | |
| Advertising (FB / Google / TikTok) | All six | |
| Mobile payment wallets | Nova and Aurora support both; Lumen one; Glow supported | |
| 3DS | All six | |

One point that's easy to confuse: a Hong Kong card can buy AI products on AWS but can't subscribe to ChatGPT Plus. The former is acquired by AWS; the latter runs through Stripe and is blocked by issuing country. They're two different paths.
On the KYC question specifically — whether a card that skips it is actually safer — MothCard's blog takes that apart separately: [Is a "no KYC" crypto card actually safe?](https://www.mothcard.io/blog/is-a-no-kyc-crypto-card-actually-safe/).

---

## 6. MothCard's Limitations

### 1. No crypto withdrawals

Funds that come in can be spent and can be transferred within the platform, but **they can't be moved back on-chain**.

This is the hardest constraint in the whole piece. The practical implication: MothCard isn't a place to park funds, so it's best to only load what you plan to spend.

### 2. Not every card covers every scenario

Issuing countries differ, and so do card types. MothCard has six different cards across three issuing regions, which means no single card works everywhere. That said, MothCard does let you open multiple cards — in testing I opened eight in total and could still keep going.

### 3. The physical card isn't out yet

The physical card is said to be launching before long, but for now ATM withdrawals and in-person card payments aren't possible.

### 4. Fees aren't the lowest

There are products with zero fees on the spending side; MothCard isn't one of them. But if you care more about security, stability, and transparency, MothCard is a solid choice.

### 5. Card opening goes through review

Every card goes through a review — you submit and wait for the result, and it can complete in as little as one minute. The review does require documents, but MothCard doesn't block users by region. If Visa or Mastercard applications are difficult where you are, MothCard is worth considering.

---

## 7. Who It's For, and Who It Isn't

**A good fit:**

| Condition | Why | Get the Card |
|---|---|---|
| You need to pay for AI subscriptions | Three cards verified in testing; platforms issuing only in Hong Kong can't do this | [Apply for a MothCard virtual card](https://mothcard.io/h5/invite?ref=BGPPVHPVDDTW) |
| You care about single-channel failure risk | Six cards across three issuing countries; if one goes down there's an alternative | |
| You want to validate cheaply first | $10 to open, $5 out of pocket after the voucher | |
| You've been burned by a platform that shut down | KYC required, with an accountable structure behind it — a different model from the no-KYC group | |

**Not a good fit:**

| Condition | Reason |
|---|---|
| You want to leave no identity information at all | KYC required, no exceptions. That said, users from every region can open a card |
| You need to withdraw crypto at any time | Not possible |
| You need ATM withdrawals or in-person payments right now | The physical card is launching before long, but it isn't available yet |
| You run five figures a month and are fee-sensitive | Go compare zero-fee products |

---

## 8. Conclusion

MothCard isn't the cheapest in its category, and it isn't the most feature-complete. What it solves are two fairly specific problems: **it can pay for AI subscriptions**, and **it's built around security and stability rather than betting everything on a single issuing channel**.

If neither of those is on your list, there are cheaper options with more features out there.

If they are, it's worth spending $5 to verify it yourself — in this category, nobody's account is worth as much as one transaction you've pushed through on your own.

One more thing: MothCard runs active accounts on X and a Telegram group. If you want to look deeper, use my link 👉🏻 [Register for MothCard](https://mothcard.io/h5/invite?ref=BGPPVHPVDDTW), or take a look at [X](https://x.com/MothCard).
