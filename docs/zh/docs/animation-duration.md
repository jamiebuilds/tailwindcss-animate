# Animation Duration

> Utilities for controlling the duration of CSS animations.

| Class           | Properties                    |
| --------------- | ----------------------------- |
| `duration-75`   | `animation-duration: 75ms;`   |
| `duration-100`  | `animation-duration: 100ms;`  |
| `duration-150`  | `animation-duration: 150ms;`  |
| `duration-200`  | `animation-duration: 200ms;`  |
| `duration-300`  | `animation-duration: 300ms;`  |
| `duration-500`  | `animation-duration: 500ms;`  |
| `duration-700`  | `animation-duration: 700ms;`  |
| `duration-1000` | `animation-duration: 1000ms;` |

> **Note:** This is reusing the same classes as [`transition-duration`](https://tailwindcss.com/docs/transition-duration), this may change in the future if it turns out to cause friction.

## Basic Usage

### Changing animation duration

Use the `duration-{amount}` utilities to control an element’s `animation-duration`.

```html
<button class="animate-bounce duration-150 ...">Button A</button>
<button class="animate-bounce duration-300 ...">Button B</button>
<button class="animate-bounce duration-700 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:duration-0` to only apply the `duration-0` utility on hover.

```html
<div class="animate-bounce duration-300 hover:duration-0">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:duration-0` to apply the `duration-0` utility at only medium screen sizes and above.

```html
<div class="animate-bounce duration-150 md:duration-0">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind provides `animation-duration` utilities for all of the built-in browser keyword options. You can customize these values by editing `theme.animationDuration` or `theme.extend.animationDuration` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            animationDuration: {
                "2s": "2s",
            },
        },
    },
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-duration` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="duration-[2s]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
