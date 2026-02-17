# Gemini Prompt Examples

## Overview

Complete, tested examples for the three main use cases. Use these as starting templates and modify for your specific products.

---

## Example 1: Product Shot (Mattress)

**Brief:** Clean product photo of a memory foam mattress for Instagram feed

**JSON Prompt:**

```json
{
  "image_type": "product_shot",
  "product_specifications": {
    "product_line": "Memory Foam Mattress",
    "bed_frame": "Low-Profile Platform Bed Frame (black metal)",
    "material_focus": "Soft Tencel cover texture",
    "size_and_height": "Queen Size, 10-inch profile"
  },
  "setting": {
    "room_type": "Clean, airy loft bedroom",
    "key_colors": ["muted greens", "slate grey", "white"],
    "decor_style": "Industrial minimalist with Scandinavian accents",
    "unique_elements": ["exposed brick wall", "floor-to-ceiling windows"]
  },
  "art_direction": {
    "primary_mood": "Deep relaxation and tranquility",
    "lighting": "Soft morning light, gently illuminating the bed",
    "photography_style": "Architectural interior photography, clean edges",
    "focus_depth": "Shallow depth of field, with the focus sharp on the mattress"
  },
  "composition": {
    "aspect_ratio": "4:5 Vertical (Instagram Feed)",
    "shot_type": "Three-quarter bed view from the foot of the bed",
    "focal_point": "The pristine, unwrinkled mattress surface",
    "negative_space": "Clear space above the bed for logo placement"
  },
  "marketing_use": {
    "message_theme": "Pressure Relief and Cooling Comfort",
    "human_element": "None (Product focus)",
    "props_to_include": ["single clean glass of water on nightstand", "simple white linen bedding"]
  }
}
```

**Why it works:**
- Clear product identification with specific model names
- Setting supports the product story (clean, tranquil = good sleep)
- Aspect ratio matched to platform
- Negative space specified for marketing overlay
- Props are minimal and intentional

---

## Example 2: Product Shot (Beverage/CPG)

**Brief:** Premium coffee bag product photo for e-commerce

**JSON Prompt:**

```json
{
  "image_type": "product_shot",
  "product": {
    "type": "12oz coffee bag",
    "material": "matte kraft paper with black label",
    "shape": "standing pouch with flat bottom",
    "key_features": ["resealable top", "one-way valve visible"]
  },
  "photography": {
    "style": "studio commercial",
    "camera_angle": "45-degree from front right",
    "shot_type": "full product with margin",
    "aspect_ratio": "1:1",
    "depth_of_field": "moderate, product fully sharp"
  },
  "lighting": {
    "type": "studio softbox",
    "direction": "upper left at 45 degrees",
    "quality": "soft with subtle shadows",
    "highlights": "gentle reflection on bag surface"
  },
  "background": {
    "type": "gradient",
    "colors": ["warm cream fading to white"],
    "surface": "light wood grain texture visible at base"
  },
  "composition": {
    "focal_point": "product label",
    "props": ["scattered whole coffee beans around base", "single small plant in background, blurred"]
  },
  "mood": "premium artisan, warm, inviting",
  "technical": {
    "render_style": "photo-realistic",
    "detail_level": "high, texture visible on kraft paper"
  }
}
```

---

## Example 3: Lifestyle with Product (Mattress in Bedroom)

**Brief:** Aspirational bedroom scene featuring mattress for brand campaign

**JSON Prompt:**

```json
{
  "image_type": "lifestyle_product",
  "product": {
    "name": "Hybrid Cooling Mattress",
    "placement": "center of room on low platform frame",
    "visibility": "full mattress visible, surface texture highlighted",
    "bedding": "minimal white linen, slightly pulled back to show mattress edge"
  },
  "setting": {
    "room_type": "Modern master bedroom",
    "style": "California casual meets Japanese minimalism",
    "key_colors": ["warm white", "natural wood", "sage green accents"],
    "decor_elements": [
      "low wooden platform bed frame",
      "woven jute rug",
      "single olive tree in ceramic pot",
      "linen curtains, slightly billowing"
    ],
    "window": "large sliding glass door to garden, morning light streaming in"
  },
  "photography": {
    "style": "architectural interior photography",
    "camera_angle": "eye-level from bedroom doorway",
    "shot_type": "wide shot showing full room context",
    "aspect_ratio": "16:9",
    "depth_of_field": "deep, entire room in focus"
  },
  "lighting": {
    "time_of_day": "early morning, 7am",
    "source": "natural daylight through large window",
    "quality": "soft and warm, long shadows",
    "mood": "peaceful, serene"
  },
  "atmosphere": {
    "primary_mood": "tranquil sanctuary",
    "color_palette": ["warm neutrals", "touches of green", "natural wood tones"],
    "sensory_elements": "suggests stillness, fresh air, new day"
  },
  "composition": {
    "focal_point": "bed and mattress",
    "negative_space": "ceiling area for text overlay",
    "human_element": "none"
  },
  "marketing_context": {
    "message_theme": "Wake up refreshed in your personal sanctuary",
    "campaign_tone": "aspirational but attainable"
  }
}
```

