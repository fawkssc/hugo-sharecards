# Hugo Extended Share Cards

Hugo ShareCards extends the default Hugo share card template to enable using Resources for the image.
If a resource is used, a fingerprinted url is used.

## Usage

Add the following to the `head` block:

```html
{{ partial "hugo-sharecards/opengraph.html" . }}
{{ partial "hugo-sharecards/twitter_cards.html" . }}
```

## Default Configuration

`config/_default/config.toml`
```toml
title = "Your site title"
```

`config/_default/params.toml`
```toml
description = "Your site's description"
images = ["opengraph.png"] # Legacy configration; use Params.opengraph.image instead.

[opengraph]
    image = "opengraph.png"
```

## Page Front Matter

`content/**/*/index.md`
```markdown
---
title: "Page title"
summary: "Page summary"
description: "Page description" # Legacy configuration; use opengraph.description instead.
image = ["opengraph.png"] # Legacy configuration; use opengraph.image instead;
...
opengraph:
    description: "Page description"
    image: "opengraph.png"
---
```
