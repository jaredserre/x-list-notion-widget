# X List Notion Widget

A small GitHub Pages widget that displays posts from a **public X/Twitter List** and reloads itself on a configurable schedule. It uses X's own embedded List timeline, so no API key or GitHub Action is required.

## Fast setup in GitHub's website

1. Create a new **public** GitHub repository, such as `x-list-notion-widget`.
2. Upload `index.html` and `.nojekyll` to the repository's top level.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose `main` and `/ (root)`, then click **Save**.
6. Your page will use this pattern:

   `https://YOUR-USERNAME.github.io/x-list-notion-widget/`

## Add your X List

Copy the numeric ID from the public List's URL. For example:

`https://x.com/i/lists/1234567890123456789`

The List ID is:

`1234567890123456789`

Add it to your GitHub Pages URL:

`https://YOUR-USERNAME.github.io/x-list-notion-widget/?list=1234567890123456789`

You can also set the title, theme, and refresh interval:

`https://YOUR-USERNAME.github.io/x-list-notion-widget/?list=1234567890123456789&title=Tax%20Policy&theme=light&refresh=5`

## Embed in Notion

1. Type `/embed` in Notion.
2. Paste the full GitHub Pages URL, including the `?list=...` section.
3. Select **Embed link**.
4. Resize the block to the width and height you prefer.

## URL settings

| Setting | Example | Meaning |
|---|---|---|
| `list` | `list=1234567890123456789` | Required X List ID, or a full X List URL |
| `title` | `title=Tax%20Policy` | Header shown above the feed |
| `theme` | `theme=light` | `light`, `dark`, or `auto` |
| `refresh` | `refresh=5` | Reload interval in minutes; `0` disables it |

## Important limits

- The X List must be public.
- A private List cannot be shown in a public GitHub Pages iframe.
- Privacy extensions, ad blockers, workplace firewalls, or an X outage may prevent X's embedded timeline from loading.
- The page asks X for fresh content whenever it reloads, but X controls any caching inside its embed service.
- The layout of the posts themselves is controlled by X. A fully custom layout would require an authenticated server-side API integration.
