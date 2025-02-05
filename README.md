# Unexpected Behavior of `calc()` with Percentages in CSS

This repository demonstrates an uncommon issue encountered when using the `calc()` function in CSS with percentage values.  The problem arises when attempting to subtract pixels from a percentage width without a defined parent width. The `calc()` function needs a concrete reference value to operate on, which is often not present if relying on content-based width determination.

The `bug.css` file shows the problematic code. The `bugSolution.css` offers a solution to make the calculation work as expected.

## Bug
The primary issue is that the percentage in `calc(50% - 10px)` is relative to the parent container's width. If the parent's width is not defined or is dynamically determined, the calculation can lead to unexpected results. The browser might interpret the percentage before the subtraction, resulting in inaccurate rendering.