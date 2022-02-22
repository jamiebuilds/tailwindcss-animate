# Exit Animation Scale

> Utilities for controlling the ending scale of exit animations.

| Class          | Properties               |
| -------------- | ------------------------ |
| `zoom-out`     | `--tw-exit-scale: 0;`    |
| `zoom-out-0`   | `--tw-exit-scale: 0;`    |
| `zoom-out-50`  | `--tw-exit-scale: .5;`   |
| `zoom-out-90`  | `--tw-exit-scale: .9;`   |
| `zoom-out-95`  | `--tw-exit-scale: .95;`  |
| `zoom-out-100` | `--tw-exit-scale: 1;`    |
| `zoom-out-105` | `--tw-exit-scale: 1.05;` |
| `zoom-out-110` | `--tw-exit-scale: 1.1;`  |
| `zoom-out-125` | `--tw-exit-scale: 1.25;` |
| `zoom-out-150` | `--tw-exit-scale: 1.5;`  |

## Basic Usage

### Changing exit animation ending scale

Set the ending scale of an animation using the `zoom-out-{amount}` utilities.

```html
<button class="animate-in zoom-out ...">Button A</button>
<button class="animate-in zoom-out-50 ...">Button B</button>
<button class="animate-in zoom-out-75 ...">Button C</button>
<button class="animate-in zoom-out-95 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:zoom-out-50` to only apply the `zoom-out-50` utility on hover.

```html
<div class="animate-bounce zoom-out-75 hover:zoom-out-50">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:zoom-out-50` to apply the `zoom-out-50` utility at only medium screen sizes and above.

```html
<div class="animate-bounce zoom-out-75 md:zoom-out-50">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind makes the entire default [scale](https://tailwindcss.com/docs/scale) available as animation scales. You can [customize your scale](https://tailwindcss.com/docs/theme) by editing `theme.scale` or `theme.extend.scale` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            scale: {
                175: "1.75",
            },
        },
    },
}
```

Alternatively, you can customize just your animation scales by editing `theme.animationScale` or `theme.extend.animationScale` in your `tailwind.config.js` file.

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off animation scale value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="zoom-out-[1.75]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
