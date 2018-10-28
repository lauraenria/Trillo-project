# Trillo

### Hotel website made with flexbox

To start the project

* `npm run start`

## learning tips:

```css
&mdash; (—)

:root {} == html {} with higher specificity

/* Using svg with xlink:href is going to work and show the sprite file 
only on the web/local server */
<button class="search__button">
    <svg class="search__icon">
        <use xlink:href="/img/sprite.svg#icon-magnifying-glass" />
    </svg>
</button>

```

* css custom properties (**css variables**): `--nameVariable`
* background-image: linear-gradient(to right bottom, var(--color-primary-light), var(--color-primary-dark));
* SVG (Scalable Vector Graphic) are better than Icon fonts: a way to write vector graphics with code. Use app
[IcoMoon](https://icomoon.io/)
* sprite file
* fo svg `xlink:href`is deprecated in favor of simply `href`
* flexbox works with text as well


## Resources
* [IcoMoon](https://icomoon.io/)

## Live!
* [Check my project here!](happy-blackwell-trillo.netlify.com)