# tailwind-css-sample
以下を参考にTailwindCSSに入門する  
https://tailwindcss.com/docs/installation

## Utility-First Fundamentals

[Utility-First Fundamentals - Tailwind CSS](https://tailwindcss.com/docs/utility-first)

TL;DR

- classいっぱい付与するのって、styleタグでCSS書くのと変わらなくない？
    - styleタグはマジックナンバーだらけの良くも悪くも自由なCSSになってしまう
    - TailwindCSSはconstrainedなutilityクラスを使うので、誰が作ってもそこそこ同じものが生まれる
- classが増えてくると保守性下がらない？
    - React, Vueなどでcomponent化する
    - @applyで部品化（TailwindCSSの機能）

## Handling Hover, Focus, and Other States

[Handling Hover, Focus, and Other States - Tailwind CSS](https://tailwindcss.com/docs/hover-focus-and-other-states)

TL;DR

- 疑似要素は`hover:xxx`で可能
- `odd`, `even` などもできる
- 他にも色々、、（書ききれません）

## Responsive Design

[Responsive Design - Tailwind CSS](https://tailwindcss.com/docs/responsive-design)

TL;DR

- `sm:w-32`などのようにprefix付きでclassを記述するだけで、レスポンシブデザインを実現できる
- 基本思想は「Working mobile-first」
    - `@media (min-width`はあるが`max-width`がないのがミソ
    - prefix付きのclassは全サイズに適用される
    - タブレット、PCブラウザ向けのcssはprefix付きで記述する必要がある
    - つまり、モバイル用cssを先に定義して、モバイル以上のサイズは後付けで上書きする

## Dark Mode

[Dark Mode - Tailwind CSS](https://tailwindcss.com/docs/dark-mode)

TL;DR

- tailwind.config.jsにて`darkMode: 'media', // or 'class’`で設定する
    - `media`なら、OSの設定に依存する
    - `class`なら、親クラスにclass=”dark”があるかどうかで判定する
    - マニュアルで可変にすることも可能


## ****Extracting classes with `@apply`**

[Reusing Styles - Tailwind CSS](https://tailwindcss.com/docs/reusing-styles#extracting-classes-with-apply)

TL;DR

- input.cssに以下を追記する

```css
@layer components {
    .card-text {
        @apply text-slate-500 dark:text-slate-400;
    }
}
```