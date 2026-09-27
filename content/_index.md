---
title: "Demonstration Presentation"
layout: "slides"
---

{{< slide id="title" layout="title" transition="zoom" >}}

# Hugo PowerSlides

## A Markdown slide system for Hugo

Lightweight, static, and easy to theme.

{{< notes >}}
Briefly introduce Hugo PowerSlides and explain that the presentation is written entirely in Markdown.
{{< /notes >}}

---

{{< slide id="features" transition="slide" >}}

# Features

<ul>
  <li class="anim-fade">Keyboard and clicker navigation</li>
  <li class="anim-up">Presenter mode with synchronized speaker notes</li>
  <li class="anim-zoom">Ready-made layouts and thirteen transitions</li>
  <li class="anim-fade">Styled code, tables, quotes, and callouts</li>
  <li class="anim-up">Color themes driven by CSS custom properties</li>
</ul>

{{< notes >}}
Explain each feature briefly. Arrow keys, Page Up and Page Down, Space, Home, and End navigate; F toggles fullscreen; P opens presenter mode.
{{< /notes >}}

---

{{< slide id="part-layouts" layout="section" transition="wipe" >}}

# Layouts

Pick a layout per slide with the `layout` option.

{{< notes >}}
Section slides are numbered automatically, in order of appearance.
{{< /notes >}}

---

{{< slide id="layouts" transition="slide" >}}

# Available layouts

| Layout        | Use it for                          | Needs `image` |
| ------------- | ----------------------------------- | :-----------: |
| `default`     | Regular content                     |       —       |
| `title`       | Opening or closing slide            |       —       |
| `section`     | Numbered part divider               |       —       |
| `center`      | Statements and quotes               |       —       |
| `hero`        | Full-bleed image with a big message |      Yes      |
| `image-left`  | Image on the left, text on the right |     Yes      |
| `image-right` | Text on the left, image on the right |     Yes      |

```markdown
{{</* slide layout="image-left" image="/images/landscape.svg" alt="..." */>}}
```

---

{{< slide id="hero" layout="hero" image="/images/landscape.svg" transition="blur" >}}

# Ship it.

The `hero` layout places an image behind the text, with a dark scrim that keeps it readable.

{{< notes >}}
Without alt text, the hero image is treated as decorative.
{{< /notes >}}

---

{{< slide id="image-left" layout="image-left" image="/images/landscape.svg" alt="Stylized mountains at sunset under a purple sky" transition="push" >}}

# Image on the left

Text sits on the right and stays vertically centered.

- The image covers its half of the slide.
- On small screens, it stacks above the text.

---

{{< slide id="image-right" layout="image-right" image="/images/landscape.svg" alt="Stylized mountains at sunset under a purple sky" transition="push" >}}

# Image on the right

Same layout, mirrored.

Use `alt` to describe meaningful images.

---

{{< slide id="quote" layout="center" transition="fade" >}}

> Simplicity is prerequisite for reliability.

— Edsger W. Dijkstra

---

{{< slide id="columns" transition="slide" >}}

# Columns

{{< columns count="3" >}}
{{< column >}}
### Write

Plain Markdown, one file.
{{< /column >}}
{{< column >}}
### Build

`hugo` renders static HTML.
{{< /column >}}
{{< column >}}
### Present

Any browser, no dependency.
{{< /column >}}
{{< /columns >}}

```markdown
{{</* columns count="3" */>}}
{{</* column */>}}
### Write
...
{{</* /column */>}}
{{</* /columns */>}}
```

---

{{< slide id="part-content" layout="section" transition="wipe" >}}

# Markdown content

Code, tables, quotes, and callouts, styled out of the box.

---

{{< slide id="code" transition="up" >}}

# Code

Fenced blocks are highlighted by Hugo; inline `code` gets a subtle background.

```js
function goNext() {
  render(currentIndex + 1);
}
```

Set the highlighting style in `hugo.toml`:

```toml
[markup.highlight]
  style = "github-dark"
```

---

{{< slide id="tables" transition="up" >}}

# Tables

Standard Markdown tables, with column alignment:

| Transition | Style   | Duration |
| :--------- | :------ | -------: |
| `fade`     | Subtle  |   450 ms |
| `push`     | Classic |   450 ms |
| `iris`     | Retro   |   700 ms |
| `spin`     | Kitsch  |  1000 ms |

---

{{< slide id="text" transition="up" >}}

# Text elements

> Blockquotes stand out with an accent bar.

Press <kbd>F</kbd> for fullscreen, <kbd>P</kbd> for presenter mode, and <mark>highlight</mark> key words.

- [x] Task lists
- [ ] Nested lists
  - with smaller items

---

{{< slide id="callouts" transition="up" >}}

# Callouts

{{< callout type="note" >}}
A neutral remark.
{{< /callout >}}

{{< callout type="tip" title="Pro tip" >}}
Each type has its own icon and title, not just a color.
{{< /callout >}}

{{< callout type="warning" >}}
Something to be careful about.
{{< /callout >}}

---

{{< slide id="figure" transition="zoom" >}}

# Figure shortcode

{{< figure src="/images/pipeline.svg" alt="Diagram showing Markdown flowing through Hugo into a PowerSlides presentation" caption="From Markdown to a static presentation, through Hugo." >}}

