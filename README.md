# evergreenrpg.com

Static marketing and legal site for **Evergreen: Idle Hero RPG**, hosted on GitHub Pages.

| Page | URL |
|---|---|
| Landing | https://evergreenrpg.com/ |
| Privacy Policy | https://evergreenrpg.com/privacy.html |
| Terms of Service | https://evergreenrpg.com/terms.html |
| Support | https://evergreenrpg.com/support.html |

Plain HTML + one stylesheet (`assets/site.css`), no build step. Push to `main` and Pages deploys it.

## Editing

- **App Store button**: in `index.html`, replace the `Coming soon to the App Store` span with the
  `<a class="btn btn-primary" href="https://apps.apple.com/app/id…">` link in the comment beside it.
- **Legal pages**: bump the effective date in the `.meta` line whenever the text changes.
- **Images**: sources live in the game repo (`ArtSource/splash`, `ArtSource/store/listing_1320x2868`,
  `Assets/_Project/Art/Delivered/store/app_icon.png`). Web copies are resized with `sips` and encoded with
  `cwebp -q 80`.
- **Design**: palette and type follow the HeroIdleRPG mood board (bright & cheerful, earthy & warm,
  cool & mystical, pastel & playful; Lilita One display face, Nunito body). Tokens are at the top of `assets/site.css`.

## DNS for the custom domain

`CNAME` in this repo is set to `evergreenrpg.com`. At the registrar:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  john-ju.github.io
```

Then in the repo's Settings → Pages, confirm the custom domain and tick **Enforce HTTPS** once the certificate is issued.
