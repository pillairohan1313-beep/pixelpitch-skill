# PixelPitch - AI Image Prompt Engineer for Digital Marketers

> A Claude Skill that generates production-grade image prompts for LinkedIn, Instagram, and B2B marketing - in seconds.
>
> PixelPitch turns your marketing brief into a ready-to-paste prompt package for any major image generation model. No more generic prompts. No more trial and error. Just results.
>
> ---
>
> ## What PixelPitch Does
>
> When you install this skill, Claude becomes your personal AI image prompt engineer. Tell it what you need and it produces:
>
> - A production-grade prompt tailored to your chosen image model
> - - A negative prompt (where supported)
>   - - Exact model settings (aspect ratio, guidance, steps, etc.)
>     - - A brand alignment check against your hex colors and visual style
>       - - Two prompt variants (e.g. darker/premium vs. people-forward)
>         - - LinkedIn copy - hook line, CTA, and hashtags
>          
>           - ---
>
> ## Supported Image Generation Models
>
> | Model | Best For |
> |---|---|
> | Flux 1.1 Pro / Pro Ultra | Photorealistic B2B imagery |
> | Midjourney v7 | Editorial and stylized looks |
> | DALL-E 3 | Text-in-image accuracy |
> | Ideogram 2.0+ | Typography-heavy graphics |
> | Stable Diffusion 3.5 | Open-source and local workflows |
> | Adobe Firefly 3 | IP-safe commercial use |
> | Imagen 3 | Complex scenes and faces |
> | Recraft v3 | Vector, icon, and flat design |
>
> ---
>
> ## Supported Platforms
>
> LinkedIn (all formats) - Instagram - Twitter/X - Facebook - Blog/Website - YouTube
>
> All platform specs (exact pixel dimensions, aspect ratios, safe zones) are built into the skill.
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
>             8. Copy the pixelpitch folder to your personal skills directory:
>
>     cp -r pixelpitch ~/.claude/skills/
>
> Or for a specific project:
>
>     cp -r pixelpitch .claude/skills/
>
> ---
>
> ## How to Use
>
> Once installed, just talk to Claude naturally:
>
> - "Create a LinkedIn post image for my B2B SaaS company about pipeline growth"
> - - "Generate a Flux prompt for a personal brand photo on Instagram, dark premium feel"
>   - - "Make a carousel of 5 LinkedIn slides about AI in marketing"
>    
>     - PixelPitch auto-triggers whenever you mention marketing visuals, image prompts, LinkedIn graphics, or social media content.
>    
>     - ### Set Up Your Brand Config (Optional but Recommended)
>    
>     - Paste this at the start of any conversation for consistent on-brand results:
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
> The full brand config template is included in the skill at assets/brand-config-template.md.
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
>       - model-syntax.md               (Syntax for all 8 image models)
>       - platform-specs.md             (Dimensions and safe zones per platform)
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
> If PixelPitch saves you time, give it a star - it helps other marketers find it.
