# Helen's B&B: Website Redesign

A student redesign of helensbedandbreakfast.com, made by FED28 at Hyper Island.

## Team: Hamza El Bouazzaoui and Ayodeji Dairo (Home), Konstantina "Dina" Migadaki (About), Sara Lindén (Reservations)

# 1. The business
  
   Helen's B&B is a small bed and breakfast in Enskede, south Stockholm (Östrandsvägen 15), run by Helen since 2003. Guests stay in self-contained studios in a quiet, green area, 800 m from Svedmyra metro and about 20 minutes from the city center.
   Who visits: travelers who want a calm, personal place to stay outside the city center, and visitors to Globen or Stockholmsmässan.
  
  ### What we set out to fix:


   Information architecture: all content sat on one long page, split into tabs that jumped to the middle of it. Visitors had to scroll and search to find what they needed.
   The business and rooms weren't showcased: the rooms had no space of their own. They were mixed in with the sauna, garden, and Stockholm tips as tabs.
   An outdated site: it didn't support reservations well.

  ### Our goals:
 <sub>
   Separate pages with a clear structure, so guests find what they need quickly
   Showcase the business on its own page, and give the rooms a dedicated space
   Modernize the site and make booking faster, to increase reservations
 </sub>

# 2. How the site is structured
   helens-bnb-redesign/
   ├── index.html            Home page
   ├── about.html            About Helen, the house, getting here
   ├── reservations.html     Rooms, prices and booking request
   ├── css/
   │   ├── style.css         Shared styles: colors, fonts, header, footer, buttons, mobile nav
   │   ├── index.css         Home page only
   │   ├── about.css         About page only
   │   └── reservations.css  Reservations page only
   └── images/               All images

###How the CSS works
Every page loads style.css first, then its own page file. The page file can override shared styles.
Colors and fonts are CSS variables in :root at the top of style.css, for example var(--color-primary).
Layout uses flexbox. On screens 768px and smaller, the top nav is replaced by a bottom bar (.mobile-nav).
Colors
Variable
Hex
Used for
--color-bg
#F4F2EC
Page background
--color-surface
#FFFFFF
Cards, white sections
--color-text
#1E2A24
Headings, main text
--color-text-secondary
#46534C
Body text
--color-primary
#2F5D4A
Buttons, links, accents
--color-primary-hover
#1E3F31
Button hover
--color-tint
#EEF2EE
Light green backgrounds
--color-border
#D8D3C6
Lines and borders

Fonts: Newsreader for headings, Figtree for body text (Google Fonts).

3. How to update the site
   Text: edit it in the page's .html file.
   Images: add the file to images/, then update the src and alt in the HTML.
   Colors and fonts: change the variables in :root in css/style.css. Every page updates.
   Header, nav or footer: these are copied into every page, so make the same change in all three HTML files.
   Workflow: make a branch, commit (tag [ai] if AI wrote it), open a pull request, merge after a teammate approves.

4. How we used AI
   Commits tagged [ai] contain code generated or substantially written by AI. Untagged commits were written manually by us. Full prompts and decisions are in ai-log.md.
   We wrote most of the HTML and CSS ourselves and used AI in some cases to explain concepts and debug layout problems.

