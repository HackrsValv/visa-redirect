# visa-redirect

Redirector for `visa.verslografija.lt` (the retired Buttondown archive).

GitHub Pages serves `404.html` for any unmatched path, so the wildcard JS
redirect forwards every `visa.verslografija.lt/<path>` to the same path on
`https://verslografija.lt` (where posts are now self-hosted). `index.html`
redirects the root to `/archive/`.

DNS: `visa.verslografija.lt` CNAME → `hackrsvalv.github.io`.
Rollback: repoint that CNAME back to `custom-domains.buttondown.com`.

`archive/<slug>/index.html` is one static page per post Buttondown published (sent or imported) while this
domain was the archive. They answer 200 and redirect without JavaScript (meta refresh),
so links in old emails reach the post even where scripts do not run or a 404 is shown
as an error. JS keeps the query and #hash; meta refresh drops them. New posts link
verslografija.lt directly, so this list does not need to grow.
