[![Views](https://beavers-counter.YOUR_ACCOUNT.workers.dev/)](https://github.com/Bobr2610/Beavers_counter)

# Beavers Counter

View counter with beaver images for GitHub README. Increments on each page view.

## Deployment

1. Deploy the Cloudflare Worker from the `worker/` folder — [instructions](worker/README.md)
2. Replace `YOUR_ACCOUNT` in the link above with your Cloudflare Workers subdomain (from `wrangler deploy` output)

## Use in other repositories

Add to your README (replace URL with your Worker):

```markdown
[![Views](https://YOUR-WORKER.workers.dev/)](https://github.com/Bobr2610/Beavers_counter)
```
