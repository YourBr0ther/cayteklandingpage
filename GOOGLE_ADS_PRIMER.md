# Google Ads Primer for Star Citizen Referrals
## Caytek Industries - Referral Campaign Strategy

---

## Table of Contents
1. [Account Setup](#1-account-setup)
2. [Campaign Structure](#2-campaign-structure)
3. [Keyword Strategy](#3-keyword-strategy)
4. [Ad Copy Templates](#4-ad-copy-templates)
5. [Budget & Bidding](#5-budget--bidding)
6. [Targeting Settings](#6-targeting-settings)
7. [Tracking & Optimization](#7-tracking--optimization)
8. [Common Mistakes to Avoid](#8-common-mistakes-to-avoid)
9. [Timeline & Expectations](#9-timeline--expectations)

---

## 1. Account Setup

### Create Your Google Ads Account
1. Go to [ads.google.com](https://ads.google.com)
2. Sign in with your Google account
3. **IMPORTANT**: Look for promotional credits!
   - New accounts often get $100-$500 in free ad credits
   - Check for offers like "Spend $100, get $400 free"
   - These rotate, so Google "Google Ads promo code [current month]"

### Link Google Analytics (Optional but Recommended)
1. Create a Google Analytics 4 property for your landing page
2. Link it to Google Ads for better conversion tracking
3. This lets you see what users do AFTER clicking your ad

### Set Up Conversion Tracking
This is **critical** - you need to know which ads actually get referrals.

**Option A: Track clicks to RSI signup**
```javascript
// Add this to your landing page (already prepped in the code)
document.querySelectorAll('a[href*="referral=STAR-RBFL-52HK"]').forEach(link => {
    link.addEventListener('click', function() {
        gtag('event', 'conversion', {
            'send_to': 'AW-XXXXXXXXX/XXXXXX', // Your conversion ID
            'event_callback': function() {
                window.location = this.href;
            }
        });
    });
});
```

**Option B: Simple click tracking in Google Ads**
- Use "Website" as conversion action
- Track clicks to `robertsspaceindustries.com/enlist`

---

## 2. Campaign Structure

### Recommended Campaign Setup

```
Campaign: Star Citizen Referrals
├── Ad Group 1: Referral Code Seekers (HIGH INTENT)
│   ├── Keywords: "star citizen referral code", "star citizen bonus code"
│   └── Ads: Focus on the 50,000 UEC bonus
│
├── Ad Group 2: New Player Research (MEDIUM INTENT)
│   ├── Keywords: "star citizen new player", "how to start star citizen"
│   └── Ads: Focus on getting started + bonus
│
└── Ad Group 3: Free-to-Play Seekers (LOWER INTENT)
    ├── Keywords: "star citizen free", "star citizen free fly"
    └── Ads: Focus on free fly events + bonus code
```

### Why This Structure?
- **Separate ad groups** = separate budgets and bids
- **High-intent keywords** (people actively looking for codes) get higher bids
- **Lower-intent keywords** get lower bids but cast a wider net

---

## 3. Keyword Strategy

### HIGH INTENT Keywords (Bid Higher - $0.50-$1.50)
These people are ACTIVELY looking for a referral code:

```
star citizen referral code
star citizen referral code 2026
star citizen bonus code
star citizen signup bonus
star citizen new account bonus
star citizen free uec code
star citizen 50000 uec
sc referral code
rsi referral code
```

### MEDIUM INTENT Keywords (Bid Medium - $0.30-$0.80)
These people are researching but not specifically looking for codes:

```
star citizen new player guide
how to start star citizen
star citizen beginner guide
star citizen starter pack
star citizen which ship to buy
star citizen aurora vs mustang
is star citizen worth it 2026
star citizen getting started
```

### LOWER INTENT Keywords (Bid Lower - $0.15-$0.40)
Broader reach, lower conversion rate:

```
star citizen free to play
star citizen free fly
star citizen free trial
space sim games
best space games 2026
games like elite dangerous
```

### NEGATIVE Keywords (Block These!)
Add these to avoid wasting money:

```
-refund
-scam
-dead game
-review
-gameplay
-trailer
-download free
-pirate
-crack
-torrent
```

### Match Types Explained

| Match Type | Symbol | Example | What It Matches |
|------------|--------|---------|-----------------|
| Broad Match | none | star citizen code | Anything related |
| Phrase Match | "quotes" | "star citizen referral" | Must contain phrase |
| Exact Match | [brackets] | [star citizen referral code] | Exact or very close |

**Recommendation**: Start with **Phrase Match** for control, then expand to Broad Match once you know what works.

---

## 4. Ad Copy Templates

### Responsive Search Ads (RSA)
Google now primarily uses RSAs. You provide multiple headlines and descriptions, and Google mixes them.

#### Headlines (30 characters max each, provide 10-15)
```
Star Citizen Referral Code
Get 50,000 Free UEC Bonus
2026 Star Citizen Bonus Code
Free Credits - New Players
Start With 50K UEC Free
Official Referral Program
Claim Your Signup Bonus
New Pilot? Get Free UEC
Star Citizen Starter Bonus
50,000 UEC - Use Code Now
STAR-RBFL-52HK Bonus Code
Free UEC for New Accounts
```

#### Descriptions (90 characters max each, provide 4-5)
```
Create your Star Citizen account with our referral code and receive 50,000 UEC instantly. Start your adventure!

New to Star Citizen? Use referral code STAR-RBFL-52HK when signing up to claim your free 50,000 UEC bonus.

Join the 'verse with a head start! 50,000 free UEC for new pilots. Mining, cargo, salvage guides included.

Get your Star Citizen bonus credits today. Works with all starter packages. Instant 50K UEC on signup.
```

### Ad Extensions (USE THESE - They're Free!)

**Sitelink Extensions:**
```
- "Getting Started Guide" → yoursite.com/#getting-started
- "Ship Recommendations" → yoursite.com/#careers
- "Meet the Founder" → yoursite.com/#meet-cayris
- "Industrial Careers" → yoursite.com/#careers
```

**Callout Extensions:**
```
- 50,000 Free UEC
- Works With All Packages
- Instant Bonus
- Mining & Salvage Guides
- New Player Friendly
```

**Structured Snippet Extension:**
```
Types: Mining, Cargo Hauling, Salvage, Exploration
```

---

## 5. Budget & Bidding

### Starting Budget Recommendation

| Budget Level | Daily Spend | Monthly | Expected Clicks | Expected Referrals* |
|--------------|-------------|---------|-----------------|---------------------|
| Test | $5/day | ~$150 | 50-100 | 5-15 |
| Moderate | $10/day | ~$300 | 100-200 | 10-30 |
| Aggressive | $25/day | ~$750 | 250-500 | 25-75 |

*Conversion rates vary. Expect 5-15% of clickers to actually sign up and buy a package.

### Bidding Strategy

**Phase 1: Learning (Week 1-2)**
- Use **Manual CPC** bidding
- Set max CPC at $0.50-$1.00 for high-intent keywords
- This gives you control while learning

**Phase 2: Optimization (Week 3+)**
- Switch to **Maximize Conversions** once you have 15+ conversions
- Or use **Target CPA** if you know your ideal cost per referral

### Cost Per Referral Math
```
If you spend $25 and get 2 referrals:
- Cost per referral = $12.50
- Each referral gives YOU rewards on the ladder
- Break-even depends on how you value those rewards

Community reports suggest $1-3 per referral is achievable
with well-optimized campaigns.
```

---

## 6. Targeting Settings

### Geographic Targeting
Star Citizen players are worldwide, but focus on:
- **Primary**: United States, Canada, United Kingdom, Australia, Germany
- **Secondary**: Western Europe, New Zealand
- **Exclude**: Countries with very low purchasing power (lower conversion)

### Device Targeting
- **Desktop**: 70% of budget (SC is a PC game)
- **Mobile**: 30% of budget (research happens on mobile)
- **Tablet**: Include but don't prioritize

### Audience Targeting (Layered)
Add these as "Observation" (not "Targeting") to see what works:
- Gaming enthusiasts
- PC gamers
- Space & astronomy interest
- Sci-fi fans
- Technology early adopters

### Schedule (Ad Timing)
- Run ads **all day** initially
- After 2 weeks, check your data for peak conversion times
- Often evenings/weekends perform best for gaming

---

## 7. Tracking & Optimization

### Key Metrics to Watch

| Metric | Target | What It Means |
|--------|--------|---------------|
| CTR (Click-Through Rate) | >3% | Are your ads compelling? |
| CPC (Cost Per Click) | <$1.00 | Are you paying too much? |
| Conversion Rate | >5% | Is your landing page working? |
| Cost Per Conversion | <$5 | Is this profitable? |
| Quality Score | >7/10 | Is Google happy with your ads? |

### Weekly Optimization Checklist
```
□ Check Search Terms report - add negatives for irrelevant searches
□ Pause keywords with 100+ clicks and 0 conversions
□ Increase bids on keywords with good conversion rates
□ Test new ad copy variations
□ Check device performance - adjust bids if needed
□ Review geographic performance
```

### A/B Testing Ads
Always run 2-3 ad variations per ad group:
- Test different headlines
- Test different value propositions (50K UEC vs "Free Credits")
- Test urgency ("Limited Time" vs evergreen)

Let winners run, pause losers after 100+ impressions with poor CTR.

---

## 8. Common Mistakes to Avoid

### ❌ Mistake 1: Too Broad Keywords
**Bad**: `space games` (too generic, expensive, low conversion)
**Good**: `star citizen referral code 2026` (specific, high intent)

### ❌ Mistake 2: No Negative Keywords
You WILL pay for clicks like "star citizen refund" or "star citizen scam" unless you block them.

### ❌ Mistake 3: Sending to Homepage
Always send to a **dedicated landing page** (which you have!) not just any page.

### ❌ Mistake 4: Ignoring Quality Score
Low quality score = higher costs. Improve by:
- Making ad copy match keywords
- Having relevant landing page content
- Improving CTR

### ❌ Mistake 5: Not Tracking Conversions
If you don't track, you can't optimize. Set up conversion tracking BEFORE spending money.

### ❌ Mistake 6: Giving Up Too Soon
Campaigns need 2-4 weeks to optimize. Don't judge results after 3 days.

### ❌ Mistake 7: Trademark Issues
**Don't use "Star Citizen" in your display URL** - could get flagged.
**Do use it in headlines** - generally allowed for informational sites.

---

## 9. Timeline & Expectations

### Week 1: Setup & Learning
- [ ] Create Google Ads account
- [ ] Set up conversion tracking
- [ ] Launch campaign with test budget ($5-10/day)
- [ ] Monitor for disapprovals or issues
- [ ] Add negative keywords as you find bad searches

### Week 2: Initial Optimization
- [ ] Review Search Terms report
- [ ] Pause poor performers
- [ ] Increase bids on winners
- [ ] Test new ad variations

### Week 3-4: Scale What Works
- [ ] Increase budget on winning ad groups
- [ ] Pause or fix losing ad groups
- [ ] Consider switching to automated bidding
- [ ] Expand to new keyword variations

### Month 2+: Maintain & Grow
- [ ] Weekly optimization reviews
- [ ] Test new campaigns (YouTube ads, Display, etc.)
- [ ] Seasonal pushes (Free Fly events, sales)

---

## Quick Start Checklist

```
□ 1. Host your landing page (Netlify/GitHub Pages)
□ 2. Create Google Ads account
□ 3. Look for promo credits
□ 4. Set up conversion tracking
□ 5. Create campaign with structure above
□ 6. Add 10-15 keywords per ad group
□ 7. Write 3 responsive search ads
□ 8. Add all extensions
□ 9. Set daily budget ($5-10 to start)
□ 10. Add negative keywords
□ 11. Launch and monitor daily for first week
□ 12. Optimize weekly thereafter
```

---

## Bonus: Free Fly Event Strategy

Star Citizen has periodic **Free Fly events** where anyone can play free. These are GOLD for referrals.

### When Free Fly is Active:
1. **Increase budget 2-3x** - more searchers
2. **Update ads** - mention "Free Fly Active Now!"
3. **Target broader keywords** - "star citizen free", "try star citizen"
4. **Update landing page banner** (already built in!)

### Finding Free Fly Dates:
- Follow [@RobertsSpaceInd](https://twitter.com/RobertsSpaceInd) on Twitter
- Check r/starcitizen
- Watch for CitizenCon, IAE (Intergalactic Aerospace Expo), etc.

---

## Resources

- [Google Ads Help Center](https://support.google.com/google-ads)
- [Google Keyword Planner](https://ads.google.com/home/tools/keyword-planner/) (free with account)
- [Star Citizen Referral Program FAQ](https://support.robertsspaceindustries.com/hc/en-us/articles/115013102847-Referral-Program-FAQ)
- [SC Free Fly Events Calendar](https://robertsspaceindustries.com/comm-link)

---

## Summary

**The Formula:**
```
High-Intent Keywords + Compelling Ad Copy + Optimized Landing Page = Referrals
```

You already have the landing page. Now it's about:
1. Finding the right people (keywords)
2. Getting them to click (ad copy)
3. Not wasting money (negative keywords + optimization)

**Start small, learn fast, scale what works.**

Good luck, Cayris! May your referral ladder climb be swift. 🚀

---

*Last updated: January 2026*
*Landing page: caytek-landing/index.html*
*Referral code: STAR-RBFL-52HK*