```markdown
{{</* figure src="/images/pipeline.svg" alt="..." caption="..." */>}}
```

---

{{< slide id="part-transitions" layout="section" transition="iris" >}}

# Transitions

From subtle to shamelessly kitsch.

---

{{< slide id="transitions" transition="fade" >}}

# Choosing a transition

Set it per slide, per page (`transition` in front matter), or site-wide:

```markdown
{{</* slide transition="flip" */>}}
```

{{< columns count="3" >}}
{{< column >}}
### Subtle

`fade` `slide` `up` `zoom` `blur` `none`
{{< /column >}}
{{< column >}}
### Classic

`push` `flip` `wipe` `iris`
{{< /column >}}
{{< column >}}
### Kitsch

`spin` `bounce` `swing` `tv`
{{< /column >}}
{{< /columns >}}

{{< notes >}}
The next slides demonstrate each transition. They all fall back to a short fade when the system asks for reduced motion.
{{< /notes >}}

---

{{< slide id="transition-slide" transition="slide" >}}

# `slide`

Slides in horizontally, following the navigation direction.

---

{{< slide id="transition-up" transition="up" >}}

# `up`

Moves upward into view.

---

{{< slide id="transition-zoom" transition="zoom" >}}

# `zoom`

Zooms in and out.

---

{{< slide id="transition-blur" transition="blur" >}}

# `blur`

Comes into focus.

---

{{< slide id="transition-push" transition="push" >}}

# `push`

Pushes the previous slide out of the way.

---

{{< slide id="transition-flip" transition="flip" >}}

# `flip`

Turns like a card.

---

{{< slide id="transition-wipe" transition="wipe" >}}

# `wipe`

Reveals itself from the side.

---

{{< slide id="transition-iris" transition="iris" >}}

# `iris`

Opens like an old movie ending in reverse.

---

{{< slide id="transition-spin" layout="center" transition="spin" theme="synthwave" >}}

# `spin`

Breaking news! The newspaper spin is back.

---

{{< slide id="transition-bounce" layout="center" transition="bounce" theme="synthwave" >}}

# `bounce`

Drops in with a bounce.

---

{{< slide id="transition-swing" layout="center" transition="swing" theme="synthwave" >}}

# `swing`

Swings down on its hinges.

---

{{< slide id="transition-tv" layout="center" transition="tv" theme="terminal" >}}

# `tv`

Turns on like a cathode-ray tube.

---

{{< slide id="part-themes" layout="section" transition="iris" >}}

# Themes and colors

Five built-in palettes, fully overridable.

---

{{< slide id="themes" transition="fade" >}}

# Built-in themes

`dark` (default), `light`, `solarized`, `synthwave`, and `terminal`.

```toml
[params.powerslides]
  theme = "light"
```

Or per page in front matter (`theme: light`), or per slide:

```markdown
{{</* slide theme="solarized" */>}}
```

---

{{< slide id="theme-light" theme="light" transition="fade" >}}

# `light`

A clean palette for bright rooms.

| Token     | Role               |
| --------- | ------------------ |
| `primary` | Links and accents  |
| `muted`   | Secondary text     |

---

{{< slide id="theme-solarized" theme="solarized" transition="fade" >}}

# `solarized`

Warm and easy on the eyes.

{{< callout type="tip" >}}
Every color remains readable: text contrast is at least 4.5:1.
{{< /callout >}}

---

{{< slide id="theme-synthwave" theme="synthwave" layout="title" transition="zoom" >}}

# `synthwave`

## Neon glow included

---

{{< slide id="theme-terminal" theme="terminal" transition="tv" >}}

# `terminal`

```sh
$ hugo server
Web Server is available at http://localhost:1313/
```

---

{{< slide id="custom-colors" transition="fade" >}}

# Custom colors

Override any token in `hugo.toml` (or `colors` in front matter):

```toml
[params.powerslides.colors]
  primary = "#34d399"
  on-primary = "#022c22"
  background = "#0f172a"
```

Tokens: `background`, `surface`, `border`, `text`, `muted`, `primary`, `on-primary`, `accent`, `warning`, `code-background`, `code-text`.

For fonts or anything else, add stylesheets with `customCSS`.

---

{{< slide id="animations" transition="slide" >}}

# Animations

Animate items with simple CSS classes:

<ul>
  <li class="anim-fade">Fade animation</li>
  <li class="anim-up">Move upward</li>
  <li class="anim-zoom">Zoom animation</li>
</ul>

```html
<li class="anim-up">Move upward</li>
```

{{< notes >}}
Inline HTML requires `markup.goldmark.renderer.unsafe = true` in the site configuration.
{{< /notes >}}

---

{{< slide id="notes" transition="zoom" >}}

# Speaker notes

Speaker notes are written with the `notes` shortcode:

```markdown
{{</* notes */>}}
These notes are only visible to the presenter.
{{</* /notes */>}}
```

They remain synchronized with the current slide.

{{< notes >}}
Demonstrate how speaker notes can be used during a presentation without appearing on the slides.
{{< /notes >}}

---

{{< slide id="conclusion" layout="title" transition="zoom" >}}

# Thank you!

## Questions?

{{< notes >}}
Conclude the presentation and invite questions.
{{< /notes >}}
