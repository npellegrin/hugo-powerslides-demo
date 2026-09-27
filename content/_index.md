---
title: "Demonstration Presentation"
layout: "slides"
---

{{< slide id="title" transition="zoom" >}}

# Hugo PowerSlides

## A Markdown slide system for Hugo

A lightweight, static, and maintainable solution for creating presentations.

{{< notes >}}
Briefly introduce Hugo PowerSlides and explain that the presentation is written entirely in Markdown.
{{< /notes >}}

---

{{< slide id="features" transition="slide" >}}

# Features

<ul>
  <li class="anim-fade">Keyboard navigation</li>
  <li class="anim-up">Presenter mode</li>
  <li class="anim-zoom">Synchronized speaker notes</li>
  <li class="anim-fade">Slide transitions</li>
  <li class="anim-up">Simple Hugo integration</li>
  <li class="anim-fade">Columns and figure shortcodes</li>
</ul>

{{< notes >}}
Explain each feature briefly.

Keyboard navigation allows the presenter to move between slides without using the mouse.

Presenter mode provides access to speaker notes.

Animations and transitions can be added directly with CSS classes and shortcode parameters.
{{< /notes >}}

---

{{< slide id="markdown" transition="fade" >}}

# Markdown-based

Write your slides using familiar Markdown syntax, separating slides with `---`:

```markdown
{{</* slide id="example" transition="fade" */>}}

# My slide

Some content.

---

# Next slide
```

{{< notes >}}
Show that the presentation remains easy to read and edit directly in the source file.
{{< /notes >}}

---

{{< slide id="animations" transition="slide" >}}

# Animations

Animations can be added with simple CSS classes:

<ul>
  <li class="anim-fade">Fade animation</li>
  <li class="anim-up">Move upward</li>
  <li class="anim-zoom">Zoom animation</li>
</ul>

Example:

```markdown
<ul>
  <li class="anim-fade">Fade animation</li>
  <li class="anim-up">Move upward</li>
  <li class="anim-zoom">Zoom animation</li>
</ul>
```

{{< notes >}}
Explain that animations are intentionally implemented with simple CSS classes, making them easy to customize or extend.
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

{{< slide id="transitions" transition="fade" >}}

# Slide transitions

Each slide can define its own transition:

- `fade`
- `slide`
- `zoom`
- `up`

Example:

```markdown
{{</* slide transition="zoom" */>}}
```

{{< notes >}}
Explain that transitions can be selected independently for each slide. The next four slides demonstrate each one.
{{< /notes >}}

---

{{< slide id="transition-fade" transition="fade" >}}

# Fade transition

This slide fades in and out (`transition="fade"`).

```markdown
{{</* slide transition="fade" */>}}
```

{{< notes >}}
Demonstrate the fade transition between slides.
{{< /notes >}}

---

{{< slide id="transition-slide" transition="slide" >}}

# Slide transition

This slide slides in horizontally (`transition="slide"`).

```markdown
{{</* slide transition="slide" */>}}
```

{{< notes >}}
Demonstrate the slide transition between slides.
{{< /notes >}}

---

{{< slide id="transition-zoom" transition="zoom" >}}

# Zoom transition

This slide zooms in and out (`transition="zoom"`).

```markdown
{{</* slide transition="zoom" */>}}
```

{{< notes >}}
Demonstrate the zoom transition between slides.
{{< /notes >}}

---

{{< slide id="transition-up" transition="up" >}}

# Up transition

This slide moves upward into view (`transition="up"`).

```markdown
{{</* slide transition="up" */>}}
```

{{< notes >}}
Demonstrate the up transition between slides.
{{< /notes >}}

---

{{< slide id="columns" transition="slide" >}}

# Columns layout

{{< columns count="2" >}}

### Left column

Any Markdown content works here.

### Right column

Including lists, code, and images.

{{< /columns >}}

Example:

```markdown
{{</* columns count="2" */>}}

### Left column

Content.

### Right column

Content.

{{</* /columns */>}}
```

{{< notes >}}
Show how the columns shortcode arranges content side by side.
{{< /notes >}}

---

{{< slide id="figure" transition="zoom" >}}

# Figure shortcode

{{< figure src="/images/pipeline.svg" alt="Diagram showing Markdown flowing through Hugo into a PowerSlides presentation" caption="From Markdown to a static presentation, through Hugo." >}}

Example:

```markdown
{{</* figure src="/images/pipeline.svg" alt="..." caption="..." */>}}
```

{{< notes >}}
Show how the figure shortcode adds a captioned, responsive image to a slide.
{{< /notes >}}

---

{{< slide id="conclusion" transition="fade" >}}

# Conclusion

Hugo PowerSlides is:

- static;
- lightweight;
- maintainable;
- Markdown-based;
- compatible with Hugo;
- easy to customize.

## Thank you!

{{< notes >}}
Conclude the presentation and invite questions.
{{< /notes >}}
