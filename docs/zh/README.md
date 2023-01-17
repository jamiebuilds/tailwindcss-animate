# `tailwindcss-animate`

> 一个用于构建精美动画的Tailwind CSS插件

```html
<！-- 添加淡入淡出和缩放出现效果的动画——>
<div class="animate-in fade-in zoom-in">...</div>

<!-- 添加滑向左上方退出的动画-->
<div class="animate-out slide-out-to-top slide-out-to-left">...</div>

<!-- 控制动画持续时间 -->
<div class="... duration-300">...</div>

<!-- 控制动画延迟 -->
<div class="... delay-150">. 。</div>

<!-- 更多其他动画效果！ -->
```

## 安装

Install the plugin from npm:

```sh
npm install -D tailwindcss-animate
```

之后将插件添加到您的 `tailwind.config.js` 文件：

```js
// @filename tailwind.config.js
module.exports = {
    theme: {
        // ...
    },
    plugins: [
        require("tailwindcss-animate"),
        // ...
    ],
}
```

## 文档

- [基本用法](#basic-usage)
  - [更改动画延迟](#changing-animation-delay)
  - [更改动画方向](#changing-animation-direction)
  - [更改动画持续时间](#changing-animation-duration)
  - [更改动画填充模式](#changing-animation-fill-mode)
  - [更改动画重复次数](#changing-animation-iteration-count)
  - [更改动画播放状态](#changing-animation-play-state)
  - [更改动画时序方式](#changing-animation-timing-function)
  - [减少动效](#prefers-reduced-motion)
- [进入以及推出动画](#enter-and-exit-animations)
  - [添加进入动画](#adding-enter-animations)
  - [添加退出动画](#adding-exit-animations)
  - [更改进入动画时的不透明度](#changing-enter-animation-starting-opacity)
  - [更改进入动画时的旋转](#changing-enter-animation-starting-rotation)
  - [更改进入动画时的缩放](#changing-enter-animation-starting-scale)
  - [更改进入动画时的变换](#changing-enter-animation-starting-translate)
  - [更改退出动画时的不透明度](#changing-exit-animation-ending-opacity)
  - [更改退出动画时的旋转](#changing-exit-animation-ending-rotation)
  - [更改退出动画时的缩放](#changing-exit-animation-ending-scale)
  - [更改退出动画时的变换](#changing-exit-animation-ending-translate)

### 基本用法

#### 更改动画延迟

使用 `delay-{amount}` 标签控制元素的 `animation-delay`.

```html
<button class="animate-bounce delay-150 duration-300 ...">Button A</button>
<button class="animate-bounce delay-300 duration-300 ...">Button B</button>
<button class="animate-bounce delay-700 duration-300 ...">Button C</button>
```

查看更多与 [animation delay](/docs/animation-delay.md) 相关的文档

#### 更改动画方向

使用 `direction-{keyword}` 标签控制元素的`animation-delay`.

```html
<button class="animate-bounce direction-normal ...">Button A</button>
<button class="animate-bounce direction-reverse ...">Button B</button>
<button class="animate-bounce direction-alternate ...">Button C</button>
<button class="animate-bounce direction-alternate-reverse ...">Button C</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 更改动画持续时间

使用 `delay-{amount}` 标签控制元素的 `animation-delay`.

```html
<button class="animate-bounce duration-150 ...">Button A</button>
<button class="animate-bounce duration-300 ...">Button B</button>
<button class="animate-bounce duration-700 ...">Button C</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 更改动画不播放时要应用到元素的样式（animation-fill-mode）

使用 `direction-{keyword}` 标签控制元素的`animation-delay`.

```html
<button class="animate-bounce fill-mode-none ...">Button A</button>
<button class="animate-bounce fill-mode-forwards ...">Button B</button>
<button class="animate-bounce fill-mode-backwards ...">Button C</button>
<button class="animate-bounce fill-mode-both ...">Button C</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 更改动画重复次数

使用 `delay-{amount}` 标签控制元素的 `animation-delay`.

```html
<button class="animate-bounce repeat-0 ...">Button A</button>
<button class="animate-bounce repeat-1 ...">Button B</button>
<button class="animate-bounce repeat-infinite ...">Button C</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 更改动画播放状态

使用 `direction-{keyword}` 标签控制元素的`animation-delay`.

```html
<button class="animate-bounce running ...">Button B</button>
<button class="animate-bounce paused ...">Button A</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 更改动画速度曲线

使用 `direction-{keyword}` 标签控制元素的`animation-delay`.

```html
<button class="animate-bounce ease-linear ...">Button A</button>
<button class="animate-bounce ease-in ...">Button B</button>
<button class="animate-bounce ease-out ...">Button C</button>
<button class="animate-bounce ease-in-out ...">Button C</button>
```

查看更多[animation direction](/docs/animation-direction.md)相关的文档

#### 减少运动媒体查询

如果用户指定他们喜欢减少动作， 您可以使用 `motion-safe` 和 `motion-reduc` 变量来有条件地应用动画和过渡：

```html
<button class="motion-safe:animate-bounce ...">Button B</button>
```

### 进入以及退出动画

### 添加进入动画

要给元素定义进入动画，请使用 `animate-in` ，并结合一些 [`fade-in`](/docs/enter-animation-scale.md), [`spin-in`](/docs/enter-animation-rotate.md) [`zoom-in`](/docs/enter-animation-scale.md), 和 [`slide-in-from`](/docs/enter-animation-translate.md)

```html
<button class="animate-in fade-in ...">Button A</button>
<button class="animate-in spin-in ...">Button B</button>
<button class="animate-in zoom-in ...">Button C</button>
<button class="animate-in slide-in-from-top ...">Button D</button>
<button class="animate-in slide-in-from-left ...">Button E</button>
```

Learn more in the [enter animation](/docs/enter-animation.md) documentation.

### Adding exit animations

To give an element an exit animation, use the `animate-out` utility, in combination with some [`fade-out`](/docs/exit-animation-scale.md), [`spin-out`](/docs/exit-animation-rotate.md), [`zoom-out`](/docs/exit-animation-scale.md), and [`slide-out-from`](/docs/exit-animation-translate.md) utilities.

```html
<button class="animate-out fade-out ...">Button A</button>
<button class="animate-out spin-out ...">Button B</button>
<button class="animate-out zoom-out ...">Button C</button>
<button class="animate-out slide-out-from-top ...">Button D</button>
<button class="animate-out slide-out-from-left ...">Button E</button>
```

Learn more in the [exit animation](/docs/exit-animation.md) documentation.

#### Changing enter animation starting opacity

Set the starting opacity of an animation using the `fade-in-{amount}` utilities.

```html
<button class="animate-in fade-in ...">Button A</button>
<button class="animate-in fade-in-25 ...">Button B</button>
<button class="animate-in fade-in-50 ...">Button C</button>
<button class="animate-in fade-in-75 ...">Button C</button>
```

Learn more in the [enter animation opacity](/docs/enter-animation-opacity.md) documentation.

#### Changing enter animation starting rotation

Set the starting rotation of an animation using the `spin-in-{amount}` utilities.

```html
<button class="animate-in spin-in-1 ...">Button A</button>
<button class="animate-in spin-in-6 ...">Button B</button>
<button class="animate-in spin-in-75 ...">Button C</button>
<button class="animate-in spin-in-90 ...">Button C</button>
```

Learn more in the [enter animation rotate](/docs/enter-animation-rotate.md) documentation.

#### Changing enter animation starting scale

Set the starting scale of an animation using the `zoom-in-{amount}` utilities.

```html
<button class="animate-in zoom-in ...">Button A</button>
<button class="animate-in zoom-in-50 ...">Button B</button>
<button class="animate-in zoom-in-75 ...">Button C</button>
<button class="animate-in zoom-in-95 ...">Button C</button>
```

Learn more in the [enter animation scale](/docs/enter-animation-scale.md) documentation.

#### Changing enter animation starting translate

Set the starting translate of an animation using the `slide-in-from-{direction}-{amount}` utilities.

```html
<button class="animate-in slide-in-from-top ...">Button A</button>
<button class="animate-in slide-in-from-bottom-48 ...">Button B</button>
<button class="animate-in slide-in-from-left-72 ...">Button C</button>
<button class="animate-in slide-in-from-right-96 ...">Button C</button>
```

Learn more in the [enter animation translate](/docs/enter-animation-translate.md) documentation.

#### Changing exit animation ending opacity

Set the ending opacity of an animation using the `fade-out-{amount}` utilities.

```html
<button class="animate-out fade-out ...">Button A</button>
<button class="animate-out fade-out-25 ...">Button B</button>
<button class="animate-out fade-out-50 ...">Button C</button>
<button class="animate-out fade-out-75 ...">Button C</button>
```

Learn more in the [exit animation opacity](/docs/exit-animation-opacity.md) documentation.

#### Changing exit animation ending rotation

Set the ending rotation of an animation using the `spin-out-{amount}` utilities.

```html
<button class="animate-out spin-out-1 ...">Button A</button>
<button class="animate-out spin-out-6 ...">Button B</button>
<button class="animate-out spin-out-75 ...">Button C</button>
<button class="animate-out spin-out-90 ...">Button C</button>
```

Learn more in the [exit animation rotate](/docs/exit-animation-rotate.md) documentation.

#### Changing exit animation ending scale

Set the ending scale of an animation using the `zoom-out-{amount}` utilities.

```html
<button class="animate-out zoom-out ...">Button A</button>
<button class="animate-out zoom-out-50 ...">Button B</button>
<button class="animate-out zoom-out-75 ...">Button C</button>
<button class="animate-out zoom-out-95 ...">Button C</button>
```

Learn more in the [exit animation scale](/docs/exit-animation-scale.md) documentation.

#### Changing exit animation ending translate

Set the ending translate of an animation using the `slide-out-to-{direction}-{amount}` utilities.

```html
<button class="animate-out slide-out-to-top ...">Button A</button>
<button class="animate-out slide-out-to-bottom-48 ...">Button B</button>
<button class="animate-out slide-out-to-left-72 ...">Button C</button>
<button class="animate-out slide-out-to-right-96 ...">Button C</button>
```

Learn more in the [exit animation translate](/docs/exit-animation-translate.md) documentation.