---

## Example 4: Lifestyle with Product (Beverage)

**Brief:** Coffee product in cozy morning scene for social media

**JSON Prompt:**

```json
{
  "image_type": "lifestyle_product",
  "product": {
    "name": "Organic Medium Roast Coffee",
    "form_shown": "brewed in ceramic mug",
    "placement": "on wooden tray on unmade bed",
    "visibility": "mug prominent in foreground, bag visible in background"
  },
  "setting": {
    "location": "cozy bedroom, morning scene",
    "style": "lived-in, authentic, not overly styled",
    "key_elements": [
      "rumpled white linen bedding",
      "wooden breakfast tray",
      "open book face-down",
      "reading glasses",
      "small vase with single dried flower"
    ],
    "window": "soft light coming through sheer curtains"
  },
  "photography": {
    "style": "lifestyle editorial",
    "camera_angle": "overhead, flat lay of tray",
    "shot_type": "tight composition on tray and hands",
    "aspect_ratio": "4:5",
    "depth_of_field": "shallow, mug in focus"
  },
  "lighting": {
    "type": "natural morning light",
    "direction": "from right side",
    "quality": "soft, diffused, warm"
  },
  "human_element": {
    "visible": "hands only, holding mug",
    "skin_tone": "warm medium",
    "details": "natural nails, simple gold ring"
  },
  "mood": "cozy, peaceful, slow morning ritual",
  "technical": {
    "render_style": "photo-realistic",
    "texture": "tactile, you can feel the linen and ceramic"
  }
}
```

---

## Example 5: Influencer with Product (Mirror Selfie)

**Brief:** Influencer-style selfie featuring product for social campaign

**JSON Prompt:**

```json
{
  "image_type": "influencer_product",
  "subject": {
    "description": "Young woman taking a mirror selfie, playfully biting the straw of an iced green drink",
    "mirror_rules": "ignore mirror physics for text on clothing, display text forward and legible to viewer",
    "age": "young adult",
    "expression": "playful, nose scrunched, biting straw",
    "hair": {
      "color": "brown",
      "style": "long straight hair falling over shoulders"
    },
    "clothing": {
      "top": {
        "type": "ribbed knit cami top",
        "color": "white",
        "details": "cropped fit, thin straps, small dainty bow at neckline"
      },
      "bottom": {
        "type": "denim jeans",
        "color": "light wash blue",
        "details": "relaxed fit, visible button fly"
      }
    },
    "face": {
      "preserve_original": true,
      "makeup": "natural sunkissed look, glowing skin, nude glossy lips"
    }
  },
  "product_interaction": {
    "product_type": "iced beverage",
    "how_shown": "held in hand, drinking from straw",
    "details": "plastic cup with iced matcha latte and green straw",
    "visibility": "prominently featured"
  },
  "accessories": {
    "headwear": {
      "type": "olive green baseball cap",
      "details": "white NY logo embroidery, silver over-ear headphones worn over cap"
    },
    "jewelry": {
      "earrings": "large gold hoop earrings",
      "necklace": "thin gold chain with cross pendant",
      "wrist": "gold bangles and bracelets mixed",
      "rings": "multiple gold rings"
    },
    "device": {
      "type": "smartphone",
      "details": "white case with pink floral pattern"
    }
  },
  "photography": {
    "camera_style": "smartphone mirror selfie aesthetic",
    "angle": "eye-level mirror reflection",
    "shot_type": "waist-up composition, subject positioned on right side of frame",
    "aspect_ratio": "9:16 vertical",
    "texture": "sharp focus, natural indoor lighting, social media realism"
  },
  "background": {
    "setting": "bright casual bedroom",
    "wall_color": "plain white",
    "elements": [
      "bed with white textured duvet",
      "black woven shoulder bag on bed",
      "leopard print throw pillow",
      "distressed white vintage nightstand",
      "modern bedside lamp with white shade"
    ],
    "atmosphere": "casual lifestyle, cozy, spontaneous",
    "lighting": "soft natural daylight"
  }
}
```

