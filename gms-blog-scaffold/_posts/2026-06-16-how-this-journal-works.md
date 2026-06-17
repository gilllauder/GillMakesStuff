---
title: "How this journal works"
date: 2026-06-16
category: Notes
excerpt: "A note to myself on writing here — naming a post, the few lines at the top, and how to drop in photos."
---

A quick reference so future-me remembers how to add to this journal. Once it's second nature, delete this post.

## Making a new post

Create a file in the `_posts` folder named like this:

`2026-06-20-dyeing-with-onion-skins.md`

The date and the title-with-dashes are both part of the filename — that's how the date and the web address get set.

## The few lines at the top

Every post starts with a small block between two `---` lines. Copy this and change the values:

```
---
title: "Your title here"
date: 2026-06-20
category: Natural dyeing
excerpt: "One sentence that shows on the journal list."
---
```

Everything below that block is just writing.

## Writing

Plain paragraphs become paragraphs. Beyond that:

- `## Heading` makes a section heading
- `**bold**` and `*italic*` do what you'd expect
- A line starting with `-` makes a bullet, like this one
- `> ` at the start of a line makes a pulled-out quote
- `[words to show](https://the-link.com)` makes a link

## Adding a photo

Put the image file in `assets/img/`, then drop this line where you want it:

`![A short description of the photo](/assets/img/onion-skins.jpg)`

The description in the square brackets is what screen readers and search engines read, so it's worth a few honest words.

That's the whole system. Write the file, save it, push it — the site rebuilds itself and the post appears.
