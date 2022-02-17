# Exit Animations

> Utilities for creating exit animations.

| Class         | Properties                                                                                                                                                                                            |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `animate-out` | `animation-name: exit;`<br>`animation-duration: 150ms;`<br>`--tw-exit-opacity: initial;`<br>`--tw-exit-scale: initial;`<br>`--tw-exit-translate-x: initial;`<br>`--tw-exit-translate-y: initial;`<br> |

## Basic Usage

### Adding exit animations

To give an element an exit animation, use the `animate-out` utility, in combination with some [`fade-out`](/docs/exit-animation-scale.md), [`spin-out`](/docs/exit-animation-rotate.md), [`zoom-out`](/docs/exit-animation-scale.md), and [`slide-out-from`](/docs/exit-animation-translate.md) utilities.

```html
<button class="animate-out fade-out ...">Button A</button>
<button class="animate-out spin-out ...">Button B</button>
<button class="animate-out zoom-out ...">Button C</button>
<button class="animate-out slide-out-from-top ...">Button D</button>
<button class="animate-out slide-out-from-left ...">Button E</button>
```

### Adding multiple exit animations

You can apply multiple exit animations at the same time as long as they apply to different properties.

```html
<button class="animate-out fade-out zoom-out ...">Button A</button>
<button class="animate-out slide-out-from-top slide-out-from-left ...">
	Button B
</button>
<button
	class="animate-out fade-out zoom-out slide-out-from-top slide-out-from-left ..."
>
	Button C
</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:animate-out` to only apply the `animate-out` utility on hover.

```html
<div class="hover:animate-out ...">
	<!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:animate-out` to apply the `animate-out` utility at only medium screen sizes and above.

```html
<div class="md:animate-out ...">
	<!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).