**Why it works:**
- Mirror rules prevent text reversal issues
- Extensive clothing/accessory detail creates authenticity
- Smartphone aesthetic matches platform expectations
- Product interaction is natural, not forced
- Background elements support lifestyle story

---

## Example 6: Influencer with Product (Earbuds)

**Brief:** Tech product being used naturally for Instagram Reels thumbnail

**JSON Prompt:**

```json
{
  "image_type": "influencer_product",
  "subject": {
    "description": "Young man mid-workout, adjusting wireless earbuds",
    "age_range": "mid 20s",
    "expression": "focused, slight smile",
    "build": "athletic",
    "pose": "one hand touching earbud, other hand at side",
    "hair": {
      "style": "short fade",
      "color": "dark brown"
    },
    "clothing": {
      "top": {
        "type": "performance tank top",
        "color": "heather grey",
        "details": "moisture-wicking fabric, visible texture"
      },
      "bottom": "not visible in frame"
    },
    "skin": "light sweat sheen, healthy glow"
  },
  "product_interaction": {
    "product": "Wireless Sport Earbuds",
    "placement": "in ear, one hand adjusting",
    "visibility": "earbud clearly visible, logo facing camera",
    "action": "adjusting fit or changing track"
  },
  "photography": {
    "camera_style": "candid action shot",
    "angle": "eye-level, slightly off-center",
    "shot_type": "headshot to chest",
    "aspect_ratio": "9:16",
    "depth_of_field": "shallow, face and earbud sharp, background blurred"
  },
  "background": {
    "setting": "modern gym, blurred",
    "elements": ["out-of-focus gym equipment", "warm overhead lighting"],
    "atmosphere": "energetic, motivating"
  },
  "lighting": {
    "type": "mixed gym lighting",
    "quality": "warm, directional from above",
    "effect": "subtle rim light on shoulder"
  },
  "mood": "determined, in-the-zone, active lifestyle",
  "technical": {
    "render_style": "photo-realistic",
    "detail_level": "high on face and product"
  }
}
```

---

## Example 7: Conceptual/Abstract (LinkedIn Header)

**Brief:** Brain concept image for AI-related blog post

**JSON Prompt:**

```json
{
  "image_type": "conceptual",
  "concept": {
    "description": "Split brain visualization — human on left, AI/robotic on right",
    "symbolism": "human-AI collaboration, augmented intelligence"
  },
  "subject": {
    "left_half": {
      "type": "illustrated human brain",
      "style": "anatomical but stylized, not photorealistic",
      "color": "warm flesh tones, coral pink",
      "texture": "organic curves, soft"
    },
    "right_half": {
      "type": "robotic/circuit brain",
      "style": "matching shape to left half",
      "color": "cool blues and silver",
      "texture": "circuits, connection nodes, geometric patterns"
    },
    "integration": "two halves form one complete brain shape, seamless middle join"
  },
  "composition": {
    "aspect_ratio": "16:9",
    "subject_position": "centered",
    "negative_space": "minimal"
  },
  "background": {
    "color": "dark, near black",
    "gradient": "subtle radial gradient lighter behind brain"
  },
  "lighting": {
    "style": "dramatic",
    "effect": "brain halves subtly glowing"
  },
  "technical": {
    "render_style": "illustrated, not photorealistic",
    "detail_level": "sharp, clean lines",
    "text": "NO TEXT in image"
  },
  "mood": "thought-provoking, innovative, balanced"
}
```

---

## Quick Start: Minimum Viable Prompts

If you're in a hurry, these are the absolute minimum parameters:

### Product Shot (Minimum)

```json
{
  "product": "White ceramic coffee mug",
  "photography": {
    "angle": "45-degree front",
    "aspect_ratio": "1:1"
  },
  "background": "white seamless",
  "lighting": "soft studio"
}
```

### Lifestyle (Minimum)

```json
{
  "product": "Coffee mug on kitchen counter",
  "setting": "modern kitchen, morning light",
  "photography": {
    "angle": "eye-level",
    "aspect_ratio": "4:5"
  },
  "mood": "cozy morning"
}
```

### Influencer (Minimum)

```json
{
  "subject": "Woman in 20s holding coffee mug",
  "expression": "relaxed smile",
  "product_visibility": "mug clearly visible at chest height",
  "photography": {
    "style": "smartphone selfie",
    "aspect_ratio": "9:16"
  },
  "background": "cafe interior, blurred"
}
```

These will produce decent results. Add more parameters for better control.
