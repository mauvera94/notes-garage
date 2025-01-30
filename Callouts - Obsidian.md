---
title: Callouts - Obsidian
created: 2024-18-2
modification: 2025-01-01 19:07
description: 
updated: 2025-01-29
---

```markdown
> [!info] Custom titles
> Here's a callout block.
> It supports **Markdown**, [[Internal link|Wikilinks]], and [[Embed files|embeds]]!
> ![[Engelbart.jpg]]
```

> [!info] 
> Here's a callout block.
> It supports **Markdown**, [[Internal link|Wikilinks]]

### Title only callout

> [!tip] Title-only callout

```markdown
> [!tip] Title-only callout
```

### Foldable callouts

> [!faq]- Are callouts foldable?
> Yes! In a foldable callout, the contents are hidden when the callout is collapsed.
> Just add a dash after the callout

```markdown
> [!faq]- Foldable
> Lorem Ipsum
```

### Nested callouts

You can nest callouts in multiple levels.

> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.

```markdown
> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.
```


### Customize callouts
[callouts.css](hook://file/ozGOT2Zxt?p=Lm9ic2lkaWFuL3NuaXBwZXRz&n=callouts%2Ecss)

>[!code]-
>```css
> .callout[data-callout="idea"] {
>     --callout-color: 184,134,11;
>     --callout-icon: lightbulb;
> }
> 
> .callout[data-callout="caution"] {
>     --callout-color: 139,0,0;
>     --callout-icon: octagon-alert;
> }
> 
> .callout[data-callout="cooking"] {
>     --callout-color: 255,140,0;
>     --callout-icon: cooking-pot;
> }
> 
> .callout[data-callout="like"] {
>     --callout-color: 0,0,205;
>     --callout-icon: thumbs-up;
> }
> 
> .callout[data-callout="dislike"] {
>     --callout-color: 139,0,139;
>     --callout-icon: thumbs-down;
> }
> 
> .callout[data-callout="code"] {
>     --callout-color: 128,128,128;
>     --callout-icon: square-code;
> }
> 
> .callout[data-callout="formula"] {
>     --callout-color: 112,128,144;
>     --callout-icon: square-function;
>     text-align: center;
>     mjx-math {
>   font-size: 120%;
> }
> }
> 
> .callout[data-callout="book"] {
>     --callout-color: 70,130,180;
>     --callout-icon: book-open-text;
> }
> 
> .callout[data-callout="metric"] {
>     --callout-color: 128,128,0;
>     --callout-icon: gauge;
> }
>```




```css
.callout[data-callout="custom-question-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: lucide-alert-circle;
}
```

[Colors](https://www.rapidtables.com/web/color/RGB_Color.html)
[Icons](https://lucide.dev/icons/)

### Default callouts

> [!tip]
>  ```markdown
> >[!tip]
>```

> [!note]
>  ```markdown
> >[!note]
>```

> [!summary]
>  ```markdown
> >[!summary]
>```

> [!tldr]
>  ```markdown
> >[!tldr]
>```

> [!hint]
>  ```markdown
> >[!hint]
>```

> [!important]
>  ```markdown
> >[!important]
>```

> [!check]
>  ```markdown
> >[!check]
>```

> [!done]
>  ```markdown
> >[!done]
>```

> [!help]
>  ```markdown
> >[!help]
>```

> [!faq]
>  ```markdown
> >[!faq]
>```

> [!caution]
>  ```markdown
> >[!caution]
>```

> [!attention]
> ```markdown
> >[!attention]
>```


> [!fail]
> ```markdown
> >[!fail]
>```


> [!missing]
> ```markdown
> >[!missing]
>```

> [!error]
> ```markdown
> >[!error]
>```

> [!quote]
> ```markdown
> >[!quote]
>```

> [!example]
> ```markdown
> >[!example]
>```


### Custom callouts

> [!idea]
> ```markdown
> >[!idea]
>```

> [!metric]
> ```markdown
> >[!metric]
>``

> [!cooking]
> ```markdown
> >[!cooking]
>```

> [!like]
> ```markdown
> >[!like]
>```

> [!dislike]
> ```markdown
> >[!dislike]
>```

> [!code]
> ```markdown
> >[!code]
>```

> [!formula]
> ```markdown
> >[!formula]
>```

> [!book]
> ```markdown
> >[!book]
>```

> [!sheets]
> ```markdown
> >[!sheets]
>```
