# Jamie's rules for clean, maintainable CSS and Javascript

## CSS rules

### No inline styles

For the love of god, please no. We can't style things consistently if there are
manual overrides all over the place.

### Grid system of 8px

All sizes should be multiples of 8px. That means padding, margin, widths, icons, everything.

Note: this can include 2 and 4px values.

### Single class selectors only

* Long selectors are slow - see http://csswizardry.com/2011/09/writing-efficient-css-selectors/
* Long selectors make specificity wars all but certain
* Long selectors make it hard to determine just from looking at the HTML what it will look like on the page.

### Rules should add properties, not override them

Each rule should only add the minimum that is needed. That way you need need to override
those properties with other rules. Example:

```css
.shopping-list-item {
    font-weight: bold
}

.shopping-list-item--margin-top {
    margin-top: 8px;
}
```

If you need the margin, you can add that class as well as the base one. Don't be afraid of
having multiple css classes - it's more descriptive if you're just looking at the HTML
anyway.
