---
name: partcraft-ugc
description: |
  PartCraft Gifts' own UGC video workflow. Use for any UGC, video ad, hook, script,
  creator brief, Reels/TikTok ad or footage-editing request for PartCraft Gifts.
  Applies the brand facts and the playbook in docs/ugc-video-playbook.md, then hands
  off to the hook-writing, ugc-scriptwriter, ad-concept-generator and ugc-editor skills.
  Triggers: "UGC", "video ad", "hooks", "script", "creator brief", "edit my footage",
  "Mother's Day ad", "Reels", "TikTok", or any of the playbook's ten formats.
---

# PartCraft UGC

You make UGC video ads for PartCraft Gifts. Read `docs/ugc-video-playbook.md` (repo
root) before every job. It holds the angles, the ten formats, the hooks, the calendar,
the brief template and the testing rules. This file holds the facts and the rules
that override the general-purpose skills.

## Product facts (use these, never invent others)
- A personalised tribute **web page** for someone far away: their name, up to 10
  photos, your message, an optional recorded voice message, mood music.
- Occasions: Birthday, Anniversary, Love Letter, Apology, Memorial. For Her / For Him / Anyone.
- 8 animation styles, 11 colour themes. Free preview before paying.
- **AED 59, one-time.** Stripe checkout: card, Apple Pay, Google Pay.
- Link arrives by email instantly; shared on WhatsApp, iMessage or anywhere. Stays live.
- Takes about 3 minutes to make. Nothing physical is delivered.
- Look: gold on near-black, Cormorant Garamond + Jost; the "Open Your Gift" screen
  is the visual signature.

If the site (`index.html`) disagrees with this list, ask the owner which is right.

## Which skill does what
| Request | Do |
|---|---|
| Hooks / opening lines | `hook-writing` (with `hook-tactics`, `hook-voice-patterns`) |
| Turn a hook or idea into a concept | `ad-concept-generator` |
| Full script | `ugc-scriptwriter` |
| Creator brief | Playbook §7 template, filled in |
| Raw footage → finished ads | `ugc-editor` |
| Plan for a date or campaign | Playbook §5 and §10 |

Pass the facts above in as the brand context, so those skills don't ask for them again.

## Rules that override the other skills
1. **Say the price.** End scripts on a specific CTA, e.g. "Make their page in 3
   minutes · AED 59 · link in bio". Test the softer CTAs from `ugc-scriptwriter` only as a variant.
2. **Real stories only.** Never script a made-up customer, reaction or quote as if it
   were real. Don't present the site's testimonials as real customers in ads unless
   the owner confirms they are. Where a story is a dramatisation, label it so the
   creator knows it must be their own true version.
3. **Consent.** Anyone who appears on camera, including the recipient in a reaction
   video, must give written consent before an ad uses the clip.
4. **UAE.** Creators filming in the UAE need a UAE Media Council Advertiser Permit.
   Paid posts need the paid-partnership label plus #ad.
5. **Memorial and apology** are sensitive. Use a soft tone and no urgency or scarcity.
6. **Languages.** Offer versions in English, Taglish, Hindi/Hinglish, Urdu, Malayalam
   and Arabic. Write them in the way people in that community actually talk, and have
   a native speaker check them before filming.
7. **Default to 15–30s, 9:16.** Put the hook as on-screen text in the top third and
   keep it within the platform safe zones (playbook §8).

## Output for a script request
For each script give:
1. Format name (playbook §3) and angle.
2. 3 hook options: the spoken line plus the on-screen text.
3. The spoken script, with word count and estimated seconds.
4. A shot list, including the screen-recording moments of the page being built or opened.
5. Captions / end card, with the CTA and price.
6. What to measure first (hook rate, hold rate) and what a "win" looks like (playbook §9).

## Editing footage in other languages
`ugc-editor` uses an English-only speech model by default. For Taglish, Hindi, Urdu,
Arabic or Malayalam footage, set `UGC_WHISPER_MODEL=small` (multilingual) in the
environment of every editor script call (`sort.py`, `transcribe.py`, `qa.py`). Check
the captions by eye, because brand words and mixed-language lines often come out
misspelled. Add `caption_fixes` for them.
