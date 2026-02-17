# AI Image Prompt Builder

A Claude Project that helps marketing teams create structured JSON prompts for AI image generation. Instead of writing vague descriptions and hoping for the best, this project walks users through every parameter that matters and outputs precise, ready-to-use JSON.

## Why This Exists

AI image generation has improved dramatically — models like Google Gemini now produce results that are genuinely production-quality. But there's a gap between what the tools can do and what most teams actually get out of them.

The problem isn't the AI. It's the prompts.

Marketing teams describe what they want in plain language, miss critical parameters (aspect ratio, lighting direction, camera angle, depth of field), and wonder why the output doesn't match their vision. They try a few times, get inconsistent results, and move on.

After years of working with AI image generation across digital marketing teams, I built this project to solve that problem. Structured JSON prompts give you control over every variable that affects the output. Instead of "a nice product photo," you get a prompt that specifies lighting type, direction, camera angle, background surface, composition, and mood — and the results reflect that precision.

## What It Does

This is a **Claude Project** (not a standalone tool). You set it up in your Claude account with the included instructions and knowledge files. Once configured, it:

1. Takes your plain-language image description
2. Identifies the image type (product shot, lifestyle, or influencer)
3. Asks 3–5 targeted clarifying questions based on what's missing
4. Generates complete JSON ready to paste into your image generation tool
5. Explains why key parameters matter for your specific use case

### Supported Image Types

- **Product Shot** — Clean product photography, studio-style
- **Lifestyle with Product** — Product in context with environmental storytelling
- **Influencer with Product** — Person using/holding/wearing product, social media aesthetic

## Who This Is For

Digital marketers, content creators, and eCommerce teams who are already using AI image generation (or want to start) and need better, more consistent results. This is a power-user tool — it assumes you have access to both Claude and an AI image generation platform.

## Where the JSON Works

The structured JSON output has been tested primarily with **Google Gemini**, where it produces the most consistent results. The JSON format can be used with other image generation models, but your mileage may vary.

The Claude Project instructions themselves are built for **Claude** (Anthropic). They have not been tested as system prompts in other LLMs.

## Setup

### Prerequisites

- A [Claude](https://claude.ai) account (Pro, Team, or Enterprise recommended for extended usage)
- Access to an AI image generation tool (Google Gemini recommended)

### Installation

1. **Download this repository** — Clone or download all files
2. **Create a new Claude Project** at [claude.ai](https://claude.ai)
   - Go to Projects → Create Project
   - Name it whatever you'd like (e.g., "Image Prompt Builder")
3. **Add the instructions** — Copy the contents of `instructions.md` into the Project's Custom Instructions
4. **Add knowledge files** — Upload the three files from the `knowledge/` folder as Knowledge sources:
   - `parameter-guide.md`
   - `common-mistakes.md`
   - `example-prompts.md`
5. **Start a conversation** in the Project and describe the image you want

### Customization

This project is designed to be modified. Common customizations:

- **Add your product catalog** — Include product names, colors, materials, and dimensions as an additional knowledge file so Claude can auto-populate product details
- **Lock aspect ratios** — If your team only publishes to specific platforms, update the instructions to default to those ratios
- **Add brand guidelines** — Include your brand's color palette, photography style, and mood preferences as a knowledge file
- **Add example images** — Upload examples of images you like as reference for Claude to match

## File Structure

```
ai-image-prompt-builder/
├── README.md
├── LICENSE
├── instructions.md              # Claude Project custom instructions
└── knowledge/
    ├── parameter-guide.md       # Complete reference for all JSON parameters
    ├── common-mistakes.md       # What goes wrong and how to fix it
    └── example-prompts.md       # Tested, complete JSON examples
```

## Example

**You say:**
> "I need a product photo of our memory foam mattress for Instagram"

**Claude asks:**
> What's the specific product name and dimensions? What bed frame will it be on? Do you want a pure studio shot or a styled bedroom setting? Any specific color palette for the scene?

**You get:**

```json
{
  "image_type": "product_shot",
  "product_specifications": {
    "product_line": "Memory Foam Mattress",
    "bed_frame": "Low-Profile Platform Bed Frame (black metal)",
    "material_focus": "Soft Tencel cover texture",
    "size_and_height": "Queen Size, 10-inch profile"
  },
  "composition": {
    "aspect_ratio": "4:5 Vertical (Instagram Feed)",
    "shot_type": "Three-quarter bed view from the foot of the bed",
    "focal_point": "The pristine, unwrinkled mattress surface",
    "negative_space": "Clear space above the bed for logo placement"
  },
  "art_direction": {
    "primary_mood": "Deep relaxation and tranquility",
    "lighting": "Soft morning light, gently illuminating the bed",
    "photography_style": "Architectural interior photography, clean edges"
  }
}
```

Paste that JSON into Gemini (or your preferred image generation tool) and generate.

## License

MIT License — see [LICENSE](LICENSE) for details.

## Author

Created by [Matt Avery](https://github.com/elikibs) | [Elisha Consulting](https://elishaconsulting.com) | [LinkedIn](https://linkedin.com/in/mattavery)

Part of a digital marketing AI toolkit. See also: [Technical Page Grader](https://github.com/elikibs/technical-page-grader), [Schema Markup Generator](https://github.com/elikibs/schema-markup-generator), [Alt Text Generator](https://github.com/elikibs/alt-text-generator), [Word to HTML Converter](https://github.com/elikibs/word-to-html-converter)
