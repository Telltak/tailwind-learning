In a [traditional CSS style](core-css.html), styling requires writing CSS seperately from the content

While using [tailwind utility classes](tailwind-css.html), we can attach a number of classes to content which will apply similar styling.

In the tailwind example, the `p`, `flex` and `shrink` utilities are used to control layout.
- `p` is used to define the amount of padding (0.25*unit rem), e.g. `p-6` is 1.5rem of padding, ~ 24px
- `flex` is used to define a wrapping flexbox
- `shrink` is used to control how an item in a flexbox may be allowed to shrink if needed. `shrink-0` prevents any shrinking while `shrink` will allow content to shrink.
    - In contrast, `grow` classes control if an item is allowed to grow to fill the flexbox. `grow-0` (exists by default) does not permit the element to grow. `grow` will allow the element to grow.

The `max-w-*` and `mx-*` classes define the width and centering of elements
- `max-w-*` defines the max width of an element.
    - The width is defined according to 0.25*unit rem, so `max-w-24` would be 6rem or 96px.
    - There are also defined values such as `max-w-sm` for values above 6rem to make the values "easier to guess"
    - `max-w-prose` provides a max width optimised for readability and adapts based on the font size
- `m?-*` defines margins. This has a number of variations
    - `mx-*` defines margins on the x axis
    - `my-*` defines margins on the y axis
    - `m-*` defines margins on all sides
    - `*-auto` allows an element to be centered on its defined axes

NOTE: Many elements can use the `hover:` prefix to apply an additional effect when the element is hovered over. For example, you can use `class="max-w-12 hover:max-w-sm"` to state that an element will normally have a maximum width of 3rem however when hovered would have a maximum width of 6rem.
