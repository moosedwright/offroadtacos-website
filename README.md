# Off Road Mexican Food

Single-page website for Off Road Mexican Food, the green taco truck at 641 S 500 E St, American Fork, UT 84003. Explore the flavor.

`index.html` is self-contained: markup, styles, the logo (embedded once and reused in the hero and footer), Restaurant schema (JSON-LD) and a small script that shows live open/closed status in America/Denver time. It works opened on its own, with nothing next to it. `assets/` holds only the home-screen icon for phones. The only external request is Google Fonts (Barlow and Barlow Condensed).

To swap the logo, replace the base64 data in the `<symbol id="logo">` near the top of `<body>`.

## Brand colors

Sampled from the logo. The page uses only these (plus transparencies of them):

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
- Confirm burrito names and spellings.
- Once the domain is known, add `<link rel="canonical">`, `og:url`, `og:image` (the logo) and schema `logo` / `url` to the `<head>`.
- Add the site's URL to the Google Business Profile.
- Update the rating and review count (hero and the Best of 2025 section) now and then.

## Editing hours

Hours are written into the page in several places. Search `index.html` for `8 AM` and `7 PM` and update every match, plus the `HOURS` object in the script (minutes after midnight) and `opens` / `closes` in the JSON-LD.
