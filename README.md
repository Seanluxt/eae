# Eat Anchovies Every Day

The personal site: sixty lessons (plus one), each paired with a song, an artwork,
and something to explore.

This file explains how the site is put together and how to change it — in plain
language, no prior knowledge assumed.

---

## What each folder is

```
_lessons/        Your 61 lessons. One .md file = one lesson = one web page.
_layouts/        The templates. You write these ONCE; they render every lesson.
assets/css/      The styling (main.css). Change how the site looks here.
images/          Lesson artwork goes here.
index.html       The homepage (the list of all lessons).
_config.yml      Site settings. Rarely touched.
```

The key idea: you never build a page by hand. You write a lesson as plain text
in `_lessons/`, and the template in `_layouts/lesson.html` turns it into a page
automatically. Sixty-one lessons, one template.

---

## How to edit a lesson

1. Open the lesson's `.md` file in `_lessons/` (you can do this right on
   github.com — click the file, then the pencil icon).
2. The top part between the `---` lines is the structured info (title, links,
   image). The part below is the lesson text — just write normally, with a blank
   line between paragraphs.
3. Save (on GitHub this is the green "Commit changes" button). The site rebuilds
   itself in a minute or two.

## How to add a new lesson

Copy any existing file in `_lessons/`, rename it to something like
`my-new-lesson.md`, and edit the contents. That's it — it appears on the site
automatically. The filename (minus `.md`) becomes the web address.

## How the three links work

Each lesson has a `song`, an `art`, and an `explore` link. Each one has a
`label` (what the button says) and a `url` (where it goes). If a `url` is left
blank, that button simply won't appear — so a lesson with no explore link yet
won't show a broken button.

---

## Publishing

This site is built to run on **GitHub Pages**. Once the repository's Pages
setting is turned on (Settings → Pages → deploy from the `main` branch), every
time you save a change, GitHub rebuilds and publishes the site within a couple
of minutes. No separate upload step.

## Seeing it before it's live (optional)

You don't need this to work on the site, but if you ever want to preview locally:

```
gem install bundler jekyll
jekyll serve
```

Then open `http://localhost:4000` in your browser.

---

## Still to do

- [ ] Add the remaining 58 lessons to `_lessons/`
- [ ] Add lesson images to `images/`
- [ ] Fix lesson 13's song link (it has a doubled `http://https://`)
- [ ] Fill in lesson 53's missing "explore" link
- [ ] Replace placeholder alt text (e.g. lesson 1 says "test")
- [ ] The real visual design pass (palette, type, the pill-tags)
