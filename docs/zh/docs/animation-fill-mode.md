# Animation Fill Mode

> Utilities for controlling the fill mode of CSS animations.

| Class                 | Properties                        |
| --------------------- | --------------------------------- |
| `fill-mode-none`      | `animation-fill-mode: none;`      |
| `fill-mode-forwards`  | `animation-fill-mode: forwards;`  |
| `fill-mode-backwards` | `animation-fill-mode: backwards;` |
| `fill-mode-both`      | `animation-fill-mode: both;`      |

## Basic Usage

### Changing animation fill mode

Use the `fill-mode-{keyword}` utilities to control an element’s `animation-fill-mode`.

```html
<button class="animate-bounce fill-mode-none ...">Button A</button>
<button class="animate-bounce fill-mode-forwards ...">Button B</button>
<button class="animate-bounce fill-mode-backwards ...">Button C</button>
<button class="animate-bounce fill-mode-both ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:fill-mode-forwards` to only apply the `fill-mode-forwards` utility on hover.

```html
<div
    class="animate-bounce duration-300 fill-mode-backwards hover:fill-mode-forwards"
>
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:fill-mode-forwards` to apply the `fill-mode-forwards` utility at only medium screen sizes and above.

```html
<div
    class="animate-bounce duration-300 fill-mode-backwards md:fill-mode-forwards"
>
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind provides `animation-direction` utilities for all of the built-in browser keyword options. You can customize these values by editing `theme.animationDirection` or `theme.extend.animationDirection` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        extend: {
            animationDirection: {
                "forwards-backwards": "forwards, backwards",
            },
        },
    },
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-fill-mode` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="fill-mode-[forwards,backwards]">
    <!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
