# createProduct

Custom Claude Code slash command that turns a product listing URL (Meesho, Amazon,
Flipkart, Myntra, etc.) into a short-form video script.

## Usage

In this project, type:

/createProduct https://www.meesho.com/mini-led-torch-rechargeable-light-led-torch-usb-rechargeable-light-mini-torch/p/gqh761

Claude will:
1. Open the URL, read every product image (not just the first), and pull product name,
   description (inferring one if the listing doesn't have it), price, ratings, usage,
   dimensions/weight, and box contents.
2. Generate a 6-scene visual script (Hook / Setup / Primary Action / Versatility /
   Result / CTA) sized for a ~15s short-form video, ready to hand to an AI video
   model one scene at a time along with your uploaded product photos. If the box
   contains multiple items worth showing, Scene 2 becomes an unboxing beat.
3. Write a caption and 7-8 hashtags for the video, following that platform's creator/
   affiliate guidelines (e.g. Meesho's @meeshoapp tag + exact price callout rules).

## How it works

- The command is defined in .claude/commands/createProduct.md. Edit that file any time
  to change the extraction steps or the script format/timing.
- Platform-specific caption rules live in references/platform-guidelines.md. Only
  Meesho's guidelines are filled in for real; Amazon/Flipkart/Myntra use generic
  placeholder defaults until real creator guidelines are added to that file.
