# Animation Delay

> Utilities for controlling the delay of CSS animations.

| Class        | Properties                 |
| ------------ | -------------------------- |
| `delay-75`   | `animation-delay: 75ms;`   |
| `delay-100`  | `animation-delay: 100ms;`  |
| `delay-150`  | `animation-delay: 150ms;`  |
| `delay-200`  | `animation-delay: 200ms;`  |
| `delay-300`  | `animation-delay: 300ms;`  |
| `delay-500`  | `animation-delay: 500ms;`  |
| `delay-700`  | `animation-delay: 700ms;`  |
| `delay-1000` | `animation-delay: 1000ms;` |

> **Note:** This is reusing the same classes as [`transition-delay`](https://tailwindcss.com/docs/transition-delay), this may change in the future if it turns out to cause friction.

## Basic Usage

### Changing animation delay

Use the `delay-{amount}` utilities to control an element’s `animation-delay`.

```html
<button class="animate-bounce delay-150 duration-300 ...">Button A</button>
<button class="animate-bounce delay-300 duration-300 ...">Button B</button>
<button class="animate-bounce delay-700 duration-300 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:delay-0` to only apply the `delay-0` utility on hover.

```html
<div class="animate-bounce duration-300 delay-150 hover:delay-0">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:delay-0` to apply the `delay-0` utility at only medium screen sizes and above.

```html
<div class="animate-bounce duration-300 delay-150 md:delay-0">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind provides `animation-delay` utilities for all of the built-in browser keyword options. You can customize these values by editing `theme.animationDelay` or `theme.extend.animationDelay` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            animationDelay: {
                "2s": "2s",
            },
        },
    },
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-delay` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="delay-[2s]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
