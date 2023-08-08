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

[CodePen Demo](https://codepen.io/argyleink/full/OJBajxa)
Showcases blend modes and isolation usage.

Allows for progressive enhancement.

Crossfade happens by default, which helps create a more accesible transition and .

## Transition Morphs
The browser is given relations between data so that it re-uses elements.

### Demos

- [View Transitions Demo]()
Codepen showcasing animations during live edit.

- [View Transition Drag & Drop Demo]()
Animating drag and drop while remembering historical location.

- [Bento Radio Carousel]()
More remembering initial location; showcasing moving 

- [Animating a CSS Grid]()
Live editing/option changes

## @media annotation
Use customize media

## Customizing with CSS
PRovides the ability to customize the 'outgoing' and 'incoming' image.

### Demos
- [Text Replace Codepen]()
Interval goes through to replace previous image with new image - in this case it's characters.

- [Drag & Drop]()
Similar to above, but code insights show that the previously selected item/animation can be updated as the new selected animation can also be updated.
(Someone please reword this dear God)

- [Morphing Multi-State Button]()
Uses setInnerHtml to adjust transitions


## Further Customization with Only Children
When exiting or entering the stage with `:only-child`
Animation customization when there is not a pair to the item in question.

### Demos
- [IsotopJS-esque Transitions]()
Event listener for the value which adjust the display values of some elements as well as the grid transitions.

- [Input Number Changed]()
Number transitions as the number changes, combined with a number slider. Giving each individual element like the `$` or `,` character their own individual names allows for higher control of transitions.

## Recap
* Morphing
* Customizing old & new animations
* Customizing stage entrances/exits

[CodePen collections]()