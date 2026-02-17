# Common Gemini Prompt Mistakes

## Overview

These are the patterns that cause poor image generation results. Most come down to one thing: not being specific enough.

---

## Mistake #1: Plain Text Instead of Structured JSON

### The Problem

```
Here is the scene: a bedroom from 1995 with Nintendo posters and a TV showing Mario Bros. The floor has lego bricks scattered around.
```

Gemini can interpret this, but it's guessing on every detail you didn't specify. What angle? What lighting? What aspect ratio? How messy? What colors?

### The Fix

Structure the prompt so every important decision is explicit:

```json
{
  "setting": {
    "type": "1990s suburban boy's bedroom",
    "era_accuracy": "1995, Pacific Northwest"
  },
  "composition": {
    "camera_angle": "low-angle from floor level",
    "shot_type": "wide shot showing entire room",
    "aspect_ratio": "16:9",
    "focal_point": "CRT television with Nintendo"
  },
  "lighting": {
    "primary": "overcast daylight through window",
    "secondary": "warm glow from TV screen",
    "mood": "nostalgic, slightly dim"
  },
  "details": {
    "walls": ["Seattle SuperSonics team poster", "Nintendo promotional poster"],
    "floor": ["scattered LEGO bricks", "high-pile carpet"],
    "furniture": ["corner bed facing TV", "CRT television on wooden stand"],
    "screen_content": "Super Mario Bros gameplay visible"
  },
  "technical": {
    "render_style": "photo-realistic",
    "detail_level": "high"
  }
}
```

---

## Mistake #2: Vague Descriptors

### Examples of Vague Prompts

| Vague | Why It's Bad |
|-------|--------------|
| "good lighting" | Good how? Bright? Soft? Dramatic? |
| "nice background" | Nice is subjective and meaningless |
| "professional photo" | Professional could mean studio, editorial, commercial |
| "attractive model" | Undefined and problematic |
| "modern style" | Modern varies by context |
| "high quality" | Quality of what? Resolution? Composition? |

### How to Fix

Replace every vague word with specifics:

| Vague | Specific |
|-------|----------|
| "good lighting" | "soft diffused daylight from upper left window" |
| "nice background" | "plain white seamless backdrop with subtle shadow" |
| "professional photo" | "studio commercial photography with softbox lighting" |
| "modern style" | "minimalist Scandinavian interior with neutral palette" |
| "high quality" | "photo-realistic, high detail, sharp focus" |

---

## Mistake #3: Missing Aspect Ratio

### The Problem

You don't specify aspect ratio. Gemini picks something — often square or random dimensions that don't fit your use case.

### The Fix

Always include:
```json
"aspect_ratio": "9:16 vertical"
```

Quick reference:
- Instagram Stories/Reels/TikTok: `9:16`
- Instagram Feed: `4:5` or `1:1`
- Website header: `16:9`
- Pinterest: `2:3` or `3:4`

---

## Mistake #4: No Camera Angle Specified

### The Problem

You describe what's in the scene but not how we're viewing it. Gemini defaults to something generic.

### The Fix

Every prompt needs:
```json
"camera_angle": "eye-level, centered on subject"
```

Or:
```json
"composition": {
  "camera_angle": "45-degree from upper right",
  "distance": "medium shot",
  "subject_position": "right third of frame"
}
```

---

## Mistake #5: Expecting AI to Handle Text

### The Problem

You include text requirements like:
- "Show the product name clearly on the packaging"
- "Have a sign that says 'SALE 50% OFF'"
- "The t-shirt should say 'Just Do It'"

Gemini (and all image AI) struggles with text. Results are often garbled, misspelled, or nonsensical.

### The Fix

1. **Avoid text when possible.** Add text in post-production.
2. **If text must appear, keep it minimal** (1–3 words max)
3. **Specify legibility:**
```json
"text_requirements": {
  "text": "SALE",
  "placement": "top of frame",
  "must_be_legible": true,
  "style": "bold sans-serif"
}
```
4. **For mirror selfies with text on clothing:**
```json
"mirror_rules": "ignore mirror physics for text, display forward and readable"
```

---

## Mistake #6: Describing What You DON'T Want

### The Problem

```
"No cluttered background"
"Don't make it too dark"
"Avoid generic stock photo look"
```

