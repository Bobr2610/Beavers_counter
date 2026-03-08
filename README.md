[![Hits](https://hits.sh/github.com/Bobr2610/Beavers_counter.svg?label=views)](https://hits.sh/github.com/Bobr2610/Beavers_counter/)

# Beavers Counter

View counter badge for GitHub. Increments on each page view.

## Embed in your README

**Option A — auto-increment on each view** (uses [hits.sh](https://hits.sh)):

```markdown
[![Hits](https://hits.sh/github.com/YOUR_USERNAME/YOUR_REPO.svg?label=views)](https://hits.sh/github.com/YOUR_USERNAME/YOUR_REPO/)
```

Replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub username and repository name.

**Option B — beaver images** (requires manual trigger or workflow from another repo):

```markdown
[![Views](https://github.com/Bobr2610/Beavers_counter/raw/main/counter.png)](https://github.com/Bobr2610/Beavers_counter)
```

## Increment from another repo

Needs a [PAT](https://github.com/settings/tokens) with `repo` scope. Add it as `COUNTER_REPO_TOKEN` in the other repo, then add `.github/workflows/count-views.yml`:

```yaml
name: Count Views
on:
  push:
    branches: [main]
jobs:
  ping:
    runs-on: ubuntu-latest
    steps:
      - run: |
          curl -X POST -H "Accept: application/vnd.github+json" \
            -H "Authorization: Bearer ${{ secrets.COUNTER_REPO_TOKEN }}" \
            -H "X-GitHub-Api-Version: 2022-11-28" \
            https://api.github.com/repos/Bobr2610/Beavers_counter/dispatches \
            -d '{"event_type":"page_view"}'
```

Manual increment: **Actions** → **View Counter** → **Run workflow**.
