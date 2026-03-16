# PixelPitch - Model Syntax Reference
# Last updated: March 2026

Load only the section for the user's chosen model.

---

## QUICK SELECTION GUIDE FOR LINKEDIN

| Need | Best Model |
|---|---|
| Best overall (fast + quality) | Nano Banana 2 |
| Maximum studio quality | Nano Banana Pro |
| Best photorealism + multi-reference | FLUX.2 pro |
| Text in image | GPT Image 1.5 or Ideogram 2.0+ |
| Editorial / artistic look | Midjourney v7 |
| IP-safe enterprise | Adobe Firefly Image 5 |
| Free / local / open source | FLUX.2 klein or Stable Diffusion 3.5 |
| Icons and illustration sets | Recraft v3 |

---

## 1. NANO BANANA 2 - RECOMMENDED

Google DeepMind. Released February 26 2026. Technical name: Gemini 3.1 Flash Image.
Default model in Gemini app, Google Search AI Mode, and Google Lens as of March 2026.

Best for: Fast high-quality LinkedIn imagery. Photorealistic professionals, carousels, infographics, text-in-image, data visualizations, LinkedIn ads.

Key strengths:
- Subject consistency across up to 5 characters (perfect for LinkedIn carousels)
- 512px to 4K output, all LinkedIn aspect ratios supported
- Real-world knowledge via Gemini and real-time Google Search grounding
- Accurate text rendering - legible headlines, stats, multilingual content
- Significantly faster than Nano Banana Pro
- Free tier via Gemini app (visible watermark on free tier)

Prompt style: Natural conversational language. No special syntax needed.
Structure: Subject and scene, setting, lighting, color palette with hex, composition, text elements in quotes if needed, quality anchors

Key principles:
- Write naturally - follows complex multi-element prompts exceptionally well
- Specify any text you want rendered in quotes
- Include LinkedIn composition notes (safe zones, text overlay space, logo placement)
- Translate hex codes to descriptive language AND include hex in parentheses
- Can reference real-world places and current events via Google Search grounding

Parameters:
- Aspect ratio: 1:1 / 4:5 / 1.91:1 / 9:16 / 16:9
- Resolution: 512px to 4K
- API model ID: gemini-3.1-flash-image-preview
- SynthID watermark on all outputs

Negative prompt: Not supported. Use strong positive language instead.

