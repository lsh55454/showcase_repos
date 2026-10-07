# showcase_repos

A single-page portfolio that lists my **public** GitHub repositories with their descriptions and languages.

Live: <https://lsh55454.github.io/showcase_repos/> (linked from the main site [lsh55454.github.io](https://lsh55454.github.io/)).

## How it works

- `index.html` is fully static — HTML, CSS and JS in one file, no build step.
- On load it calls the public GitHub REST API (`https://api.github.com`) for user `lsh55454` and renders a card per repo, colored by primary language.
- `.nojekyll` makes GitHub Pages serve the file as-is.

## Notes

- Unauthenticated GitHub API calls are rate-limited (60 requests/hour per IP). If the limit is hit, the list will fail to load until it resets.
- Repo descriptions come from GitHub, so update them in each repo's settings rather than here.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
