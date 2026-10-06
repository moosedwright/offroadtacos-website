# Off Road Mexican Food

Single-page website for Off Road Mexican Food, the lime-green taco truck at 641 S 500 E St, American Fork, UT 84003.

Everything lives in `index.html`: markup, styles, Restaurant schema (JSON-LD) and a small script that shows live open/closed status in America/Denver time. The only external request is Google Fonts (Barlow and Barlow Condensed).

## Deploy

Any static host works. Point it at this repo with no build command and `/` as the publish directory:

- **Cloudflare Pages** or **Netlify**: connect the repo, leave the build command empty.
- **GitHub Pages**: Settings → Pages → deploy from the `main` branch, root folder.

## Before launch

- Confirm with the owner that they take phone orders and that (385) 283-0268 can receive texts.
- Confirm burrito names and spellings.
- Once the domain is known, add `<link rel="canonical">` and `og:url` to the `<head>`.
- Add the site's URL to the Google Business Profile.
- Update the rating and review count (hero and reviews heading) now and then.

## Editing hours

Hours are written into the page in several places. Search `index.html` for `8 AM` and `7 PM` and update every match, plus the `HOURS` object in the script (minutes after midnight) and `opens` / `closes` in the JSON-LD.
