# Gemini Prompt Parameters — Complete Guide

## Overview

This guide explains every parameter used in structured Gemini prompts. Use it to understand what each field controls and how to fill it effectively.

---

## Core Photography Parameters

### aspect_ratio

Controls the shape of the output image. Choose based on where the image will be used.

| Value | Use Case | Platform |
|-------|----------|----------|
| `1:1` | Square posts, product thumbnails, profile images | Instagram feed, LinkedIn |
| `4:5` | Vertical feed posts, product features | Instagram feed, Facebook |
| `9:16` | Full-screen vertical, stories, short-form video thumbnails | Instagram Stories, Reels, TikTok |
| `16:9` | Landscape, headers, video thumbnails | Website banners, YouTube, presentations |
| `3:4` | Portrait orientation, pins | Pinterest, editorial |

**Tip:** Always specify. If you don't, Gemini chooses — often not what you want.

---

### camera_angle

Determines viewer perspective and psychological impact.

| Value | Effect | Best For |
|-------|--------|----------|
| `eye-level` | Neutral, relatable, natural | Portraits, lifestyle, approachable products |
| `overhead` / `bird's eye` / `flat lay` | Shows arrangement, eliminates depth | Products, food, accessories, organized layouts |
| `45-degree` | Shows dimension, most versatile | Product photography, hero shots |
| `low angle` | Powerful, heroic, aspirational | Premium products, dramatic effect |
| `three-quarter` | Shows depth and multiple surfaces | Furniture, electronics, dimensional products |
| `close-up` / `macro` | Texture and detail focus | Material quality, craftsmanship |
| `wide shot` | Context and environment | Lifestyle, room settings |

---

### shot_type

Defines framing and how much of the subject is visible.

| Value | Description |
|-------|-------------|
| `full product` | Entire product visible with margin |
| `hero shot` | Dramatic product angle, often low with dynamic lighting |
| `detail shot` | Zoomed in on specific feature or texture |
| `in-context` | Product shown in use environment |
| `full body` | Person from head to toe |
| `waist-up` / `medium shot` | Person from waist up |
| `headshot` | Face and shoulders |
| `three-quarter body` | Person from knees up |

---

### depth_of_field

Controls what's in focus vs. blurred.

| Value | Effect |
|-------|--------|
| `shallow` | Subject sharp, background blurred (bokeh). Draws attention to subject. |
| `moderate` | Subject and nearby elements sharp, far background soft |
| `deep` / `wide` | Everything in focus. Good for room shots, flat lays |

**Example:** "shallow depth of field, product in sharp focus, background softly blurred"

---

## Lighting Parameters

### lighting.type

The source and character of light.

| Value | Look | Use Case |
|-------|------|----------|
| `soft natural daylight` | Gentle, diffused, approachable | Lifestyle, casual products |
| `studio softbox` | Clean, even, controlled | Commercial product photography |
| `golden hour` | Warm, orange/yellow tones | Outdoor lifestyle, aspirational |
| `overcast` | Soft, even, no harsh shadows | Natural portraits, moody lifestyle |
| `dramatic` / `chiaroscuro` | Strong contrast, deep shadows | Editorial, luxury, artistic |
| `flat` / `even` | No shadows, fully lit | E-commerce, product detail |
| `tungsten` / `warm artificial` | Indoor warm glow | Evening scenes, cozy atmosphere |
| `flash` / `strobe` | Harsh, high contrast | Fashion editorial, smartphone aesthetic |

---

### lighting.direction

Where the light comes from relative to subject.

| Value | Effect |
|-------|--------|
| `front` | Even lighting, minimal shadows, flat look |
| `side` / `left` / `right` | Creates dimension, shows texture |
| `back` / `backlit` | Silhouette effect, rim lighting, ethereal |
| `top` / `overhead` | Can create under-eye shadows on faces; good for products |
| `45-degree` | Classic portrait lighting, dimensional |
| `diffused window` | Soft directional, natural look |

---

### lighting.quality

The hardness or softness of light.

| Value | Look |
|-------|------|
| `soft` / `diffused` | Gentle transitions, subtle shadows |
| `hard` / `harsh` | Sharp shadow edges, high contrast |
| `dappled` | Light through leaves or blinds, pattern |
| `reflected` | Bounced light, fill shadows |

---

## Background Parameters

### background.type

The environment behind the subject.

| Value | Description |
|-------|-------------|
| `seamless` | Studio backdrop with no visible edges |
| `gradient` | Color transitions from light to dark |
| `environmental` | Real setting (room, outdoor, location) |
| `contextual` | Setting that tells a story about the product |
| `minimal` | Simple, non-distracting |
| `busy` / `layered` | Multiple elements, lifestyle richness |

---

### background.surface (for product shots)

What the product sits on.

| Value | Feel |
|-------|------|
| `white seamless` | Clean, e-commerce, neutral |
| `concrete` / `cement` | Industrial, modern, masculine |
| `marble` | Luxury, premium, beauty |
| `wood` / `natural wood` | Warm, organic, craft |
| `fabric` / `linen` | Soft, lifestyle, tactile |
| `reflective` / `glossy` | Tech, premium, sleek |
| `textured paper` | Artisan, handmade, creative |

