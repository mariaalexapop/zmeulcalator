# Zmeul Calator - Clone Project Brief

## 1. Site Identity

- **Name:** Zmeul Calator
- **Tagline:** "Calatoria ca un zbor de zmeu" (Travel like a kite's flight)
- **Author:** Alexandra Enea
- **Domain:** zmeulcalator.ro
- **Logo:** Custom PNG logo (`/wp-content/uploads/2016/09/Zmeul-Calator.png`)
- **Language:** Primarily Romanian, with an English category for select posts
- **Active period:** October 2015 - February 2018 (~70 posts across 8 paginated pages, 9 posts per page)
- **Platform:** WordPress (self-hosted)
- **Theme:** "Let's Blog" (premium WordPress theme)
- **Copyright:** 2016

---

## 2. Content Inventory

### 2.1 Pages (5 total)

| Page | URL | Notes |
|------|-----|-------|
| Home | `/` | Blog listing with pagination (8 pages) |
| Home (alt) | `/home/` | Legacy alternate homepage |
| Destinatii | `/destinatii/` | Destinations page - **BROKEN** (Instagram widget requires auth) |
| Despre Zmeu | `/despre-zmeu/` | About page with author bio, quote, interests |
| Contact | `/contact/` | Bilingual contact form (RO/EN) |

### 2.2 Posts (~70 total, 9 per page)

Posts span from October 2015 to February 2018. Content types:

- **Travel narratives** - Detailed destination stories (India, Germany, France, Portugal, Turkey, Netherlands, Spain, Argentina)
- **Mountain hiking** ("Hai-hui prin munti") - Trail reports with practical info (Bucegi, Piatra Mare, Piatra Craiului)
- **Food/culinary** ("Taste the World") - Local cuisine experiences and recipes
- **Photography posts** - Photo essays, gallery posts, photography tips
- **Travel lifestyle** - Books, music, apps, marketing, mindfulness
- **Event coverage** - Festivals, art exhibitions, conferences (Web Summit)
- **English posts** - 4 posts in English (Amsterdam, Hamburg, Istanbul coffee, Lisbon azulejos)

### 2.3 Categories (19 total)

**Geographic hierarchy:**
- Asia > India
- Europe > France, Germany, The Netherlands, Portugal, Romania (> Bucuresti), Spain, Turkey
- South America

**Thematic:**
- Cu zmeul prin lume (Around the world) - main travel category
- Hai-hui prin munti (Mountain hiking)
- Taste the World (food & culinary)
- Travel Lifestyle > Travel Notes
- Diverse (miscellaneous)
- English

### 2.4 Post URL Structure

```
/{year}/{category-slug}/{post-slug}/
```

Examples:
- `/2016/india/nunta-indiana/`
- `/2016/europe/city-break-in-koln/`
- `/2016/hai-hui-prin-munti/padina-si-cascadele-din-jurul-ei/`
- `/2017/cu-zmeul-prin-lume/mindfulness-in-munti-piatra-craiului/`

---

## 3. Design System

### 3.1 Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Primary accent | Gold/Bronze | `#be9656` |
| Text / Frame borders | Black | `#222222` |
| Background | White | `#ffffff` |
| Button / Secondary text | Gray | `#888888` |
| Borders / Dividers | Light gray | `#e1e1e1` |

### 3.2 Typography

| Element | Font | Notes |
|---------|------|-------|
| Body / Menu | Source Sans Pro | Sans-serif, 14px base |
| Headings | Roboto | Sans-serif |
| Dates / Accents | Lustria | Serif, Georgia fallback |

All loaded via Google Fonts.

### 3.3 Design Patterns

- **Frame aesthetic**: Dark `#222222` borders creating a "framed" look around content areas (`.frame_top` class)
- **Post titles**: Uppercase with letter-spacing
- **Dates**: Gold color, serif font (Lustria)
- **"Read More" links**: Gold text
- **Image thumbnails**: 700x529px standard size
- **Post grid**: Card-style listing on homepage/archives
- **Dark footer**: Contrasting dark background with light text

---

## 4. Layout Structure

### 4.1 Global Layout

```
+--------------------------------------------------+
| Top Bar (minimal, white)                          |
+--------------------------------------------------+
| Header: Logo + Primary Navigation + Social Icons  |
+--------------------------------------------------+
| Content Area (left)    | Sidebar (right)          |
|                        |                          |
| Post grid / Single     | - Author bio widget      |
| post content           | - Search widget          |
|                        | - Facebook page widget   |
|                        | - Blogroll (30+ links)   |
|                        | - Instagram feed widget  |
|                        | - Recent posts           |
+--------------------------------------------------+
| Footer (dark bg)                                  |
| Copyright + Social Links + Footer Menu            |
+--------------------------------------------------+
```

### 4.2 Homepage / Archive Pages

- 9 posts per page with pagination ("Newer Posts" / "Older Posts")
- Each post card shows:
  - Featured image thumbnail (700x529px)
  - Post title (uppercase, letter-spaced)
  - Publication date (gold, serif)
  - Category tags as links
  - "Read More" link (gold)
  - Comment count

### 4.3 Single Post Layout

- Full-width content area (no sidebar on some posts)
- Post header: Title + Date + Categories breadcrumb
- Content: Paragraphs with inline images and thumbnail galleries
- Image galleries: Linked thumbnails triggering lightbox overlay
- Social sharing buttons: Facebook, Twitter, Pinterest (+ 2 others)
- Related posts section: 3 related articles with thumbnails and dates
- Comment form: Name, Email, Website, Message fields
- Post navigation between posts

### 4.4 Sidebar Widgets

1. **Author bio**: "Enthusiastic Traveler | Self-Taught Photographer..." with photo
2. **Search**: Autocomplete search widget
3. **Facebook Page**: Like widget for zmeulcalator.ro page
4. **Blogroll**: 30+ categorized travel blog links (Romanian travel blogs, foreign travel blogs, book blogs)
5. **Instagram feed**: Grid of recent photos (**currently broken** - requires re-authorization)
6. **Recent posts**: Thumbnails with category and date

---

## 5. Navigation

### 5.1 Primary Menu (Header)

```
Home
Cu zmeul prin lume (dropdown)
  +-- Asia > India
  +-- Europe > France, Germany, Netherlands, Portugal, Romania, Spain, Turkey
  +-- South America
Hai-hui prin munti
Taste the World
Travel lifestyle (dropdown)
  +-- Travel notes
Despre Zmeu
Contact
English
```

### 5.2 Mobile Navigation

- Collapsible mobile menu (`.mobile_menu_wrapper`)
- Megamenu capability (`.megamenu` class)

### 5.3 Footer Menu

- Simplified navigation links
- Social media icon links

---

## 6. Integrations & Plugins

### 6.1 Social Media

| Platform | Handle/URL | Integration Type |
|----------|-----------|-----------------|
| Facebook | zmeulcalator.ro | Page widget, share buttons, schema link |
| Instagram | @zmeulcalator | Feed widget (**broken**), schema link |
| Twitter | @alexandra_enea | Share buttons, schema link |
| Pinterest | zmeulcalator | Share buttons, schema link |
| Flickr | (portfolio link) | Link in footer/social icons |

### 6.2 WordPress Plugins (detected)

| Plugin | Purpose | Status |
|--------|---------|--------|
| Contact Form 7 | Contact page form | Working |
| Google reCAPTCHA | Spam protection on forms | Working |
| Facebook Page Like Widget | Sidebar Facebook embed | Working |
| Instagram Feed (likely JEJEWE or Jejewe) | Sidebar Instagram grid | **BROKEN** - needs re-auth |
| Yoast SEO | Sitemap generation, meta tags | Working |
| Lightbox/Gallery plugin | Image gallery overlays | Working |
| WordPress Emoji | Native emoji support | Working |

### 6.3 SEO & Schema

- **Yoast SEO** generating XML sitemaps (post, page, attachment, category)
- **Schema.org markup**: WebSite schema with SearchAction, Person schema with social profiles
- **Open Graph tags**: Present for social sharing
- **Permalink structure**: `/%year%/%category%/%postname%/`

---

## 7. Known Issues (Theme-Related)

### 7.1 Broken Elements

1. **Instagram feed widget** - Shows "Please authorize with your Instagram account" on sidebar and Destinations page. Requires Instagram API re-authorization (likely due to Instagram API deprecation/changes since 2018).

2. **Destinations page (`/destinatii/`)** - Completely broken. Shows only the Instagram authorization message instead of destination content. Was likely powered by an Instagram gallery or custom widget.

3. **Some post URLs returning 404** - Newer posts (2017-2018) have inconsistent URL patterns. Some posts from the sitemap may have different slugs than expected.

### 7.2 Potential Theme Issues to Investigate

- Theme hasn't been updated in years - may have compatibility issues with newer WordPress/PHP versions
- Google Fonts loading method may need updating
- jQuery dependency may be outdated
- Mobile responsiveness should be verified on modern devices
- Facebook widget may need SDK version update
- reCAPTCHA version may need updating (v2 to v3)

---

## 8. Technical Stack Summary

| Component | Value |
|-----------|-------|
| CMS | WordPress (self-hosted) |
| Theme | Let's Blog (premium) |
| Language | PHP (WordPress) |
| Database | MySQL (WordPress standard) |
| Fonts | Google Fonts (Source Sans Pro, Roboto, Lustria) |
| SEO | Yoast SEO |
| Forms | Contact Form 7 + reCAPTCHA |
| Social | Facebook Widget, Instagram Feed, sharing buttons |
| Gallery | Lightbox-enabled image galleries |
| Emoji | WordPress native emoji via s.w.org CDN |
| Sitemap | Yoast-generated XML sitemaps |

---

## 9. Complete Post Inventory (by date, newest first)

### 2018
1. Un an nou, o viata noua in... Amsterdam (Feb 8) - Netherlands

### 2017
2. The Elbphilharmonie Hamburg - 'Ode to Joy' Light Show (May 9) - English
3. 3 great places in Istanbul for coffee lovers (Apr 29) - English, Turkey
4. The story of azulejos - Lisbon, tiles and sun (Nov 19, 2016 or 2017) - English, Portugal
5. Mindfulness in munti | Piatra Craiului (Mar 13) - Hiking
6. Gusturile calatoriilor si preferintele culinare (Feb 20) - Taste the World
7. Experience Bucharest (Feb 14) - Romania
8. Arta la metrou - 2 statii spectaculoase (Feb 11) - Cu zmeul prin lume
9. Go Wild si calatoriile pentru suflet (Feb 9) - Travel lifestyle
10. Livin' la vida loca sau cum a fost in Buenos Aires (Jan 15) - South America

### 2016 (bulk of content)
11. Com o seu silencio - O seara de Fado (Dec 18) - Portugal, Taste the World
12. Planuri de travel pentru 2017 (Dec 16) - Travel lifestyle
13. Instagram in poze de sarbatoare #25panape25 (Dec 4)
14. Speicherstadt - Hamburg (Nov 26) - Germany
15. 9 startup-uri de travel de la Web Summit 2016 (Nov 22) - Diverse
16. Web Summit Live Text (Nov 5) - Diverse
17. Bucurestiul intr-o poveste de toamna (Oct 23)
18. Despre carti si citit (Sep 13) - Travel lifestyle
19. Impresii de o zi din Dusseldorf (Sep 10) - Germany
20. City Break in Koln (Aug 27) - Germany
21. Padina Fest si Canionul Horoabei (Aug 13) - Hiking
22. Locuri din Paris in care m-as intoarce oricand (Aug 2) - France
23. O zi in Piatra Mare (Jul 20) - Hiking
24. Cu sportul in vacanta (Jul 18) - Diverse
25. 5 idei faine de campanii de marketing in turism (Jul 12) - Travel lifestyle
26. Cu bicicleta prin Transilvania (Jul 3) - Romania
27. 5 carti care sa va inspire in viitoarele calatorii (Jun 30) - Diverse
28. Cum sa descoperi Europa cu trenul (Jun 25) - Europe
29. Statui Vivante 2016 - Galerie foto (Jun 18)
30. Festivalul B-FIT in the Street! 2016 (Jun 12)
31. Festivalul statuilor vivante revine in Bucuresti (Jun 7) - Romania
32. Incredible India - video (May 20) - India
33. Noua campanie Airbnb (May 18) - Diverse
34. Palatul Dacia-Romania la Art Safari 2016 (May 6) - Romania
35. 3 aplicatii pentru bucataria locala (Apr 19) - Diverse, Taste the World
36. In calatorie pe Facebook si Instagram - #TheTravelingGame (Apr 12) - Diverse
37. Aleile Gradinii Botanice din Bucuresti (Apr 5)
38. Provocarile fotografiei de calatorie (Apr 1) - Diverse
39. Creativitate in fotografie (Mar 14) - Diverse
40. 8 martie in culori (Mar 8) - Diverse
41. De la festivaluri Indiene adunate (Feb 25) - India
42. De ce facem fotografii? (Feb 18) - Diverse
43. Visatorii si rasariturile de soare (Feb 11) - Romania
44. Pauza de poze II (Feb 7) - Romania
45. Adu spiritul calatoriilor in lumea copilului tau (Jan 26) - Diverse
46. Bucharest City App (Jan 25) - Romania/Bucuresti
47. Nunta indiana (Jan 22) - India
48. Provocarea suprema: Saree-ul! I & II (Jan 20) - India
49. Ignoranta omului oglindita in apele din Alleppey (Jan 16) - India
50. Prin valurile verzi de ceai din Munnar (Jan 13) - India
51. Cele 9 emotii ale dansurilor Kathakali (Jan 8) - India
52. Oamenii Indiei (Jan 6) - India

### 2015
53. Cate am auzit despre India si cate s-au confirmat (Dec 14) - India
54. 5 melodii pentru sufletul calatorului din voi (Dec 8) - Diverse
55. Cele mai frumoase festivaluri Europene 2016 (Dec 6) - Europe
56. Apus de iarna in Bucegi (Nov 30) - Hiking
57. Plimbare prin Bucegi (Nov 26) - Hiking, Romania
58. Bucurestiul si arta de a calatori (Nov 23) - Travel lifestyle
59. Brasovul in lumina toamnei (Nov 14) - Romania
60. Anul acesta Mos Craciun ma gaseste pe taramul cocotierilor (Oct 29) - India
61. Pauza de poze I (Oct 29) - Romania

---

## 10. Clone Scope & Recommendations

### What to clone exactly:
- Full WordPress installation with Let's Blog theme
- All 5 pages with their content
- All ~70 posts with images, galleries, and metadata
- Category structure (19 categories with hierarchy)
- Navigation menus (primary + footer + mobile)
- Sidebar widgets (author bio, search, blogroll, recent posts)
- Color scheme and typography (gold/black/white + Source Sans Pro/Roboto/Lustria)
- Social sharing buttons on posts
- Related posts sections
- Comment forms with reCAPTCHA
- Yoast SEO configuration and sitemaps
- Lightbox gallery functionality
- Schema.org markup

### Theme fixes to consider:
1. **Fix Instagram widget** - Re-authorize with Instagram API or replace with updated Instagram plugin compatible with current Instagram Graph API
2. **Fix Destinations page** - Restore content or redesign without Instagram dependency
3. **Update Facebook widget** - Ensure Facebook SDK version is current
4. **Update reCAPTCHA** - Migrate to v3 if still on v2
5. **Check theme PHP compatibility** - Ensure Let's Blog theme works with current PHP version
6. **Verify mobile responsiveness** - Test on modern devices and screen sizes
7. **Update Google Fonts loading** - Use `display=swap` for better performance
8. **Fix any broken post URLs** - Verify all sitemap URLs resolve correctly
