# Pre-launch Checklist

Complete every item on this list **before** executing any GTM channel activity. These are the non-negotiable foundations. Without them, traffic and demand you generate will leak out.

---

## 1. Analytics Setup

You cannot optimize what you cannot measure.

- [ ] **Google Analytics 4** installed on all pages ([ga.google.com](https://analytics.google.com))
- [ ] **Mixpanel or PostHog** for product event tracking (signups, activations, feature usage)
- [ ] Core events defined and firing: `page_view`, `signup`, `activation`, `conversion`
- [ ] UTM parameter strategy documented (so every campaign is trackable)
- [ ] Dashboard or report created for weekly GTM review

**Recommended stack:** GA4 (top-of-funnel) + PostHog (in-product) — both have generous free tiers.

---

## 2. Email Automation

Email is your highest-ROI owned channel. Set it up before you have a single user.

- [ ] Email platform configured: **Mailchimp / ConvertKit / Loops / Resend**
- [ ] Welcome email live and tested (fires within 60 seconds of signup)
- [ ] Onboarding sequence written and scheduled (at least 3 emails in first 7 days)
- [ ] Unsubscribe / GDPR compliance confirmed
- [ ] SPF, DKIM, DMARC records set on your domain (check with [mail-tester.com](https://www.mail-tester.com))
- [ ] Sender reputation score > 9/10

---

## 3. On-page SEO

Every page you publish should be found. This is table stakes.

- [ ] Title tag on every page (50–60 chars, primary keyword included)
- [ ] Meta description on every page (150–160 chars, compelling CTA)
- [ ] H1 tag present and matches primary keyword intent
- [ ] Open Graph tags set (for social sharing previews)
- [ ] Canonical tags configured
- [ ] XML sitemap generated and submitted to Google Search Console
- [ ] robots.txt configured correctly (not blocking indexing)
- [ ] Page load speed < 3 seconds (test at [PageSpeed Insights](https://pagespeed.web.dev))
- [ ] Mobile-responsive layout confirmed

---

## 4. Social Media Profiles

Claim your handles before someone else does. Even if you won't be active on every platform immediately.

- [ ] **Twitter/X** — handle claimed, bio written, link to landing page
- [ ] **LinkedIn Company Page** — created, logo uploaded, description complete
- [ ] **Instagram** — if relevant to your audience
- [ ] **YouTube** — channel created if video content is part of your strategy
- [ ] **Product Hunt** — profile created for upcoming launch
- [ ] **GitHub** — organization set up if developer-facing product
- [ ] **TikTok** — if B2C / consumer product targeting under-35 audience

---

## 5. ESPN Stack (Email + SMS + Push Notifications)

The ESPN stack lets you talk to your users across three channels and dramatically increases activation and retention rates.

### Email (E)
- [ ] Platform: **Mailchimp / Loops / ConvertKit** (see item 2 above)
- [ ] Signup form embedded on landing page
- [ ] Double opt-in configured

### SMS (S)
- [ ] **Twilio** account created ([twilio.com](https://www.twilio.com))
- [ ] Phone number purchased (or toll-free number registered in US)
- [ ] SMS opt-in form built with TCPA-compliant language
- [ ] First SMS message drafted (keep it < 160 chars, include opt-out instructions)
- [ ] Test message sent and received successfully

### Push Notifications (P)
- [ ] **Notifyfy.com** (or OneSignal / Firebase) configured
- [ ] Web push prompt implemented on landing page and app
- [ ] First push notification drafted for launch day
- [ ] Opt-in rate baseline noted (industry average ~5–10% of visitors)

---

## 6. Landing Page

Your landing page is your first sales rep. It should work even when you sleep.

- [ ] **Hero section** — clear headline (what it is + who it's for + the outcome)
- [ ] **Sub-headline** — the differentiator in one sentence
- [ ] **Primary CTA** — above the fold, high contrast, action-oriented text
- [ ] **Social proof** — at least one testimonial, logo, or data point
- [ ] **Features section** — benefit-led, not feature-led copy
- [ ] **FAQ section** — address the top 3 objections
- [ ] **Second CTA** — at the bottom for users who scrolled
- [ ] **Analytics** — GA4 + conversion event firing on CTA click
- [ ] **A/B test** — at least 2 headline variants queued for Day 1 (use Hotjar, Optimizely, or VWO)
- [ ] **Page speed** — Lighthouse score > 85 on mobile

---

## 7. Product Readiness

No GTM plan survives contact with a broken product.

- [ ] Core user journey tested end-to-end (signup → activation → key action → success state)
- [ ] Error states and edge cases handled gracefully (no blank screens or cryptic errors)
- [ ] Mobile experience tested on at least 2 device sizes
- [ ] Cross-browser tested (Chrome, Safari, Firefox at minimum)
- [ ] Performance tested under realistic load (use [k6](https://k6.io) or [Loader.io](https://loader.io))
- [ ] Uptime monitoring set up ([Better Uptime](https://betterstack.com) or [UptimeRobot](https://uptimerobot.com))
- [ ] Error monitoring active ([Sentry](https://sentry.io) recommended)
- [ ] Customer support channel ready (email alias, Intercom, or Crisp chat)

---

## Pre-launch Checklist Summary

Print this out and tick it off before you run a single ad, send a single DM, or post a single tweet:

```
ANALYTICS
□ GA4 installed and events firing
□ Mixpanel / PostHog configured
□ UTM strategy documented

EMAIL AUTOMATION
□ Platform configured
□ Welcome email live
□ Onboarding sequence active
□ Domain authentication (SPF/DKIM/DMARC) set

SEO
□ Title + meta on every page
□ Sitemap submitted to GSC
□ Page speed < 3s

SOCIAL PROFILES
□ All relevant handles claimed
□ Bios written, profile pics uploaded

ESPN STACK
□ Email opt-in live
□ Twilio SMS configured
□ Push notifications (Notifyfy) set up

LANDING PAGE
□ Clear hero + CTA above fold
□ Social proof present
□ Analytics firing on conversion events

PRODUCT
□ End-to-end journey works
□ Mobile tested
□ Error monitoring (Sentry) active
□ Uptime monitoring active
```

> **Reminder from GTM Canvas:** This checklist represents your Day 0 infrastructure. Without it, every channel you activate will underperform. Complete it before sprint 1 begins.
