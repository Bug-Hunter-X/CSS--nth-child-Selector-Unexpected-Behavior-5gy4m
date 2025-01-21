# CSS :nth-child Selector Bug

This repository demonstrates a common misunderstanding in using the CSS `:nth-child` selector, specifically concerning selecting every other element. The `bug.css` file contains the problematic code, while `bugSolution.css` provides the correct solution.

The issue arises from incorrectly using the `:nth-child` selector to target every other element. This is a frequent error because the starting index isn't always intuitive.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the unexpected styling of the list items.
4. Replace `bug.css` with `bugSolution.css` and observe the correct styling.

## Bug Analysis

The problem occurs because `:nth-child(2n)` selects even-indexed elements. To select every other element starting from the first, you need to use `:nth-child(2n+1)` which covers every odd index.

## Solution

Use `:nth-child(2n+1)` to style every other element starting from the first, while `:nth-child(2n)` will select even-indexed elements.  Understanding the `n` in `:nth-child(an+b)` is crucial. `a` represents the step, and `b` the offset.