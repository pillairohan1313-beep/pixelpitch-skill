# PixelPitch - AI Image Prompt Engineer for LinkedIn Marketers

> A Claude Skill built specifically for LinkedIn B2B marketing. Generate production-grade image prompts in seconds.
>
> PixelPitch turns your LinkedIn marketing brief into a ready-to-paste prompt package for any major image generation model. No more generic visuals. No more trial and error. Just scroll-stopping LinkedIn content.
>
> ---
>
> ## What PixelPitch Does
>
> When you install this skill, Claude becomes your personal AI image prompt engineer for LinkedIn. Tell it what you need and it produces:
>
> - A production-grade prompt tailored to your chosen image model
> - - A negative prompt (where supported)
>   - - Exact model settings (aspect ratio, dimensions, guidance, steps)
>     - - A brand alignment check against your hex colors and visual style
>       - - Two prompt variants (e.g. darker/premium vs. people-forward)
>         - - LinkedIn post copy - hook line, CTA, and hashtags
>          
>           - ---
>
> ## Supported Image Generation Models
>
> | Model | Best For |
> |---|---|
> | Flux 1.1 Pro / Pro Ultra | Photorealistic LinkedIn imagery |
> | Midjourney v7 | Editorial and stylized looks |
> | DALL-E 3 | Text-in-image accuracy |
> | Ideogram 2.0+ | Typography-heavy graphics |
> | Imagen 3 (Google) | Complex scenes and faces |
> | Stable Diffusion 3.5 | Open-source and local workflows |
> | Adobe Firefly 3 | IP-safe commercial use |
> | Recraft v3 | Vector, icon, and flat design |
>
> ---
>
> ## LinkedIn Formats Supported
>
> | Format | Dimensions | Use Case |
> |---|---|---|
> | Single image post | 1200 x 627 px | Standard feed post |
> | Square post | 1080 x 1080 px | Personal brand, quotes |
> | Portrait post | 1080 x 1350 px | Max feed visibility |
> | Carousel slide | 1080 x 1080 px | Multi-slide content |
> | Article header | 1200 x 644 px | LinkedIn articles |
> | Profile banner | 1584 x 396 px | Personal branding |
>
> All dimensions, safe zones, and composition tips are built into the skill.
>
> ---
>
> ## How to Install
>
> ### On Claude.ai (No coding required)
>
> 1. Download the `pixelpitch.skill` file from this repo
> 2. 2. In Claude.ai, go to Settings > Capabilities and enable Code execution and file creation
>    3. 3. Go to Customize > Skills
>       4. 4. Click Upload and select the `pixelpitch.skill` file
>          5. 5. Done - PixelPitch is now active
>            
>             6. Skills are available on Free, Pro, Max, Team, and Enterprise plans.
>            
>             7. ### On Claude Code
>            
>             8.     cp -r pixelpitch ~/.claude/skills/
>
> ---
>
> ## How to Use
>
> Once installed, just talk to Claude naturally:
>
> - "Create a LinkedIn post image for my B2B SaaS company about pipeline growth"
> - - "Make a LinkedIn carousel about AI in sales, dark premium feel, Flux"
>   - - "Generate a LinkedIn personal brand photo prompt for a founder"
>     - - "Create a LinkedIn article header for my post about GTM strategy"
>      
>       - PixelPitch auto-triggers whenever you mention LinkedIn graphics, B2B visuals, or marketing image prompts.
>      
>       - ### Set Up Your Brand Config (Optional but Recommended)
>      
>       - Paste this at the start of any conversation for consistent on-brand results:
>
>     ### MY BRAND CONFIG
>     Model: Flux 1.1 Pro
>     Platform: LinkedIn
>     Primary color: #1B3A6B
>     Secondary color: #F4A623
>     Style: Clean/Minimal, Corporate/Professional
>     Target audience: B2B SaaS founders and GTM leads
>     People preference: Yes - diverse professionals, 28-45, business casual
>     Always avoid: stock photo cliches, handshakes, red tones
>
> The full brand config template is at pixelpitch/assets/brand-config-template.md.
>
> ---
>
> ## Skill Structure
>
>     pixelpitch/
>     - SKILL.md                        (Core skill instructions)
>     - assets/
>       - brand-config-template.md      (Fillable brand config)
>     - references/
>       - model-syntax.md               (Exact syntax for all 8 image models)
>       - platform-specs.md             (LinkedIn dimensions and safe zones)
>       - style-library.md              (B2B style descriptors and lighting presets)
>
> ---
>
> ## License
>
> MIT - free to use, share, and modify.
>
> ---
>
> Built for LinkedIn marketers, B2B founders, and personal brand builders who need to move fast without sacrificing quality.
>
> If PixelPitch saves you time, give it a star - it helps other marketers find it.
