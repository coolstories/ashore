# Readyway

The marketing site for Readyway — the part of travel that happens after the plan.

`index.html` is the whole site: one self-contained document with no build step,
no dependencies, and nothing fetched from another host. Open it in a browser to
work on it.

## Publishing it

The repository is private and nothing is being served yet. To put it online with
GitHub Pages:

```sh
gh repo edit --visibility public --accept-visibility-change-consequences
gh api -X POST repos/:owner/:repo/pages -f 'source[branch]=main' -f 'source[path]=/'
```

It will appear at `https://<owner>.github.io/readyway/` within a minute or two.

## Before it goes public

Two things on the page are claims rather than copy, and they are worth a second
look from someone who can stand behind them:

- **The figures in the receipt panel** — zero false confirmations, zero double
  bookings, zero charged-for-nothing. These are real measurements from the
  execution benchmarks, but they are internal test results.
- **"Real systems, not a demo"** — true of the integrations, which speak each
  provider's protocol properly. Every one of them is currently pointed at test
  and sandbox credentials.
