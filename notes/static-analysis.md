---
id: d7w2zpv4ukha5bltqxd6q7j
title: Static Analysis
desc: ''
updated: 1694555476965
created: 1691527484192
---
# Static Analysis: Don't Fear the Linter! - Josh Goldberg
[Slides](https://onedrive.live.com/view.aspx?resid=D699ACCFCBD51CF5!1028281&ithint=file%2cpptx&authkey=!ACxCyVcuS7lZvSs)
[Talk on YouTube](https://www.youtube.com/watch?v=qiDzxvdKt-Y)

Josh Goldberg - [Speaking Schedule](https://www.joshuakgoldberg.com/speaking/#2023)

## Moving past the FUD
(Fear, Uncertainty, Doubt)

# Static Analysis
Scrutinizes your code without running it.

## Common forms of Static Analysis
1. Formatters
2. Linters
3. Type Checkers (TypeScript)

### 1.Formatters
A formatter is a tool that looks at the code and reformats it *without* changing logic or breaking code.

Packages like Prettier `npm install prettier --save-dev` or `npx prettier . --write`
[Template typescript package]()

Recommends: set `editor.formatOnSave": true`

### 2. Linters
A tool that runs a set of discrete checks (rules) on your code. The checks are discreet and don't touch each other, and may contain an optional fix.

Example: Eslint can notify of new JavaScript methods and fixes.
Eslint uses a `.eslintrc.js` config file 
Recommends: 
* Set package.json settings to fail build on 0 warnings
* Auto set linter to fix things on save

#### Disable a lint rule: `// eslint-disable-next-line no-console`
Disables the next line.

> STOP USING ESLINT FOR FORMATTING!
Use a separate formatter for formatting!

### 3. Type Checkers (yay TypeScript!)
TypeScript describes your values' intent, while JavaScript only describes your value

Uses a `tsconfig.json` config file

TypeScript
1. Language Service
Program that runs the type checker.
2. Compiler
    Transpiler and type checker
3. Type Checker
4. Programming Language

#### Life Without Type Checking
Questions on what type of value is being passed through - if this changes, what will break in 5 years?

**Recommends**:
Set `strict:true` - Be informed of all of the issues

FYI: Frameworks usually write a type config for you.

Adjust ESLint rules to always show as yellow 'warn' squigglies instead of all red.
"eslint.rules.customizations": { "rule": *, "severity": "warn"}

### Eslint Parser
Tells ESLint how to parse TypeScript / read TypeScript syntax

## Type-checked Linting
Detect Incorrect Async Code

## TLDR; 
1. Make sure you're using a formatter, linter AND type checker
2. Use the recommended lint configs for your langauge, frameworks
3. Check the [template-typescript-node-package](https://github.com/JoshuaKGoldberg/template-typescript-node-package)
4. Check dustispecker/awesome-eslint for great ESLint configs & plugins

## Resources
* prettier.io
* eslint.org
* typescriptlang.org
* typescript-eslint.io