AI handles positive instructions better than negative ones. "Don't" prompts often get ignored or misinterpreted.

### The Fix

Describe what you DO want:

| Negative (Bad) | Positive (Good) |
|----------------|-----------------|
| "no cluttered background" | "clean minimal background with single accent prop" |
| "don't make it too dark" | "well-lit with soft shadows, no dark areas" |
| "avoid stock photo look" | "candid lifestyle aesthetic, natural poses, authentic environment" |
| "not too busy" | "minimal composition with clear focal point" |

---

## Mistake #7: Inconsistent JSON Structure

### The Problem

```json
{
  "subject": "woman holding coffee",
  "background": {
    "type": "cafe",
    "details": "exposed brick"
  },
  "lighting": "natural"
}
```

Mixing flat values (`"subject": "woman"`) with nested objects (`"background": {...}`) creates inconsistency. Some details get lost.

### The Fix

Use consistent nesting. If one element has sub-properties, structure all major elements the same way:

```json
{
  "subject": {
    "description": "young woman in late 20s",
    "pose": "seated, holding coffee cup",
    "expression": "relaxed smile"
  },
  "background": {
    "type": "modern cafe interior",
    "elements": ["exposed brick wall", "pendant lights"],
    "atmosphere": "cozy, warm"
  },
  "lighting": {
    "type": "natural daylight",
    "source": "large window to left",
    "quality": "soft, diffused"
  }
}
```

---

## Mistake #8: Not Specifying Product Visibility

### The Problem

For product shots, you describe the scene but don't specify how prominently the product appears.

Results: product gets lost in the scene, partially obscured, or positioned poorly.

### The Fix

Be explicit about product placement:

```json
"product_interaction": {
  "product_name": "Wireless Earbuds Pro",
  "placement": "held in right hand at chest height",
  "visibility": "product clearly visible, logo facing camera",
  "focus": "product in sharp focus"
}
```

Or for lifestyle:
```json
"product": {
  "name": "Green Tea Memory Foam Mattress",
  "placement": "center of frame, bed fully visible",
  "visibility": "hero product, main focal point",
  "details_visible": ["surface texture", "profile height"]
}
```

---

## Mistake #9: Forgetting Platform Context

### The Problem

Creating an image without considering where it will be used. A beautiful 16:9 landscape image is useless for Instagram Stories.

### The Fix

Start with the platform, then work backwards:

```json
"platform_optimization": {
  "primary_platform": "Instagram Stories",
  "aspect_ratio": "9:16",
  "text_safe_zone": "center vertical third",
  "scroll_stopping_elements": "high contrast, clear subject"
}
```

---

## Mistake #10: Overcomplicating the Prompt

### The Problem

Adding every possible detail creates confusion:

```json
{
  "subject": {
    "age": "exactly 27",
    "height": "5'6",
    "eye_color": "hazel with gold flecks",
    "specific_face_shape": "heart-shaped with high cheekbones"
  }
}
```

Gemini can't process all of this. Important details get lost in noise.

### The Fix

Focus on what's visible and important:

1. **Essential details:** Composition, lighting, aspect ratio, key subject features
2. **Important details:** Mood, color palette, photography style
3. **Nice-to-have:** Supporting props, minor details

If a detail won't be visible or doesn't affect the image, leave it out.

---

## Mistake #11: No Iteration Mindset

### The Problem

Expecting perfect results on the first prompt. Getting frustrated and giving up.

### The Fix

Treat it as iterative:

1. **Generate first version** with core parameters
2. **Review what's wrong** — lighting? Angle? Expression? Background?
3. **Adjust specific parameters** — don't rewrite everything
4. **Regenerate and compare**

Keep notes on what adjustments worked. Build a personal reference of effective parameters.

---

## Quick Self-Check Before Submitting Prompt

Before pasting into Gemini, verify:

- [ ] Aspect ratio specified
- [ ] Camera angle specified
- [ ] Lighting type and direction specified
- [ ] Subject/product clearly described
- [ ] Background defined (even if "minimal" or "white seamless")
- [ ] Photography style stated
- [ ] No vague words (good, nice, professional, quality)
- [ ] No negative instructions (no, don't, avoid, without)
- [ ] Text requirements minimal or absent
- [ ] JSON is valid (no trailing commas, proper quotes)
