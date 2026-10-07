# Off Road Mexican Food

Single-page website for Off Road Mexican Food, the green taco truck at 641 S 500 E St, American Fork, UT 84003. Explore the flavor.

`index.html` is self-contained: markup, styles, the logo (embedded once and reused in the hero and footer), Restaurant schema (JSON-LD) and a small script that shows live open/closed status in America/Denver time. It works opened on its own, with nothing next to it. `assets/` holds the full-size logo and the home-screen icon for phones. The only external request is Google Fonts (Barlow and Barlow Condensed).

## Logo

The logo is the round badge on the truck: "OFF ROAD" arched over red-rock spires, a black Jeep with its light bar lit, and "MEXICAN FOOD" arched along the bottom. It was rebuilt from a photo of the trailer. The glossy vinyl reflected the sky and the photographer, so the sky sheen was measured and removed in linear light, the badge was straightened, and the paint was flattened into its colors. The Jeep's windows were hidden by the reflection and were redrawn from the photo; the faint dark-on-dark "EXPLORE THE FLAVOR" tagline under the Jeep couldn't be recovered and is left out.

- `assets/off-road-logo.png`: 2048 × 2048 transparent PNG for menus, social media and print.
- The page embeds a 720px copy in the `<symbol id="logo">` near the top of `<body>`; replace that base64 data to swap the logo.
- On dark backgrounds, put the logo on lime (as in the footer); its outer ring is black.
- For print, the original artwork file from whoever made the trailer's vinyl will always beat a photo rebuild.

Badge colors: black `#141414`, charcoal `#3B3D3C`, tan `#B69760`, cream `#F0DA9B`, red `#96402F`, dark red `#5E2219`, light yellow `#FFDD70`.

## English and Spanish

The EN / ES switch sits in the top bar. English text lives in the HTML; every translatable element has a `data-i18n` key, and the Spanish for each key is in the `ES` object at the top of the script. To change copy, edit the English in the HTML and the matching Spanish entry together.

- The choice is remembered on that device. Spanish-language browsers start in Spanish.
- Link straight to Spanish with `?lang=es` (for Spanish social posts or flyers).
- The live open/closed text, hours, award seal and the catering text-message template all switch too.

## Ordering

DoorDash (delivery and pickup): https://www.doordash.com/store/off-road-mexican-food-american-fork-33566525/ — linked in the hero, menu intro, phone action bar and footer, and in the schema as an `OrderAction`.

## Brand colors

The page itself uses only these (plus transparencies of them). Lime is the truck's green; the logo sits on it just as it does on the trailer.

| Color | Hex |
| --- | --- |
| Lime | `#62F006` |
| Black | `#000000` |
| White | `#FFFFFF` |
| Signpost cream | `#F2ECDC` |

## Deploy

Any static host works. Point it at this repo with no build command and `/` as the publish directory:

- **GitHub Pages**: Settings → Pages → deploy from the `main` branch, root folder.
- **Cloudflare Pages** or **Netlify**: connect the repo, leave the build command empty.

## Before launch

- Confirm with the owner that they take phone orders and that (385) 283-0268 can receive texts.
- Confirm burrito names and spellings. DoorDash lists "Birria Burrito" and "Red Birria Peak a Boo" separately; the site treats them as one.
- Once the domain is known, add `<link rel="canonical">`, `og:url`, `og:image` (the logo) and schema `logo` / `url` to the `<head>`.
- Add the site's URL to the Google Business Profile.
- Update the rating and review count (hero and the Best of 2025 section) now and then.

## Editing hours

Hours are written into the page in several places, in both languages. Search `index.html` for `AM`, `PM`, `a.m.` and `p.m.` (times use `&nbsp;` between number and suffix, e.g. `8&nbsp;AM`) and update every match, plus the `HOURS` object in the script (minutes after midnight) and `opens` / `closes` in the JSON-LD.
