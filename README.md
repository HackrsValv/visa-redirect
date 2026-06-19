# visa-redirect

Redirector for `visa.verslografija.lt` (the retired Buttondown archive).

GitHub Pages serves `404.html` for any unmatched path, so the wildcard JS
redirect forwards every `visa.verslografija.lt/<path>` to the same path on
`https://verslografija.lt` (where posts are now self-hosted). `index.html`
redirects the root to `/archive/`.

DNS: `visa.verslografija.lt` CNAME → `hackrsvalv.github.io`.
Rollback: repoint that CNAME back to `custom-domains.buttondown.com`.
