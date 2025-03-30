# Problems

The problem about the spacing between inline-block display element it not stick together, even when the margin is zero.

## Solution #1: Change `font-size`

- Change the font-size of container into zero (`font-size:0`)
- Change the letter space (`letter-spacing: -1px`) is to fix Safari.

## Solution #2: Negative `margin`

- Using negative margin left (`margin-left: -1em`) for the first element;

Or:

- Using negative margin right (`margin-right: -1em`) for the last element;

## Resource

- <https://css-tricks.com/fighting-the-space-between-inline-block-elements/>
- <https://stackoverflow.com/questions/6213354/how-can-i-eliminate-spacing-between-inline-elements-in-css>
