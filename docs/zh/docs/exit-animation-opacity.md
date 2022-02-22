# Exit Animation Opacity

> Utilities for controlling the ending opacity of exit animations.

| Class          | Properties                 |
| -------------- | -------------------------- |
| `fade-out`     | `--tw-exit-opacity: 0;`    |
| `fade-out-0`   | `--tw-exit-opacity: 0;`    |
| `fade-out-5`   | `--tw-exit-opacity: 0.05;` |
| `fade-out-10`  | `--tw-exit-opacity: 0.1;`  |
| `fade-out-20`  | `--tw-exit-opacity: 0.2;`  |
| `fade-out-25`  | `--tw-exit-opacity: 0.25;` |
| `fade-out-30`  | `--tw-exit-opacity: 0.3;`  |
| `fade-out-40`  | `--tw-exit-opacity: 0.4;`  |
| `fade-out-50`  | `--tw-exit-opacity: 0.5;`  |
| `fade-out-60`  | `--tw-exit-opacity: 0.6;`  |
| `fade-out-70`  | `--tw-exit-opacity: 0.7;`  |
| `fade-out-75`  | `--tw-exit-opacity: 0.75;` |
| `fade-out-80`  | `--tw-exit-opacity: 0.8;`  |
| `fade-out-90`  | `--tw-exit-opacity: 0.9;`  |
| `fade-out-95`  | `--tw-exit-opacity: 0.95;` |
| `fade-out-100` | `--tw-exit-opacity: 1;`    |

## Basic Usage

### Changing exit animation ending opacity

Set the ending opacity of an animation using the `fade-out-{amount}` utilities.

```html
<button class="animate-in fade-out ...">Button A</button>
<button class="animate-in fade-out-25 ...">Button B</button>
<button class="animate-in fade-out-50 ...">Button C</button>
<button class="animate-in fade-out-75 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:fade-out-50` to only apply the `fade-out-50` utility on hover.

```html
<div class="animate-bounce fade-out-25 hover:fade-out-50">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:fade-out-50` to apply the `fade-out-50` utility at only medium screen sizes and above.

```html
<div class="animate-bounce fade-out-25 md:fade-out-50">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind makes the entire default [opacity scale](https://tailwindcss.com/docs/opacity) available as animation opacities. You can [customize your opacity scale](https://tailwindcss.com/docs/theme) by editing `theme.opacity` or `theme.extend.opacity` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            opacity: {
                67: ".67",
            },
        },
    },
}
```

Alternatively, you can customize just your animation opacities by editing `theme.animationOpacity` or `theme.extend.animationOpacity` in your `tailwind.config.js` file.

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off animation opacity value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="fade-out-[.67]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
