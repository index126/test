# OGAds locker return page

Single purpose: be the **Redirect URL** of the OGAds content locker, i.e. the URL the
user lands on once an offer converts.

## Publish

1. Create a GitHub repo (e.g. `og-locker-return`) and push `unlocked.html`.
2. Settings → Pages → Deploy from branch → `main` / root.
3. The URL becomes `https://<user>.github.io/og-locker-return/unlocked.html`.

## Use it

- Paste that URL into the locker's **Redirect URL** field on OGAds.
- Paste the same URL into the app factory's **Redirect URL** field.

The iOS shell matches it as a prefix and cancels the navigation, so the page never
actually loads in the app — tracking params OGAds appends still match. On web/Android
the page does load and posts the result back to the opener.