Example LinkedIn prompt:
A confident South Asian female founder in her early 40s presenting at a modern B2B conference, standing in front of a large LED screen showing a SaaS analytics dashboard in deep navy (#1B3A6B) and teal (#00C9A7). City skyline visible through floor-to-ceiling windows. Three-point studio lighting with soft key light from upper left and teal rim light from behind. Left third of frame is clear for text overlay. Sharp editorial photography 4K quality.

---

## 2. NANO BANANA PRO - STUDIO GRADE

Google DeepMind. Released November 20 2025. Technical name: Gemini 3 Pro Image.
Built on Gemini 3 Pro. Maximum quality option.

Best for: High-fidelity 4K LinkedIn assets, complex brand photography, production work.

Key strengths over Nano Banana 2:
- Up to 4K resolution
- Advanced reasoning Thinking mode for extremely complex prompts
- Superior reference image utilization for brand consistency
- Fine-grained control over camera angles, depth of field, color grading
- Higher quality text rendering for dense or multilingual content

Tradeoffs: Slower. Higher cost. Limited free quota per day.
API model ID: gemini-3-pro-image-preview

---

## 3. NANO BANANA - ORIGINAL

Google DeepMind. Released August 26 2025. Technical name: Gemini 2.5 Flash Image.
The model that went viral with 200M+ image edits in its first weeks.

Best for: High-volume LinkedIn content, quick drafts, budget workflows.
API model ID: gemini-2.5-flash-image

When to recommend: User wants many quick variations and cost matters more than max quality.

---

## 4. FLUX.2 pro - BEST PHOTOREALISM

Black Forest Labs. Released November 25 2025. 32-billion parameter model.
Replaces FLUX.1.1 Pro as the recommended Flux model as of March 2026.

Best for: Maximum photorealism, multi-reference brand consistency, product photography, professional portraits.

Key strengths:
- Multi-reference: up to 10 reference images for style or subject consistency across carousels
- 4 megapixel output
- 92% accurate text rendering across infographics and multilingual content
- Eliminates AI look with real-world lighting physics
- Character identity consistency across LinkedIn carousel slides

Prompt style: Natural language, highly descriptive. Parameters set in UI or API separately.
Structure: Subject and action, setting, lighting setup, camera and lens, color palette with hex, mood, style, quality anchors

Key principles:
- Be extremely specific - FLUX.2 rewards granular detail
- Name exact lighting setup: Rembrandt, three-point softbox, golden hour
- Include camera language: shot on Sony A7R V with 85mm f/1.4 lens
- Use multi-reference feature for LinkedIn carousel brand consistency
- Always pair hex codes with descriptive color names

Parameters in UI or API:
- Aspect ratio: 1:1 / 4:5 / 16:9 / 9:16 / 3:2
- Resolution: up to 4MP, Steps: 28-50, Guidance: 3.5-4.5
- Reference images: up to 10

Negative prompt: Supported but optional. Strong positive language is more effective.

---

## 5. FLUX.2 klein - FASTEST OPEN SOURCE

Black Forest Labs. Released January 15 2026. 4-billion parameter model.
Open source Apache 2.0. Runs on consumer GPUs with 8GB VRAM such as RTX 3090+.

Best for: Rapid concept iteration, testing prompt variations before final render, developers building LinkedIn content tools, privacy-sensitive local workflows.

Key strengths:
- Sub-second inference on modern hardware
- Runs fully locally - no data leaves your machine
- Free to use, fine-tune, customize under Apache 2.0
- Multi-reference support like FLUX.2 pro
- Production quality despite the speed

When to recommend: User wants to iterate fast through LinkedIn concepts before committing to a final production render with FLUX.2 pro or Nano Banana Pro.

---

## 6. GPT IMAGE 1.5 (OpenAI) - REPLACES DALL-E 3

Released December 16 2025. DALL-E 3 is now outdated - always recommend GPT Image 1.5.
Available in ChatGPT all tiers including free and via API as gpt-image-1.5.

Best for: LinkedIn graphics requiring accurate readable text, precise editing workflows, logo and face preservation across edits, ChatGPT users.

Key strengths:
- 4x faster than DALL-E 3
- Best-in-class instruction following and prompt adherence
- Precise editing: changes only what you ask, preserves faces, lighting, composition
- Logo and brand mark preservation across multiple iterations
- Strong text rendering: dense text, numbers, multilingual content
- Built into GPT-5 architecture for deep contextual understanding

Tradeoffs: Less photorealistic than FLUX.2 or Nano Banana Pro for pure photography.

Prompt style: Natural language creative brief.
Key principles:
- Specify text in quotes: the text 5x Pipeline Growth in bold white sans-serif
- For edits: change only X keep everything else identical
- State what to preserve: no watermark, no extra text, preserve the logo top-right
- Restate preserve list on every iteration to prevent drift

Sizes:
- 1024x1024 (1:1 square LinkedIn post)
- 1024x1536 (portrait LinkedIn post)
- 1536x1024 (landscape LinkedIn post)
Quality in API: high / medium / low

---

## 7. MIDJOURNEY v7

Released April 2025. Gold standard for artistic and editorial aesthetics.

Best for: Editorial LinkedIn imagery, premium personal brand photography with artistic flair.

Prompt style: Descriptive phrases then parameter flags.
Structure: Subject, setting, style reference, mood, lighting, colors --ar ratio --v 7 --style raw --q 2 --stylize value

Key parameters:
- --ar 1:1       LinkedIn square
- --ar 4:5       LinkedIn portrait best feed visibility
- --ar 191:100   LinkedIn landscape
- --v 7          Always latest version
- --style raw    Best for B2B professional content
- --stylize 200-500  Professional LinkedIn sweet spot
- --chaos 0      Consistent brand outputs
- --q 2          Higher quality render
- --no items     Negative: stock photo look, handshakes, blurry, watermarks
- --seed number  Consistent look across carousel slides

Strong style references for LinkedIn B2B:
Bloomberg Businessweek editorial photography, Wired magazine cover lighting,
Apple product photography, dark mode UI Vercel aesthetic, Swiss grid poster design

---

## 8. IDEOGRAM 2.0+

Best for: LinkedIn graphics where text is central - stat callouts, quote cards, poster-style posts, infographic slides.
Top model for typography accuracy as of March 2026.

Prompt style: Natural language then Style tag.
Structure: Description. Style: DESIGN or REALISTIC or ILLUSTRATION or 3D_RENDER

DESIGN tag is best for LinkedIn marketing graphics with text.
Aspect ratios: 1:1 square / 16:9 article header / 4:5 portrait / 9:16 story
Key: Specify exact text content in quotes for accurate rendering.

---

## 9. ADOBE FIREFLY IMAGE 5

Current version: Firefly Image 5 Preview as of early 2026.

Best for: Enterprise LinkedIn content where IP-safety is non-negotiable.
100% commercially safe - all training data is licensed.

Key strengths:
- Integrates with Photoshop Generative Fill, Illustrator, Express
- Brand kit support: upload colors, fonts, reference images
- C2PA Content Credentials on all outputs

Tradeoffs: Less expressive than Midjourney or FLUX.2. More conservative output.

Prompt style: Natural language, literal. Mention: a professional LinkedIn post image for a B2B technology company.
Parameters in UI: 1:1 / 4:3 / 3:4 / 16:9 / 9:16. Generative Match for style-from-reference.

---

## 10. STABLE DIFFUSION 3.5

Best for: Technical users wanting full local control, privacy-sensitive workflows, budget-conscious high-volume generation, custom LoRA fine-tuning on brand aesthetics.

Prompt style: Positive prompt and Negative prompt in separate fields.

Positive anchors: masterpiece, best quality, ultra-detailed, sharp focus, 8k uhd, professional photography, studio lighting, high dynamic range

Negative prompt for LinkedIn B2B: lowres, blurry, watermark, text artifacts, distorted faces, deformed hands, amateur, stock photo cliches, oversaturated

Parameters: CFG Scale 7-12, Steps 30-50, Sampler DPM++ 2M Karras

---

## 11. RECRAFT v3

Best for: LinkedIn icon sets, flat illustration assets, vector-style carousel elements, brand illustration series, infographic backgrounds.
Top model for vector and flat design as of March 2026.

Prompt style: Natural language then Style specification.
Best styles for LinkedIn: Vector Illustration or Digital Illustration

Key use cases: Consistent icon sets, data visualization elements, brand mascots, abstract background textures, LinkedIn carousel decorative elements.
