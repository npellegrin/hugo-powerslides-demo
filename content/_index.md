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

Example:

```markdown
{{</* slide transition="zoom" */>}}
```

{{< notes >}}
Explain that transitions can be selected independently for each slide.
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

{{< notes >}}
Show how the columns shortcode arranges content side by side.
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
