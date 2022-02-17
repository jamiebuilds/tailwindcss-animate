# Animation Direction

> Utilities for controlling the timing function of CSS animations.

| Class         | Properties                                                 |
| ------------- | ---------------------------------------------------------- |
| `ease-linear` | `animation-timing-function: normal;`                       |
| `ease-in`     | `animation-timing-function: cubic-bezier(0.4, 0, 1, 1);`   |
| `ease-out`    | `animation-timing-function: cubic-bezier(0, 0, 0.2, 1);`   |
| `ease-in-out` | `animation-timing-function: cubic-bezier(0.4, 0, 0.2, 1);` |

> **Note:** This is reusing the same classes as [`transition-timing-function`](https://tailwindcss.com/docs/transition-timing-function), this may change in the future if it turns out to cause friction.

## Basic Usage

### Changing animation timing function

Use the `ease-{keyword}` utilities to control an element’s `animation-timing-function`.

```html
<button class="animate-bounce ease-linear ...">Button A</button>
<button class="animate-bounce ease-in ...">Button B</button>
<button class="animate-bounce ease-out ...">Button C</button>
<button class="animate-bounce ease-in-out ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:ease-in-out` to only apply the `ease-in-out` utility on hover.

```html
<div class="animate-bounce ease-linear hover:ease-in-out">
	<!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:ease-in-out` to apply the `ease-in-out` utility at only medium screen sizes and above.

```html
<div class="animate-bounce ease-linear md:ease-in-out">
	<!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind provides four general purpose `animation-timing-function` utilities. You can customize these values by editing `theme.animationTimingFunction` or `theme.extend.animationTimingFunction` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
	theme: {
		extend: {
			animationTimingFunction: {
				"in-expo": "cubic-bezier(0.95, 0.05, 0.795, 0.035)",
				"out-expo": "cubic-bezier(0.19, 1, 0.22, 1)",
			},
		},
	},
}
```

> **Note:** By default `animationTimingFunction` extends from `transitionTimingFunction`, by modifying `transitionTimingFunction` you also modify `animationTimingFunction`.

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-timing-function` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="ease-[cubic-bezier(0.95,0.05,0.795,0.035)]">
	<!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
