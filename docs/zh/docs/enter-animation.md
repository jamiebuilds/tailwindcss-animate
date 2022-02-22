# Enter Animations

> Utilities for creating enter animations.

| Class        | Properties                                                                                                                                                                                                                                     |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `animate-in` | `animation-name: enter;`<br>`animation-duration: 150ms;`<br>`--tw-enter-opacity: initial;`<br>`--tw-enter-scale: initial;`<br>`--tw-enter-translate-x: initial;`<br>`--tw-enter-translate-y: initial;`<br> |

## Basic Usage

### Adding enter animations

To give an element an enter animation, use the `animate-in` utility, in combination with some [`fade-in`](/docs/enter-animation-scale.md), [`spin-in`](/docs/enter-animation-rotate.md), [`zoom-in`](/docs/enter-animation-scale.md), and [`slide-in-from`](/docs/enter-animation-translate.md) utilities.

```html
<button class="animate-in fade-in ...">Button A</button>
<button class="animate-in spin-in ...">Button B</button>
<button class="animate-in zoom-in ...">Button C</button>
<button class="animate-in slide-in-from-top ...">Button D</button>
<button class="animate-in slide-in-from-left ...">Button E</button>
```

### Adding multiple enter animations

You can apply multiple enter animations at the same time as long as they apply to different properties.

```html
<button class="animate-in fade-in zoom-in ...">Button A</button>
<button class="animate-in slide-in-from-top slide-in-from-left ...">
    Button B
</button>
<button
    class="animate-in fade-in zoom-in slide-in-from-top slide-in-from-left ..."
>
    Button C
</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:animate-in` to only apply the `animate-in` utility on hover.

```html
<div class="hover:animate-in ...">
    <!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:animate-in` to apply the `animate-in` utility at only medium screen sizes and above.

```html
<div class="md:animate-in ...">
    <!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).
