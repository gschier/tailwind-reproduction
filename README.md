# TailwindCSS no-underline bug

The bug:

- Define an element with both `underline` and `no-underline`
- In Tailwind < v4, the element is not underlined
- In Tailwind >= v4, the element is underlined

The resulting build for the CSS in this project contains the following, which are in the
incorrect order:

```css
.no-underline {
  text-decoration-line: none
}

.underline {
  text-decoration-line: underline
}

```
