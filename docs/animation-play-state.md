# Animation Play State

> Utilities for controlling the play state of CSS animations.

| Class     | Properties                       |
| --------- | -------------------------------- |
| `running` | `animation-play-state: running;` |
| `paused`  | `animation-play-state: paused;`  |

## Basic Usage

### Changing animation play state

Use the `running` and `paused` utilities to control an element’s `animation-play-state`.

```html
<button class="animate-bounce running ...">Button B</button>
<button class="animate-bounce paused ...">Button A</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:running` to only apply the `running` utility on hover.

```html
<div class="animate-bounce paused hover:running">
  <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:running` to apply the `running` utility at only medium screen sizes and above.

```html
<div class="animate-bounce paused md:running">
  <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).
