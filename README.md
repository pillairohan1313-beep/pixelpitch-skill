# PixelPitch - AI Image Prompt Engineer for LinkedIn Marketers

> A Claude Skill built specifically for LinkedIn B2B marketing. Generate production-grade image prompts in seconds.

PixelPitch turns your LinkedIn marketing brief into a ready-to-paste prompt package for any major image generation model. No more generic visuals. No more trial and error. Just scroll-stopping LinkedIn content.

---

## What PixelPitch Does

When you install this skill, Claude becomes your personal AI image prompt engineer for LinkedIn. Tell it what you need and it produces:

- A production-grade prompt tailored to your chosen image model
- A negative prompt (where supported)
- Exact model settings (aspect ratio, dimensions, guidance, steps)
- A brand alignment check against your hex colors and visual style
- Two prompt variants (e.g. darker/premium vs. people-forward)
- LinkedIn post copy - hook line, CTA, and hashtags

---

## Supported Image Generation Models

Last updated: March 2026

| Model | Best For |
|---|---|
| Nano Banana 2 (Google) | Best overall - fast + high quality - RECOMMENDED |
| Nano Banana Pro (Google) | Studio-grade, 4K, maximum quality |
| Nano Banana original (Google) | High-volume, budget workflows |
| FLUX.2 pro (Black Forest Labs) | Best photorealism, multi-reference carousels |
| FLUX.2 klein (Black Forest Labs) | Fastest open source, runs locally free |
| GPT Image 1.5 (OpenAI) | Text-in-image accuracy, replaces DALL-E 3 |
| Midjourney v7 | Editorial and artistic looks |
| Ideogram 2.0+ | Typography-heavy graphics |
| Adobe Firefly Image 5 | IP-safe commercial use |
| Stable Diffusion 3.5 | Open-source and local workflows |
| Recraft v3 | Vector, icon, and flat design |

---

## LinkedIn Formats Supported

| Format | Dimensions | Use Case |
|---|---|---|
| Single image post | 1200 x 627 px | Standard feed post |
| Square post | 1080 x 1080 px | Personal brand, quotes |
| Portrait post | 1080 x 1350 px | Max feed visibility |
| Carousel slide | 1080 x 1080 px | Multi-slide content |
| Article header | 1200 x 644 px | LinkedIn articles |
| Profile banner | 1584 x 396 px | Personal branding |

All dimensions, safe zones, and composition tips are built into the skill.

---

## How to Install

### On Claude.ai (No coding required)

1. Download the pixelpitch.skill file from this repo
2. In Claude.ai, go to Settings > Capabilities and enable Code execution and file creation
3. Go to Customize > Skills
4. Click Upload and select the pixelpitch.skill file
5. Done - PixelPitch is now active

Skills are available on Free, Pro, Max, Team, and Enterprise plans.

### On Claude Code

    cp -r pixelpitch ~/.claude/skills/

---

## How to Use

Once installed, just talk to Claude naturally:

- "Create a LinkedIn post image for my B2B SaaS company about pipeline growth"
- "Make a LinkedIn carousel about AI in sales, dark premium feel, Nano Banana 2"
- "Generate a LinkedIn personal brand photo prompt for a founder using FLUX.2"
- "Create a LinkedIn article header for my post about GTM strategy"

PixelPitch auto-triggers whenever you mention LinkedIn graphics, B2B visuals, or marketing image prompts.

### Set Up Your Brand Config (Optional but Recommended)

Paste this at the start of any conversation for consistent on-brand results:

    ### MY BRAND CONFIG
    Model: Nano Banana 2
    Platform: LinkedIn
    Primary color: #1B3A6B
    Secondary color: #F4A623
    Style: Clean/Minimal, Corporate/Professional
    Target audience: B2B SaaS founders and GTM leads
    People preference: Yes - diverse professionals, 28-45, business casual
    Always avoid: stock photo cliches, handshakes, red tones

The full brand config template is at pixelpitch/assets/brand-config-template.md.

---

## Skill Structure

    pixelpitch/
    - SKILL.md                        (Core skill instructions)
    - assets/
      - brand-config-template.md      (Fillable brand config)
    - references/
      - model-syntax.md               (Syntax for all 11 models, updated March 2026)
      - platform-specs.md             (LinkedIn dimensions and safe zones)
      - style-library.md              (B2B style descriptors and lighting presets)

---

## License

MIT - free to use, share, and modify.

---

Built for LinkedIn marketers, B2B founders, and personal brand builders who need to move fast without sacrificing quality.

If PixelPitch saves you time, give it a star - it helps other marketers find it.
