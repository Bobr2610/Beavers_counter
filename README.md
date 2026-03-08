[![Views](https://raw.githubusercontent.com/Bobr2610/Beavers_counter/main/counter.png)](https://github.com/Bobr2610/Beavers_counter)

# Beavers Counter

View counter with custom beaver images. Use in any repo.

## Use in another repo

**1. Add to README** (one line):

```markdown
[![Views](https://raw.githubusercontent.com/Bobr2610/Beavers_counter/main/counter.png)](https://github.com/Bobr2610/Beavers_counter)
```

**2. (Optional) Increment on push** — copy [views.yml.example](views.yml.example) to `.github/workflows/views.yml`, add secret `COUNTER_PAT` (PAT with `repo` scope).

---

*Shared counter for all repos. For per-repo counters with view tracking, deploy the Worker from `worker/` and use `?id=your-repo-name`.*
