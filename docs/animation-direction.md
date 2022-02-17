# Animation Direction

> Utilities for controlling the direction of CSS animations.

| Class                         | Properties                                |
| ----------------------------- | ----------------------------------------- |
| `direction-normal`            | `animation-direction: normal;`            |
| `direction-reverse`           | `animation-direction: reverse;`           |
| `direction-alternate`         | `animation-direction: alternate;`         |
| `direction-alternate-reverse` | `animation-direction: alternate-reverse;` |

## Basic Usage

### Changing animation direction

Use the `direction-{keyword}` utilities to control an element’s `animation-delay`.

```html
<button class="animate-bounce direction-normal ...">Button A</button>
<button class="animate-bounce direction-reverse ...">Button B</button>
<button class="animate-bounce direction-alternate ...">Button C</button>
<button class="animate-bounce direction-alternate-reverse ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:direction-normal` to only apply the `direction-normal` utility on hover.

```html
<div class="animate-bounce duration-300 delay-150 hover:direction-normal">
	<!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:direction-normal` to apply the `direction-normal` utility at only medium screen sizes and above.

```html
<div class="animate-bounce duration-300 delay-150 md:direction-normal">
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
				"normal-reverse": "normal, reverse",
			},
		},
	},
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-direction` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="direction-[normal,reverse]">
	<!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
