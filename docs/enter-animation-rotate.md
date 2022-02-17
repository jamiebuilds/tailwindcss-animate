# Enter Animation Rotate

> Utilities for controlling the starting rotation of enter animations.

| Class         | Properties                   |
| ------------- | ---------------------------- |
| `spin-in`     | `--tw-enter-rotate: 30deg;`  |
| `spin-in-0`   | `--tw-enter-rotate: 0deg;`   |
| `spin-in-1`   | `--tw-enter-rotate: 1deg;`   |
| `spin-in-2`   | `--tw-enter-rotate: 2deg;`   |
| `spin-in-3`   | `--tw-enter-rotate: 3deg;`   |
| `spin-in-6`   | `--tw-enter-rotate: 6deg;`   |
| `spin-in-12`  | `--tw-enter-rotate: 12deg;`  |
| `spin-in-45`  | `--tw-enter-rotate: 45deg;`  |
| `spin-in-90`  | `--tw-enter-rotate: 90deg;`  |
| `spin-in-180` | `--tw-enter-rotate: 180deg;` |

## Basic Usage

### Changing enter animation starting rotations

Set the ending rotation of an animation using the `spin-in-{amount}` utilities.

```html
<button class="animate-in spin-in ...">Button A</button>
<button class="animate-in spin-in-12 ...">Button B</button>
<button class="animate-in spin-in-45 ...">Button C</button>
<button class="animate-in spin-in-90 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:spin-in-90` to only apply the `spin-in-90` utility on hover.

```html
<div class="animate-bounce spin-in-45 hover:spin-in-90">
	<!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:spin-in-90` to apply the `spin-in-90` utility at only medium screen sizes and above.

```html
<div class="animate-bounce spin-in-45 md:spin-in-90">
	<!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind makes the entire default [rotate](https://tailwindcss.com/docs/rotate) available as animation rotations. You can [customize your rotation](https://tailwindcss.com/docs/theme) by editing `theme.rotation` or `theme.extend.rotation` in your `tailwind.config.js` file.

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

If you need to use a one-off animation rotation value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="spin-in-[175deg]">
	<!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
