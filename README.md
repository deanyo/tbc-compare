# tbc-compare.github.io

Static comparison UI for Warcraft Logs (TBC). Connects to the Cloudflare
Worker proxy at `dnyo-wclogs-proxy`.

## Configure
- Set `API_BASE` in `index.html` to your Cloudflare Worker URL.
- The worker should expose `POST /compare` and return summary, gaps, rotation,
  and coach arrays like the `demoData` shape.

## Notes
- Compare player supports `name-realm` or `name@realm`. If omitted, it falls
  back to the realm field.
- Compare report URL lets you compare two specific runs (same player or
  another player on that report).
