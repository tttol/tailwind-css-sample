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