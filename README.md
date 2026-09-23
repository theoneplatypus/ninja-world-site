# ninjaworld.ca — the site

Static, no build step, no dependencies. `index.html` is the landing page; the
three legal pages are copies of `store/legal/` with their nav pointed at
`privacy.html` instead of `index.html` (on the store repo the privacy policy
IS the index; on a real site the landing page is).

## The URLs Play Console needs
- Privacy policy:  https://ninjaworld.ca/privacy.html
- Data deletion:   https://ninjaworld.ca/delete-account.html
Until the domain resolves, the GitHub Pages address works for both and is what
was pasted into the console on 22 September 2026:
  https://theoneplatypus.github.io/ninja-world-site/privacy.html
  https://theoneplatypus.github.io/ninja-world-site/delete-account.html

## Pointing ninjaworld.ca at it (once registered at Namecheap)
1. Namecheap → Domain List → ninjaworld.ca → Advanced DNS. Add:
   - A     @    185.199.108.153
   - A     @    185.199.109.153
   - A     @    185.199.110.153
   - A     @    185.199.111.153
   - CNAME www  theoneplatypus.github.io
2. GitHub → ninja-world-site → Settings → Pages → Custom domain: ninjaworld.ca
   → Save → wait for the DNS check → tick "Enforce HTTPS".
3. Rename `CNAME.later` to `CNAME` and push. NOT BEFORE the DNS is live: the
   moment a `CNAME` file exists, GitHub redirects the github.io address to the
   custom domain, and if that domain does not resolve yet the privacy-policy URL
   in Play Console 404s — which is a review rejection.

## Screenshots
Drop phone shots in `shots/` and replace the `<p class="empty">` inside
`#shots` in index.html with `<img src="shots/1.png" alt="...">` per shot.
