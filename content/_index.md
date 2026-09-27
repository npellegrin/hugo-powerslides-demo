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

{{< fragments >}}
- Keyboard, clicker, and swipe navigation
- Step-by-step reveals
- Presenter mode with timer, next slide, and notes
- Ready-made layouts and thirteen transitions
- Color themes driven by CSS custom properties
- PDF export from the browser
{{< /fragments >}}

{{< notes >}}
Each item appears on the next key press. In this window, upcoming items are shown faded.
{{< /notes >}}

---

{{< slide id="navigation" transition="slide" >}}

# Navigation

| Keys                                      | Action                     |
| ----------------------------------------- | -------------------------- |
| <kbd>→</kbd> <kbd>Space</kbd> <kbd>Page Down</kbd> | Next step or slide  |
| <kbd>←</kbd> <kbd>Page Up</kbd>           | Previous step or slide     |
| <kbd>Home</kbd> <kbd>End</kbd>            | First or last slide        |
| <kbd>1</kbd> <kbd>2</kbd> … <kbd>Enter</kbd> | Go to slide number      |
| <kbd>O</kbd> or <kbd>Esc</kbd>            | Overview of all slides     |
| <kbd>F</kbd>                              | Fullscreen                 |
| <kbd>P</kbd>                              | Presenter window           |

On touch screens, swipe left or right.

---

{{< slide id="fragments" transition="slide" >}}

# Step-by-step reveals

{{< fragments style="zoom" >}}
- Wrap content in `fragments`
- Each item is one step
- Styles: `up`, `fade`, `zoom`, `highlight`
{{< /fragments >}}

```markdown
{{</* fragments style="zoom" */>}}
- Each item is one step
{{</* /fragments */>}}
```

{{< fragments style="highlight" >}}
Going back shows every step of the previous slide.
{{< /fragments >}}

{{< notes >}}
Any element with the `fragment` class also becomes a step, for example `<p class="fragment">`.
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

{{< slide id="background" background-image="/images/landscape.svg" transition="fade" >}}

# Backgrounds

Any slide can have a background image or color:

```markdown
{{</* slide background-image="/images/landscape.svg" background-dim="0.75" */>}}
{{</* slide background="#312e81" theme="synthwave" */>}}
```

The image is tinted with the theme background, so text stays readable.

---

{{< slide id="quote" layout="center" background="#312e81" theme="synthwave" transition="fade" >}}

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

Colors follow the slide theme. Highlight lines with `hl_lines`:

```js {hl_lines=[2]}
function goNext() {
  render(currentIndex + 1);
}
```

This requires classes instead of inline colors in `hugo.toml`:

```toml
[markup.highlight]
  noClasses = false
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

{{< slide id="math" transition="up" >}}

# Math

KaTeX renders formulas, inline like \(e^{i\pi} + 1 = 0\) or as blocks:

$$
\int_0^1 x^2 \, dx = \frac{1}{3}
$$

It loads only when a page contains math, from a pinned version checked with Subresource Integrity.

{{< notes >}}
Math needs the Goldmark passthrough extension in `hugo.toml`, so that Markdown leaves the LaTeX untouched.
{{< /notes >}}

---

{{< slide id="diagrams" transition="up" >}}

# Diagrams

```mermaid
flowchart LR
  A[Markdown] --> B[Hugo]
  B --> C[Slides]
  C --> D[PDF]
```

A `mermaid` code block becomes a diagram in the slide's theme colors.

---

{{< slide id="media" transition="up" >}}

# Video and embeds

{{< embed src="https://www.openstreetmap.org/export/embed.html?bbox=2.29%2C48.85%2C2.30%2C48.86&layer=mapnik" title="Map of the area around the Eiffel Tower" >}}

```markdown
{{</* video src="/videos/demo.mp4" autoplay="true" loop="true" */>}}
{{</* embed src="https://…" title="…" ratio="4/3" */>}}
```

{{< notes >}}
Autoplay videos start muted when the slide appears and pause when it is left. Embeds load only when their slide is current or next.
{{< /notes >}}

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

# Entrance animations

These play automatically when the slide appears:

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

{{< slide id="presenter" transition="fade" >}}

# Presenter mode

Press <kbd>P</kbd> to open the presenter window. It stays in sync with the audience window and shows:

- the current slide, with upcoming steps faded;
- the next slide;
- speaker notes;
- elapsed time, which can be paused or reset, and the clock.

---

{{< slide id="pdf" transition="fade" >}}

# Export to PDF

Print the presentation from the browser (<kbd>Ctrl</kbd> <kbd>P</kbd>) and choose **Save as PDF**:

- one page per slide, at the slide size;
- every step shown;
- controls and notes hidden.

{{< callout type="tip" >}}
Enable **Background graphics** in the print dialog if your browser asks. Chromium-based browsers give the best results.
{{< /callout >}}

---

{{< slide id="conclusion" layout="title" transition="zoom" >}}

# Thank you!

## Questions?

{{< notes >}}
Conclude the presentation and invite questions.
{{< /notes >}}