---

### background.elements (for lifestyle/influencer)

Items visible in the setting. Be specific.

**Examples:**
- `["bed with white textured duvet", "rattan nightstand", "potted monstera plant"]`
- `["exposed brick wall", "floor-to-ceiling windows", "mid-century leather chair"]`
- `["clean kitchen counter", "copper pendant lights", "white subway tile backsplash"]`

---

## Subject Parameters (for influencer shots)

### subject.age_range

General age bracket. Avoid exact ages.

Values: `young adult`, `20s`, `30s`, `middle-aged`, `mature`

---

### subject.expression

Facial expression and energy.

| Value | Vibe |
|-------|------|
| `neutral` | Calm, editorial |
| `slight smile` | Approachable, friendly |
| `laughing` / `joyful` | Energetic, candid |
| `contemplative` | Thoughtful, moody |
| `confident` | Direct, empowered |
| `playful` | Fun, youthful |
| `serene` | Peaceful, relaxed |

---

### subject.pose

Body position and product interaction.

**Examples:**
- `"holding product at chest height, angled toward camera"`
- `"seated on couch, product on lap, relaxed posture"`
- `"mirror selfie, phone in right hand, product visible in left"`
- `"walking pose, product bag over shoulder, mid-stride"`
- `"lying on bed, product next to face, looking at camera"`

---

### subject.clothing

What the person is wearing. Be specific about type, color, material/texture, fit (oversized, fitted, cropped), and details (buttons, patterns, logos).

**Example:**
```json
"clothing": {
  "top": {
    "type": "oversized knit sweater",
    "color": "cream",
    "details": "chunky cable knit, slightly off-shoulder"
  },
  "bottom": {
    "type": "high-waisted jeans",
    "color": "medium wash blue",
    "details": "straight leg, raw hem"
  }
}
```

---

## Mood and Atmosphere

### mood / atmosphere

The emotional feel of the image.

| Value | Associated Elements |
|-------|---------------------|
| `minimal` | Clean, sparse, white space |
| `cozy` | Warm lighting, soft textures, intimate |
| `luxurious` | Rich materials, dramatic lighting, premium |
| `energetic` | Bright colors, dynamic poses, movement |
| `serene` | Soft colors, natural light, calm |
| `editorial` | High-fashion, dramatic, artistic |
| `candid` | Natural, unposed, authentic |
| `nostalgic` | Warm tones, vintage elements, film grain |
| `modern` | Clean lines, neutral palette, contemporary |

---

### color_palette

Dominant colors in the image. Specify 2–4 colors.

**Examples:**
- `["warm neutrals", "cream", "terracotta", "sage green"]`
- `["cool tones", "slate grey", "white", "pale blue"]`
- `["monochromatic black and white with gold accents"]`
- `["muted earth tones", "beige", "olive", "rust"]`

---

## Technical Parameters

### render_style

Visual treatment of the output.

| Value | Look |
|-------|------|
| `photo-realistic` | Looks like a photograph |
| `illustrated` | Drawn/graphic style |
| `3D render` | CGI look |
| `film photography` | Grain, color shifts, analog feel |
| `high-fashion editorial` | Stylized, dramatic |

---

### texture / detail_level

How much fine detail to include.

| Value | Description |
|-------|-------------|
| `high detail` | Sharp textures, fine details visible |
| `soft` | Slightly smoothed, beauty retouching feel |
| `sharp focus` | Crisp edges, no softening |
| `film grain` | Added noise for analog feel |

---

### camera_style (for influencer shots)

The apparent device/method used to capture.

| Value | Look |
|-------|------|
| `smartphone mirror selfie` | Casual, social media native |
| `DSLR portrait` | Professional, clean |
| `vintage digital camera` | Early 2000s aesthetic, flash |
| `disposable camera` | Grain, light leaks, candid |
| `editorial photography` | High-end, magazine quality |
| `paparazzi style` | Candid, telephoto, caught-in-action |

---

## Marketing-Specific Parameters

### negative_space

Empty area for text/logo overlay.

**Examples:**
- `"clear space above product for headline"`
- `"left third of frame empty for copy placement"`
- `"sky area at top for logo overlay"`

---

### text_safe_zone

Where text can be placed without covering key elements.

Values: `top`, `bottom`, `left`, `right`, `top-left`, `none needed`

---

### message_theme

The marketing message the image should support.

**Examples:**
- `"premium quality and craftsmanship"`
- `"everyday comfort and ease"`
- `"professional performance"`
- `"natural and sustainable"`
- `"bold self-expression"`

---

## Mirror Selfie Special Rules

When generating mirror selfie images, include:

```json
"mirror_rules": "ignore mirror physics for text on clothing, display text forward and legible to viewer"
```

This prevents backwards text on clothing/products in mirror reflections.
