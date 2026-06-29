# Tará Travel Co. — Brand & Style Analysis

> **SUPERSEDED 2026-06-20** — kept for historical reference only. The Vietnam/Philippines positioning question raised below has been resolved (Vietnam only). Current brand direction lives in `tara-travel-brand-brief.md`.

*Prepared as a senior project manager review. No changes were made to the live site.*
*Pages reviewed: Home, Who we are, Private Trips.*

---

## Project Manager's Notes

I have reviewed the homepage, the "Who we are" page, and the "Private Trips" page. The analysis below captures everything observable from the live site's content and structure. The exact technical design tokens — precise hex colour values, specific font file names, and spacing units — are **not** exposed in the page text and cannot be confirmed by viewing the site externally. These are flagged clearly in the prompt below as items to be read directly from the codebase. I would recommend verifying them within Claude Code before hardwiring them to memory, so the record is exact rather than approximate.

**One observation worth raising:** the brief describes the audience as primarily Filipino tourists visiting Vietnam, while the live "Who we are" page states the company serves journeys "across Vietnam and the Philippines," and the reviews feature US, Australian, and Filipino travellers. The prompt below reflects the live site, but you may wish to reconcile the positioning so the memory record matches your intended direction.

---

## Claude Code Memory Prompt

The block below is written to be pasted directly into Claude Code.

---

```markdown
# TARÁ TRAVEL CO. — BRAND & STYLE MEMORY

## PURPOSE
This document defines the brand, voice, and visual standards for Tará Travel Co.
All content, copy, and design work must adhere to it. When in doubt, match the
existing live site rather than introducing new conventions.

## COMPANY OVERVIEW
- Name: Tará Travel Co. (always written with the accented "á" — "Tará").
- Business: An online travel concierge creating bespoke, tailor-made trips.
- Primary destination: Vietnam. Secondary/expansion destination: the Philippines.
- Base of operations: Da Nang, Vietnam.
- Core audience: Filipino travellers, alongside an international audience
  (reviews feature US, Australian, and Filipino guests).
- Model: Fully tailor-made itineraries plus pre-packaged private day-trip bundles
  (Hanoi, Sapa, Da Nang, Ninh Binh, Ha Long, Hue, Hoi An).
- Tagline in use: "We create tailor-made trips."
- Brand catchphrase: "Tara na!" (Filipino for "Let's go!") — used playfully in
  share copy. This is the linguistic root of the brand name.

## BRAND POSITIONING
- Premium but warm. Refined, not stiff. The promise is effortless luxury:
  "We believe your vacation should feel like a vacation."
- Concierge-led: the brand handles planning, coordination, logistics, dining,
  and spa reservations so the guest only has to enjoy the moment.
- Trust-driven: "Trusted by over 350+ happy travelers." Social proof leans on
  REAL travellers, explicitly NOT influencers ("These aren't influencers").
- Personal, thoughtfully paced, smooth, meaningful, and stress-free.

## TONE OF VOICE
- Warm, personable, and reassuring — speaks directly to the guest as "you."
- Confident and calm; never pushy or salesy.
- Light, friendly Filipino warmth woven in sparingly ("Tara na!").
- Clear and plain-spoken. Short sentences. Benefit-led, not feature-led.
- Emphasises ease, care, and being looked after at every step.
- Calls to action are inviting and low-pressure: "I'm ready to plan", "I'm ready!",
  "Get a free quote".
- AVOID: corporate jargon, hard-sell language, generic stock-travel clichés,
  and over-claiming.

## STRUCTURE & MESSAGING PATTERNS
- The signature process is the "Tailor-made in 4 steps" framework:
  1. Request  2. Review  3. Receive  4. Ready to go!
  Reuse this structure and these step names for consistency.
- Private trips are presented as bundles with a consistent benefit row:
  🕒 Flexible | 🚙 Private Car | 💁🏻‍♀️ Licensed Guide | 💸 Group Perks | 🔁 Free Rebooking
  Keep this icon-and-label pattern consistent across all trip cards.
- Social proof (testimonials with name + country flag emoji) is a core component.

## VISUAL & PHOTOGRAPHY STYLE
- Imagery is authentic, candid, real-traveller photography ("Real moments" series)
  — NOT polished stock imagery. This is a deliberate brand choice; preserve it.
- Galleries mix lifestyle and destination shots.
- Logo: the Tará Travel Co. wordmark/logo (held in /wp-content/uploads/).
  Use the official logo files; do not recreate or alter the mark.

## TYPOGRAPHY — VERIFY IN CODEBASE
- The exact typefaces, weights, and sizes are NOT recorded here because they must
  be read directly from the live theme/CSS rather than assumed.
- ACTION: confirm the heading font, body font, and weight scale from the
  stylesheet before relying on them. Maintain whatever is currently in use for
  consistency; do not substitute fonts.

## COLOUR PALETTE — VERIFY IN CODEBASE
- The exact hex values are NOT recorded here for the same reason.
- ACTION: extract the primary, secondary, accent, background, and text colours
  directly from the theme/CSS and record them here as exact hex codes.
  Do not introduce new colours outside the confirmed palette.

## PLATFORM & TECHNICAL CONTEXT
- Built on WordPress.
- Key pages: Home, Tailor-made Form, Private Trips, Travel Guides, Who we are.
- Contact channels: Facebook Messenger (m.me) and Viber are the primary
  direct-contact methods; surface both consistently.
- Payment methods to display: PayPal, Visa, Mastercard, AMEX, JCB, UnionPay,
  Discover, BPI, GCash. (BPI and GCash signal the Filipino audience — keep them.)
- Social channels: Instagram (@taratravelco), Facebook, Pinterest, TikTok
  (@tara.travel.co).

## CONSISTENCY RULES
1. Always spell the brand "Tará Travel Co." with the accent.
2. Keep the warm, concierge, low-pressure tone in all copy.
3. Reuse established frameworks (4 steps; trip-card benefit row) rather than
   inventing new ones.
4. Use authentic photography, never generic stock.
5. Do not change fonts or colours away from the confirmed site values.
6. Lead with guest benefit and reassurance; close with a friendly, soft CTA.

## OPEN ITEM TO RESOLVE
- Positioning notes "Vietnam and the Philippines" on the live site, while the
  stated audience is Filipino tourists travelling TO Vietnam. Confirm the intended
  primary direction and align all copy accordingly.
```

---

## Closing Recommendations

1. **Fill in the technical tokens from source.** Once in Claude Code, ask it to read the active theme's stylesheet so the typography and colour sections can be completed with exact values. This turns the draft into a definitive reference.
2. **Keep the open item live.** Retain the "Open Item to Resolve" in the memory record until the Vietnam/Philippines positioning is settled, to prevent inconsistent copy later.
