---
id: sq5b7d8hhtd5jdf8oxnfaxp
title: View Transitions
desc: ''
updated: 1691520423765
created: 1691519173033
---
# FLIP no more; Viva View Transitions - Adam Argyle
[Slides](seattlejs-view-transitions.netlify.app)

## Two Flavors
1. Same Page 
Already exists in the browser.
2. Across Pages
Work in progress for the browser.


## Same Page
Tell the browser you're about to mod the dom, and then do it. The browser will handle transitions between those states.

```js
// browser: 📸 (old)
document.startViewTransition(async () => {
  // me: does stuff to the page…
  // browser: 📸 (new)
})
```

[CodePen Demo 1](https://codepen.io/argyleink/full/OJBajxa)
[CodePen Demo 2]([https://codepen.io/argyleink/full/OJBajxa](https://codepen.io/bramus/full/xxQKvJP))
Showcases blend modes and isolation usage.

Allows for progressive enhancement.

```js
if (!document.startViewTransition)
    modifyPage()
else
  document.startViewTransition(async () =>
    modifyPage())
```

[Crossfade happens by default]([url](https://seattlejs-view-transitions.netlify.app/crossfade-is-a-great-default/)), which helps create a more accesible transition.

## Transition Morphs
The browser is given relations between data so that it re-uses elements.

### Demos

- [View Transitions - Grid Alignment](https://codepen.io/argyleink/full/NWOEvro)
Codepen showing how 1 line of CSS takes the previous demo that crossfades, into one that morphs positions.

- [View Transitions Demo](https://codepen.io/argyleink/full/QWBgEmK)
Codepen showcasing animations during live edit.

- [View Transition Drag & Drop Demo](https://codepen.io/argyleink/full/rNQZbLr)
Animating drag and drop while remembering historical location.

- [Bento Radio Carousel](https://codepen.io/argyleink/full/BaGrXmv)
More remembering initial location; showcasing moving 

- [Animating a CSS Grid](https://codepen.io/bramus/full/VwEXmqd)
Live editing/option changes (by @bramus)

## Don't forget prefers-reduced-motion

```css
@media (prefers-reduced-motion: no-preference) {
  .box {
    view-transition-name: box;
  }
}
```

## @media annotation
Use [custom media](https://drafts.csswg.org/mediaqueries-5/#at-ruledef-custom-media) to make it more succinct and within the design system.

```css
@media (--motionOK) {
  .box {
    view-transition-name: box;
  }
}
```

## Customizing with CSS
PRovides the ability to customize the 'outgoing' and 'incoming' image.

```css
::view-transition-old(box) {
  animation: var(--animation-scale-down);
}

::view-transition-new(box) {
  animation: var(--animation-slide-in-up);
}
```

### Demos
- [Text Replace Codepen](https://codepen.io/argyleink/full/KKBWwMr)
Interval goes through to replace previous image with new image - in this case it's characters.

- [Drag & Drop](https://codepen.io/argyleink/full/rNQZbLr)
Same demo as before, but upon closer inspection of the code, the animated gif was optimized to remain persistent and playing with the following CSS:

```css
::view-transition-old(yes-this-keeps-animating-during-morph) {
  display: none;
}
::view-transition-new(yes-this-keeps-animating-during-morph) {
  animation: none;
}
```

- [Morphing Multi-State Button](https://codepen.io/argyleink/full/ZEmLrze)
Uses setInnerHtml to put content into a multistep button, but uses the following CSS to squish the created images into the size of the fully rendered button:

```css
::view-transition-old(buy-btn),
::view-transition-new(buy-btn) {
  height: 100%;
  width: 100%;
}
```

[Watch Adam build this on YouTube]([url](https://www.youtube.com/watch?v=N2BKAKwGP6M))

## Further Customization with Only Children
When exiting or entering the stage with `:only-child`
Animation customization when there is not a pair to the item in question.

### Demos
- [IsotopJS-esque Transitions](https://codepen.io/argyleink/full/VwBKjwj)
Listens to change events in the gradio buttons and then simply uses `display: none` to hide non-matches. CSS grid does all the layout work and view transitions does all the transition work.

- [Input Number Changed](https://codepen.io/argyleink/full/jOQKdeW)
Number transitions as the number changes, combined with a number slider. Giving each individual element like the `$` or `,` character their own individual names allows for higher control of transitions.

## Browser Support
Chromium 111+ with a nice progressive enhancement story

## Docs
From Jake Archibald https://developer.chrome.com/docs/web-platform/view-transitions/

## Recap
* Morphing
* Customizing old & new animations
* Customizing stage entrances/exits

[All Demos in a CodePen Collections](https://codepen.io/collection/GoGOGK/)

## Morphull
The whole slideshow was built with view transitions, but not the JS api, rather the full page (MPA) api inside Chrome Canary.
Find the [Astro starter kit for Murphull here]([url](https://github.com/argyleink/morphull)https://github.com/argyleink/morphull)
