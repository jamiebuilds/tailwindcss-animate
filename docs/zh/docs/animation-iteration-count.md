# Animation Iteration Count

> Utilities for controlling the iteration count of CSS animations.

| Class             | Properties                             |
| ----------------- | -------------------------------------- |
| `repeat-0`        | `animation-iteration-count: 0;`        |
| `repeat-1`        | `animation-iteration-count: 1;`        |
| `repeat-infinite` | `animation-iteration-count: infinite;` |

> **Note:** This is reusing the same classes as `transition-delay`, this may change in the future if it turns out to cause friction.

## Basic Usage

### Changing animation iteration count

Use the `repeat-{amount}` utilities to control an element’s `animation-iteration-count`.

```html
<button class="animate-bounce repeat-0 ...">Button A</button>
<button class="animate-bounce repeat-1 ...">Button B</button>
<button class="animate-bounce repeat-infinite ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:repeat-1` to only apply the `repeat-1` utility on hover.

```html
<div class="animate-bounce repeat-infinite hover:repeat-1">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:repeat-1` to apply the `repeat-1` utility at only medium screen sizes and above.

```html
<div class="animate-bounce repeat-infinite md:repeat-1">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind includes a handful of general purpose `animation-iteration-count` utilities. You can customize these values by editing `theme.animationIterationCount` or `theme.extend.animationIterationCount` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            animationIterationCount: {
                2: "2",
            },
        },
    },
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-iteration-count` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="repeat-[2]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
