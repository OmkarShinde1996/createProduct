---
description: Fetch an e-commerce product page and produce a short-form video script breakdown
---

The user ran `/createProduct $ARGUMENTS`. `$ARGUMENTS` is a product URL from an e-commerce
platform (Meesho, Amazon, Flipkart, Myntra, or similar). Do the following, in order.

## Step 1 — Fetch the product page

Open `$ARGUMENTS` using whatever web browsing/fetching tool is available in this environment
(a browser tool, WebFetch, or similar). These sites are JS-heavy, so a single fetch is often
incomplete — check for and open:
- The main title, price, discount, and rating summary
- "Product details" / "Highlights" / "Specifications" tables (weight, dimensions, material, etc.)
- The full description or bullet points
- Number of ratings and reviews, and a couple of sample reviews if visible
- The "Box contains" / "What's in the box" / "Package contents" section specifically — look for
  it under specifications, description bullets, or on a packaging-shot image (see below). If the
  listing states no accessories/manual/cable are included, note that explicitly.

If the page blocks fetching or content is thin, say so explicitly rather than inventing data.

### Study the product images directly

Don't just note that images exist — actually look at each one (fetch/view the image files if
your tools allow it), since visual details (shape, buttons/ports, materials, color variants,
scale relative to a hand, included accessories, packaging) are often clearer from the photos
than from the text and directly drive scene quality:

1. Go through every listing image, not just the first one.
2. For each image, note: what it shows (product alone / in use / scale reference / packaging /
   box contents laid out / size chart / infographic), and any detail relevant to filming a scene
   (button/switch placement, ports, textures, included accessories, how it's held or opened).
3. Specifically look for a packaging/"in the box" image (contents laid out next to an opened box)
   — this is what makes an unboxing scene possible. Record exactly what's laid out in it.
4. Keep a running list of concrete visual facts gathered this way — you'll draw on it directly
   when writing scenes in Step 3.

## Step 2 — Extract & present product details

Present a clearly labeled summary before the script:

- **Product name**
- **Description** — use what's on the page; if the listing has no real description (common on
  Meesho for generic/unbranded items), infer from the name/category/images what the product is,
  what it's used for, and its likely advantages. Label inferred content as "(inferred)" so it's
  never confused with what the listing actually states.
- **Price** (current price, original price, % off if shown)
- **Ratings** (average rating, number of ratings, number of reviews)
- **Usage** — how/when it's typically used
- **Dimensions / weight / height / length** — whatever the listing provides
- **Box contents** — every item confirmed to ship in the box (product, cable, manual, spare
  parts, etc.), gathered from the specs text and/or the packaging image
- **Key visual details from the images** — a short bullet list of what you actually saw across
  the product photos (colors/variants, ports/buttons, materials, how it's held, scale)
- **Seller info** if relevant (shop rating, dispatch time) — optional, brief

Flag anything you could not find on the page instead of guessing silently.

## Step 3 — Write the Visual Script Breakdown

Using the extracted details — including the visual facts gathered from the images and the box
contents — write a script following this exact 4-part / 6-scene retention formula. Every scene
must be tailored to *this specific product's* real features, form factor, and use case — never
generic placeholders. Each scene description will be used standalone as a prompt for an AI video
generation model (e.g. Google's video model) alongside an uploaded product image, so it must be
visually concrete and self-contained: specify camera framing/angle, lighting, what exactly the
hands are doing, and the product's state at that moment. Avoid vague language like "shows the
product" — describe the literal shot.

If the product has confirmed box contents worth showing (multiple items, accessories, a manual,
a nicely presented box), treat unboxing as a natural fit for **Scene 2: The Setup** — hands
opening the box and lifting out the confirmed contents (name them specifically, don't invent
items not in the box-contents list) — before moving into first use. If the box contains only the
product itself, skip the unboxing beat and use Scene 2 for powering on/prepping instead.

**The 4-part formula this maps to:**
- *The Intriguing Hook (0:00–0:02):* product in focus, showing its most unique feature/action
  immediately — something visually interesting enough to stop a scroll.
- *The Setup (0:02–0:05):* quick demo of how the product is prepped for use (turning on, loading,
  plugging in, assembling, etc.) — answers "how does this work?"
- *The Rapid-Fire Demonstration (0:05–0:12):* fast 1–2 second cuts showing the product solving its
  problem in multiple scenarios/contexts, proving versatility, ideally "oddly satisfying" to watch.
- *The Result & CTA (0:12–end):* the successful end result, then an explicit on-screen
  "Link in Bio" style call to action.

**Output exactly these 6 scenes, in this format:**

- **Scene 1: The Hook (2 seconds):** [camera framing/angle + what the hands do, showing the
  product's most unique feature/action]
- **Scene 2: The Setup (3 seconds):** [camera framing + hand actions prepping the product for use]
- **Scene 3: Primary Action (3 seconds):** [camera framing + hand actions showing the product
  solving its main problem, satisfying to watch]
- **Scene 4: Secondary Action/Versatility (3 seconds):** [rapid cut(s), 1–2 seconds each, camera
  framing + hand actions showing the product used in a different context/object/scenario]
- **Scene 5: The Satisfying Result (2 seconds):** [camera framing on the final completed/clean/lit
  result, hands optional — mostly product/result in frame]
- **Scene 6: The CTA (2 seconds):** [on-screen text overlay content + what it points to (e.g.
  "Link in Bio"), and any final camera move]

After the 6 scenes, add a one-line note reminding the user these are meant to be fed one-by-one,
alongside the uploaded product images, into their AI video model.

## Step 4 — Caption & hashtags

Read references/platform-guidelines.md and identify which platform's rules apply based on the
URL's domain (meesho.com, amazon.in, flipkart.com, myntra.com, etc.). Then write:

- **A caption** for the reel/video that complies with that platform's rules — e.g. for Meesho:
  include @meeshoapp, name the exact product/color variant shown, and state the exact current
  price fetched in Step 1 (labeled "per item"/"combo price" if applicable). For platforms with no
  user-supplied guidelines yet, use the general defaults in that file and say explicitly that
  these are defaults, not confirmed platform rules.
- **7–8 hashtags** — mix of product-specific, category/use-case, and platform/discovery tags
  (e.g. a branded/platform tag, a category tag, a problem-it-solves tag). Base them on the actual
  product, not generic filler.

If anything required for compliance (e.g. an exact live price) wasn't confirmed in Step 1, say so
instead of inventing it — an unconfirmed price in the caption risks the creator's payout.
