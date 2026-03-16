# PixelPitch - Model Syntax Reference

Exact prompt structure, flags, and parameters for each supported image generation model.
Load the section for the user's chosen model only.

---

## 1. FLUX 1.1 PRO / FLUX PRO ULTRA

Best for: Photorealistic images, commercial photography aesthetics, detailed B2B scenes.

Prompt style: Natural language, highly descriptive. Parameters set via UI separately.

Structure: [Subject + action], [setting], [lighting], [camera/lens], [color palette], [mood], [style], [quality anchors]

Key principles:
- Be extremely specific - Flux rewards granular detail
- Name lighting setup explicitly (Rembrandt, softbox, golden hour)
- Include camera language: "shot on Sony A7R V with 85mm f/1.4 lens"
- Color: translate hex codes into descriptive language AND include hex in parentheses
- Flux 1.1 Pro handles text in images reasonably well

Parameters (set in UI, not in prompt):
- Aspect ratio: 1:1 / 4:5 / 16:9 / 9:16 / 3:2
- Steps: 28-50
- Guidance: 3.5-4.5
- Negative prompt: Not natively supported - use strong positive language instead

Example prompt:
A confident South Asian woman in her early 40s presenting at a sleek B2B product demo, standing in front of a large curved monitor displaying a SaaS dashboard, modern open-plan office with floor-to-ceiling windows, afternoon natural light from the left, shot on Sony A7R V with 50mm lens at f/2.0, deep navy (#1B3A6B) accent tones, professional editorial photography aesthetic, sharp focus on subject, ultra-detailed, 8K, commercial photography quality

---

## 2. MIDJOURNEY V7

Best for: Artistic/stylized outputs, editorial looks, mood-heavy imagery.

Prompt style: Descriptive phrases separated by commas, followed by -- flags.

Structure: [Subject], [setting], [style reference], [mood], [lighting], [color palette], --ar [ratio] --v 7 --style [raw/default] --q [1/2] --stylize [0-1000]

Key parameters:
- --ar 1:1 = Square (LinkedIn square post)
- --ar 1.91:1 = LinkedIn landscape (1200x627)
- --ar 4:5 = Instagram portrait / LinkedIn portrait
- --ar 9:16 = Story / Vertical
- --v 7 = Always use latest version
- --style raw = Less opinionated, closer to your prompt
- --stylize 100-500 = Sweet spot for B2B
- --chaos 0 = Consistent results
- --q 2 = Higher quality
- --no [items] = Negative prompt (e.g., --no text, watermarks, blurry)

Example:
confident tech founder presenting on stage, minimalist conference background, dramatic rim lighting in deep navy and electric teal, sharp editorial portrait, left third negative space for text, Bloomberg Businessweek cover photography --ar 1.91:1 --v 7 --style raw --stylize 350 --q 2 --no stock photo, cheesy smile, handshake

---

## 3. DALL-E 3

Best for: Accurate text rendering in images, quick iterations, clean commercial outputs.

Prompt style: Full natural language sentences. Write it like briefing a photographer.

Key principles:
- Best model for embedding readable text directly in images
- Specify text content in quotes: with the text "5x Pipeline Growth" in bold white type
- Follows detailed compositional instructions very well
- No negative prompt support - use positive framing

Parameters (via API):
- size: "1024x1024" or "1792x1024" or "1024x1792"
- quality: always use "hd" for marketing
- style: "natural" for photo-realism, "vivid" for punchy graphics

Example:
A professional marketing dashboard graphic in deep navy blue (#1B3A6B) and warm amber (#F4A623). The image shows a clean data visualization with an upward trending line chart. Display the text "3.2x Revenue Growth" in large bold white sans-serif typography centered in the upper half. The lower third features abstract geometric shapes in teal (#00C9A7) against the navy background. Clean, corporate, modern B2B SaaS aesthetic.

---

## 4. IDEOGRAM 2.0+

Best for: Typography integration, poster/infographic style, social media graphics with text.

Prompt style: Natural language + Style tag.

Structure: [Description]. Style: [DESIGN / ILLUSTRATION / REALISTIC / 3D_RENDER]

Style tags:
- DESIGN = Best for marketing graphics, posters, social media with text
- REALISTIC = Photographic look
- ILLUSTRATION = Illustrated / editorial art
- 3D_RENDER = 3D objects and scenes

Key principles:
- Best model for readable text - always specify exact text in quotes
- Excellent at clean minimal design
- Both hex and descriptive color language work well

Example:
A bold LinkedIn post graphic for a B2B marketing agency. Deep navy background (#1B3A6B). Centered text in white reads "Stop Guessing. Start Growing." in clean modern sans-serif. Below: a teal (#00C9A7) underline accent. Bottom left: small amber (#F4A623) geometric triangle. Minimalist, professional, high-contrast. No people. Style: DESIGN

---

## 5. STABLE DIFFUSION 3.5

Best for: Open-source flexibility, running locally, full control.

Prompt style: Positive prompt + Negative prompt (separate fields).

Common quality anchors (positive):
masterpiece, best quality, ultra-detailed, sharp focus, 8k uhd, professional photography, award-winning, studio lighting, high dynamic range

Common negative prompts for B2B:
lowres, bad anatomy, blurry, watermark, text artifacts, distorted faces, deformed hands, ugly, amateur, stock photo cliches, oversaturated, noise, low quality

Key parameters:
- CFG Scale: 7-12 (7.5 is a good B2B default)
- Steps: 30-50
- Sampler: DPM++ 2M Karras (sharp) or Euler a (creative)
- Size: 1024x1024, 1216x832 (landscape), 832x1216 (portrait)

---

## 6. ADOBE FIREFLY 3

Best for: Commercially safe images (all content licensed), brand kit integration, Adobe CC workflows.

Key advantages:
- IP-safe for commercial use
- Integrates with Adobe Express, Photoshop generative fill
- Supports brand kits directly in UI
- Content credentials for AI image authenticity

Prompt tips:
- Be conservative and literal
- State use case explicitly: "a professional LinkedIn post image for a B2B technology company"
- Mention "commercial use, clean, safe for business"

Parameters (in UI):
- Aspect ratio: 1:1 / 4:3 / 3:4 / 16:9 / 9:16
- Content type: Photo / Art / Graphic
- Color and tone: Cool / Warm / Muted / Vibrant

---

## 7. IMAGEN 3 (Google)

Best for: Photorealism, complex scenes, accurate hand/face rendering, Google ecosystem.

Key strengths:
- Best-in-class for realistic human hands and faces
- Excellent at following complex scene compositions
- Strong understanding of spatial relationships
- Available via Google Vertex AI, Gemini Advanced

Prompt tips:
- Can handle very long prompts (400+ words) without degradation
- Specify exact spatial relationships
- Include "photojournalistic", "editorial", or "commercial photography" for professional outputs

---

## 8. RECRAFT V3

Best for: Vector-style graphics, icons, UI elements, consistent brand illustration sets, flat design.

Style options:
- Realistic Image = Photographic
- Digital Illustration = Editorial art
- Vector Illustration = Flat design, icons, infographic elements
- Icon = Simple icon/pictogram

Key strengths:
- Best for icon sets and UI element graphics
- Excellent at brand-consistent flat illustration
- Great for infographic-style images
- Supports brand color palette input directly in UI

---

## 9. CUSTOM / UNLISTED MODEL

If the user is using a model not listed above, ask:
1. Does it use natural language prompts or special syntax?
2. Does it support negative prompts?
3. What aspect ratios / sizes does it support?
4. Are there any special flags or parameters?

Then apply the universal PixelPitch layered approach (Subject > Style > Color > Lighting > Composition > Quality) and adapt the syntax to whatever the model expects. The quality of the content layer matters more than model-specific syntax.
