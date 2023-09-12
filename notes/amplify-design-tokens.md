---
id: 1lamf6j027gow759p4q0sv8
title: Amplify Design Tokens
desc: ''
updated: 1694557781099
created: 1691520450864
---
### Creating a Design System using Design Tokens With Amplify - Erik Hanchett
[Talk on YouTube](https://www.youtube.com/watch?v=5wo8sD0gkYE)
co-written by Heather Bucknell from Amplify UI team

Erik Hanchett - Developer Advocate for Amplify
@ErikCH on Twitter

### Scenario
Multiple websites/ website with lots of components.

## Design Systems
A set of reusable standards and components which reinforce a brand's identity. Libraries like MaterialUI are more like component libraries.

### Contains:
- Style Guide
- Design Tokens

## Design Tokens
Values needed to construct and maintain a design system.

## Amplify UI with Tokens
Amplify UI - React components designed around accessible, themeable and performant based ideas with connection to the cloud.

Amplify UI is used as a design system. 
It provides a blueprint/skeleton component library that allows incorporation with provided designs and the ability to customize as you go.

**Blueprint/skeleton libraries** are intended to have core functionality but the design is left up the respective team.

**A design system should not limit your creativity** or prevent you from being able to do what you want to do.

## Creating Your Own Design System
Should you? It depends on your situation.
 - What resources already exist within your company?

 ## Using Design Tokens
 * Make them re-usable & extendable
 * Designer friendly
 * Utilize tooling like Figma or Sketch

 Anatomy: `[namespace] [sub_namespace] [scale]`
 The design tokens boil down to custom CSS properties.

 [Amplify UI Design Tokens Spec](ui.docs.amplify.aws/react/theming)

 ## Creating a Custom Theme
 1. Create a Theme Object
 2. Something-something Amplify UI

 ex: 
 `export const summerTheme: Theme = {`
    `name: "summerTheme",`
    `tokens: {`
        `colors: { * *css item here* * }`
    `}`
`}`

### Mobile?
Breakpoints can be specified in the theme object instead of declaring in multiple locations.

## Takeaway
If you don't have a design system - make a design system. This prevents inconsistencies.

If you do - learn the design tokens in your system and identify where to use them.

There's no tokens? - Add them!
Is your design consistent from front to back? - Audit and put those items in the backlog.

Follow the best practices defined in your design system and style guide.