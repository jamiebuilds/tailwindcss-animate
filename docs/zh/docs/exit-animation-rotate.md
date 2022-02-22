# Exit Animation Rotate

> Utilities for controlling the ending rotation of exit animations.

| Class          | Properties                  |
| -------------- | --------------------------- |
| `spin-out`     | `--tw-exit-rotate: 30deg;`  |
| `spin-out-0`   | `--tw-exit-rotate: 0deg;`   |
| `spin-out-1`   | `--tw-exit-rotate: 1deg;`   |
| `spin-out-2`   | `--tw-exit-rotate: 2deg;`   |
| `spin-out-3`   | `--tw-exit-rotate: 3deg;`   |
| `spin-out-6`   | `--tw-exit-rotate: 6deg;`   |
| `spin-out-12`  | `--tw-exit-rotate: 12deg;`  |
| `spin-out-45`  | `--tw-exit-rotate: 45deg;`  |
| `spin-out-90`  | `--tw-exit-rotate: 90deg;`  |
| `spin-out-180` | `--tw-exit-rotate: 180deg;` |

## Basic Usage

### Changing exit animation ending rotation

Set the ending rotation of an animation using the `spin-out-{amount}` utilities.

```html
<button class="animate-out spin-out ...">Button A</button>
<button class="animate-out spin-out-12 ...">Button B</button>
<button class="animate-out spin-out-45 ...">Button C</button>
<button class="animate-out spin-out-95 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:spin-out-90` to only apply the `spin-out-90` utility on hover.

```html
<div class="animate-bounce spin-out-45 hover:spin-out-90">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:spin-out-90` to apply the `spin-out-90` utility at only medium screen sizes and above.

```html
<div class="animate-bounce spin-out-45 md:spin-out-90">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind makes the entire default [rotate](https://tailwindcss.com/docs/rotate) available as animation scales. You can [customize your rotation](https://tailwindcss.com/docs/theme) by editing `theme.rotate` or `theme.extend.rotate` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            rotate: {
                175: "175deg",
            },
        },
    },
}
```

Alternatively, you can customize just your animation rotations by editing `theme.animationRotate` or `theme.extend.animationRotate` in your `tailwind.config.js` file.

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off animation scale value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="spin-out-[175deg]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
