# CSS Specificity Issue with Nested :hover

This repository demonstrates a common CSS specificity issue related to the `:hover` pseudo-class on nested elements.  The problem arises because the parent element's `:hover` style has higher specificity than the child element's `:hover` style, effectively overriding it.

The `bug.css` file contains the problematic CSS code.  The `bugSolution.css` file offers a solution to resolve the specificity conflict.

## How to reproduce the bug

1. Create an HTML file (e.g., `index.html`) containing the following structure:

```html
<div>
  <span>Hover over me!</span>
</div>
```

2. Link `bug.css` to your HTML file.

3. Observe that hovering over the inner `<span>` does not change its background color to orange as intended.

## Solution

The solution involves adjusting the CSS to ensure the child element's `:hover` style has sufficient specificity to override the parent's style.  See `bugSolution.css` for the corrected code.  This often involves using more specific selectors or the `!important` flag (though the latter is generally discouraged).