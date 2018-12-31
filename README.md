# Trillo

### Hotel website made with flexbox

To start the project

- `npm run start`

## learning tips:

```css
&mdash; (—)

&copy; Ⓒ

:root {} == html {} with higher specificity

/* Using svg with xlink:href is going to work and show the sprite file
only on the web/local server */

/* add the local path of sprite + # + name of icon (use demo file) */
<button class="search__button">
    <svg class="search__icon">
        <use xlink:href="/img/sprite.svg#icon-magnifying-glass" />
    </svg>
</button>

/* currentColor */

div {
    color: red;
    border: 5px solid currentColor;
    box-shadow: 0 0 5px solid currentColor;
}

&__item {
        position: relative;

        &:not(:last-child){
            margin-bottom: .5rem;
        }
    }

  &__item::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 3px;
        background-color: var(--color-primary);
        // normal scale
        transform: scaleY(0);
        transform-origin: bottom; //default center
        transition: transform 1s;
    }

    /* You can add different setting for different properties */
    /* small line that become visible and the expands to the right side */
    &__item::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        // initially
        width: 3px;
        background-color: var(--color-primary);
        // normal scale
        transform: scaleY(0);
        transition: transform .2s,
            width .4s cubic-bezier(1,0,0,1) .2s;  /* this second .2s is the delay */
    }

    /* the z-index works onlly if we have specified the position */

    {
        position: relative;
        z-index: 10;

    }

    /* the element occupy the space it needs and the rest is calculated */
    {
        margin-right: auto
    }


```

- css custom properties (**css variables**): `--nameVariable`
- background-image: linear-gradient(to right bottom, var(--color-primary-light), var(--color-primary-dark));
- SVG (Scalable Vector Graphic) are better than Icon fonts: a way to write vector graphics with code. Use app
  [IcoMoon](https://icomoon.io/)
- sprite file
- fo svg `xlink:href` is deprecated in favor of simply `href`
- flexbox works with text as well
- The `:link` CSS pseudo-class represents an element that has not yet been visited. It matches every unvisited `<a>`, `<area>`, or `<link>` element that has an `href` attribute.
- currentColor: pick the current color reference in a class and when you assign currentColor as one of the value of the property it will show the refer color.

* CSS Masks:
  - mask-image
  - mask-size

The `:last-of-type` selector allows you to target the last occurence of an element within its container. It targets a particular type of element in a particular arrangement _with relation to similar siblings, not all siblings._

```css
.paragraph:not(:last-of-type) {
  margin-bottom: 2rem;
}
```

## Resources

- [jonasschmedtmann Github](https://github.com/jonasschmedtmann/advanced-css-course)
- [Trillo original Github project and solution](https://github.com/jonasschmedtmann/advanced-css-course/tree/master/Trillo)
- [IcoMoon](https://icomoon.io/)
- [cubic-bezier](http://cubic-bezier.com/#.17,.67,.83,.67)

## Live!

- [Check my project here!](https://happy-blackwell-trillo.netlify.com)
