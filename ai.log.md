# AI Log

A record of how AI was used in the Helen's B&B redesign. Commits tagged `[ai]` contain code generated or substantially written by AI.

## Home page (Hamza & Ayo)

### Horizontal page scrolling problem

You noticed the mobile page was jiggling/sliding left and right. We identified likely causes such as:

- fixed widths
- `100vw`
- large desktop margins like `5rem`
- duplicate `.mobile-nav` CSS
- elements wider than the viewport

### Favicon logo

You asked for a PNG logo for your helens-bnb-redesign website to use as a favicon. I generated a minimalist logo featuring:

- an H
- house/roof shape
- leaf element
- "Helen's B&B"
- dark green + warm ivory styling

## Reservations page (Sara)

No AI usage.

## About page (Dina)

Before I started tagging commits, I also used Claude to explain concepts (flexbox, the cascade, rem vs px) and to debug small typos. That guidance isn't logged below; only the commits I tagged `[ai]` are.

### 1. `[ai]` add full-width white band to house and garden section

- **Prompt:** The house and garden section needs a full-width white background like in the design, but the body has side margins.
- **Produced:** A negative side margin to cancel the body margin, with matching padding to keep the text aligned, plus a green bullet color.
- **Kept / changed / thrown away:** Kept as given.

### 2. `[ai]` style getting here section

- **Prompt:** Give me the CSS for the "Getting here" section.
- **Produced:** A row with the distances list and the map, each distance on its own row with the value pushed right, and divider lines between rows.
- **Kept / changed / thrown away:** Kept as given.

### 3. `[ai]` edit style for last about section

- **Prompt:** I want a booking call-to-action, since the shared footer is plain. Fix my HTML for it.
- **Produced:** A full-width green band with a heading, short text, phone, address and a booking link.
- **Kept / changed / thrown away:** Removed the phone and address, since the footer already has them. Rewrote the heading to "Thinking about booking?". Styled the link as a white pill button.

### 4. `[ai]` Media queries

- **Prompt:** Make the page work on tablet and mobile, down to 320px.
- **Produced:** A tablet media query that stacks the sections, makes them full width and shrinks headings, plus a smaller-screen query for phones.
- **Kept / changed / thrown away:** Kept the approach. Changed in the next commit after testing.

### 5. `[ai]` edit media query

- **Prompt:** The text only fills half the screen on mobile.
- **Produced:** Found the cause with the browser inspector: my desktop rule capped the text at half width (`max-width: 50%`), which overrode the mobile full width. Added `max-width: 100%` to the mobile rules.
- **Kept / changed / thrown away:** Kept. I also fixed a missing closing brace that had nested one media query inside the other.

### 6. `[ai]` align about page with updated style.css and add mobile nav

- **Prompt:** After merging main, my side margins disappeared and the layout broke. Also add the new mobile nav.
- **Produced:** Side padding on `main` to replace the removed body margin, a mobile media query matching the shared stylesheet, the Material Icons link, and a rule hiding the mobile nav on desktop.
- **Kept / changed / thrown away:** The first version of the hide rule also hid the nav on phones. I replaced it with a desktop-only version. Threw away my earlier body margin fix.
