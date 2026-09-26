# realemal.github.io

These files are the whole website at https://realemal.github.io, which lives
in its own GitHub repository named `realemal.github.io` (GitHub Pages only
serves a site at the domain root from a repository with that exact name).
Copy them there unchanged. `67Y56ALD7B` in `.well-known/apple-app-site-association`
is the Apple Developer Team ID.

- `.nojekyll` makes GitHub Pages serve the files as they are, including the
  `.well-known` folder, which its default site builder would skip.
- `.well-known/apple-app-site-association` tells iOS that links under
  `/plaid/` belong to the Safe to Spend app (`app.json` → `ios.associatedDomains`).
- `plaid/` is Plaid's OAuth redirect URI, `https://realemal.github.io/plaid/`.
  Banks that sign you in on their own site (Wells Fargo, Chase, Bank of
  America...) send you back there, iOS opens the app instead, and Plaid Link
  finishes the connection. The page only shows if the app isn't installed.
