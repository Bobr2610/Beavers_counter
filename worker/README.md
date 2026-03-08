# Beavers Counter — Cloudflare Worker

View counter that **increments on each README view**. Returns SVG with beaver images from `theme/`.

## Deployment (5 minutes)

1. Install [Wrangler](https://developers.cloudflare.com/workers/wrangler/install-and-update/):
   ```bash
   npm install -g wrangler
   ```

2. Log in to Cloudflare:
   ```bash
   wrangler login
   ```

3. Create KV namespace:
   ```bash
   cd worker
   wrangler kv namespace create "COUNTER"
   ```

4. Copy the `id` from the output and paste it into `wrangler.toml`:
   ```toml
   kv_namespaces = [
     { binding = "COUNTER", id = "YOUR_ID" }
   ]
   ```

5. Deploy:
   ```bash
   wrangler deploy
   ```

6. Copy the URL (e.g. `https://beavers-counter.xxx.workers.dev`) and use it in your README:
   ```markdown
   [![Views](https://beavers-counter.xxx.workers.dev/)](https://github.com/Bobr2610/Beavers_counter)
   ```

## Free tier

Cloudflare Workers: 100,000 requests/day free.
