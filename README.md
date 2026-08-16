# PCX 50% Convertible Deposit Bonus

Landing page for the PCX 50% Convertible Deposit Bonus campaign.

## Contents

```
landing-page/
  landing-page-safe-version.html    single-file page (CSS, JS and images inlined)
```

Open the file directly in a browser, or serve the folder over HTTP. No build step
and no external dependencies except Google Fonts (Inter + IBM Plex Mono).

Live page: https://www.pcxtrader.com/bonus50

## What "safe version" means

The copy in this file is the compliance-reviewed wording. It replaced the earlier
marketing-led copy: claims are stated conditionally, the drawdown rule is framed
around capital preservation, and the bonus is described as convertible credit
rather than money the client already owns.

## Page structure

| Section | Purpose |
| --- | --- |
| Hero | Offer statement, CTA scrolls to "how it works" |
| Pain | Two failure modes of conventional deposit bonuses |
| Credit model | Three differentiators, with a text CTA |
| Why / take | Split card: why the program exists, why it is worth taking |
| Math | Worked example of credit converting into balance |
| How it works | Three steps, plus the closing CTA |
| FAQ | Four collapsible categories |
| Terms dialog | Full Bonus Terms, opened from the drawdown section |

## Call to action map

| Position | Label | Target |
| --- | --- | --- |
| Hero | See how it works | `#how` (in-page) |
| Credit model | Get Credit That Converts | registration |
| Why / take card | Take What's Mine | registration |
| Closing | Open Account & Activate Credit | registration |
| Terms dialog | Open account | registration |

In this file the registration links point to `https://pcxtrader.com/bonus50`.
On the live site they resolve to `/go/register`.

## Pending

- **Floating WhatsApp button.** Requested by marketing, not implemented here. It
  needs a live support number and will be added together with the developer, on
  the production site rather than in this file.
- **Meta Ads tracker is not installed.** No Meta pixel or conversion API is
  present on this page. It must be added before any paid campaign starts,
  otherwise none of the traffic from ads is measurable.
- **No per-CTA tracking parameters.** All CTAs point at the same URL, so there is
  no way to tell which section produces registrations. Suggested fix is a source
  parameter per position, for example `?src=bonus50&pos=credit-model`.
- **Campaign dates in the Terms are provisional** (15 August 2026 to 15 November
  2026) and need to be confirmed before launch.
- **Terms clause 2.2 still requires opt-in before the first deposit**, while the
  page and the KOL posters describe deposit first, then activation by email.
  One of the two has to change.
- **Images are inlined as base64**, which is why the file is about 1.8 MB. Split
  them into separate assets before serving this at scale.
