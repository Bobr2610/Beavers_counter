[![Views](https://raw.githubusercontent.com/Bobr2610/Beavers_counter/main/counter.png)](https://github.com/Bobr2610/Beavers_counter)

# Beavers Counter

View counter for GitHub READMEs with **custom beaver images** from `theme/`.

> **Static badge above** updates every 5 minutes or when you run the workflow. For **increment on each view**, use Option 1 (Worker) or Option 2 (Moe-Counter).

Custom images + view tracking

Deploy the Cloudflare Worker from `worker/` — increments on each page view, uses your images. See [worker/README.md](worker/README.md).

After deploy, use your Worker URL:
```markdown
[![Views](https://beavers-counter.YOUR_ACCOUNT.workers.dev/)](https://github.com/Bobr2610/Beavers_counter)
```