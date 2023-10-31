---
# try also 'default' to start simple
theme: default
background: /assets/the_great_wave_off_the_coast_of_kanagawa.jpg
# apply any windi css classes to the current slide
class: "text-center"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
drawings:
  persist: false
# use UnoCSS
css: unocss
colorSchema: dark
---

# The new wave of Javascript frameworks - Solid.js

<style>
h1 {
  font-weight: 500;
  text-shadow: 4px 2px black !important;
}
</style>

<img class="absolute left-4 bottom-4" width="140" height="140" src="/assets/slides-url.svg" />

<h2 class="absolute right-4 bottom-4" style="font-weight: 500; text-shadow: 4px 2px black !important;">Speaker: Fabrizio A. Vitale</h2>

---
layout: image
image: /assets/brian-mcgowan-rCKIz0V7_Ok-unsplash.jpg
---

# Once upon a time...


<style>
h1 {
  text-shadow: 1px 1px black;
}
</style>

---

# The first rise of the Javascript frameworks

<v-click>

## jQuery 🏆

```js
Select2.prototype.render = function () {
  var $container = $(
    '<span class="select2 select2-container">' +
      '<span class="selection"></span>' +
      '<span class="dropdown-wrapper" aria-hidden="true"></span>' +
    '</span>'
  );

  $container.attr('dir', this.options.get('dir'));

  this.$container = $container;

  this.$container[0].classList
    .add('select2-container--' + this.options.get('theme'));

  Utils.StoreData($container[0], 'element', this.$element);

  return $container;
};
```

</v-click>

<style>
h2 {
  background-color: yellow;
  background-image: linear-gradient(45deg, yellow 10%, orange 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image-right
image: "/assets/rowell-heria-XFqzxqQja3g-unsplash.jpg"
---

# The coming of React

<v-clicks>

- Declarative
- Performant (compared to .innerHTML)
- Composable
- SSR!

</v-clicks>

---
layout: image
image: "/assets/jezael-melgoza-layMbSJ3YOE-unsplash.jpg"
---

<h1 class="text-pic">Today</h1>

---
layout: image-left
image: "/assets/alora-griffiths-E3wehabi_B4-unsplash.jpg"
---

# React is starting to show its limits

<v-clicks>

- Too many renders issue
- Lack of standards
- Hydration times

</v-clicks>

---
src: ./slides/solidjs.md
class: solidjs-slides
---

---

# Conclusions

## SolidJS

<v-clicks>

- Lightweight and fast runtime ⚡️
- Familiar DX for React developers
- Deceptively shallow learning curve

</v-clicks>

---
layout: two-cols
---

# Thank you!

<div class="left-col-content">

## Slides

- [https://next-wave-fw-solidjs.netlify.app/1](https://next-wave-fw-solidjs.netlify.app/1)
- [<uim-github /> source](https://github.com/fabrizio-vitale-deltatre/slides-next-wave-of-javascript-fw/tree/feat/update-slides-for-internal-talk)


## Demo apps

-  [https://next-wave-fw-react.netlify.app/](https://next-wave-fw-react.netlify.app/) - [<uim-github /> source](https://github.com/fabrizio-vitale-deltatre/next-frameworks-sample-app/tree/reactjs)
-  [https://next-wave-fw-solid.netlify.app/](https://next-wave-fw-solid.netlify.app/) - [<uim-github /> source](https://github.com/FaberVitale/next-frameworks-sample-app/tree/solidjs)
- [<uim-github /> react-tv source](https://github.com/fabrizio-vitale-deltatre/next-frameworks-sample-app/tree/reactjs-tv)
- [<uim-github /> solidjs-tv source](https://github.com/fabrizio-vitale-deltatre/next-frameworks-sample-app/tree/solidjs-tv)

## Speakers

- [Fabrizio A. Vitale](https://github.com/FaberVitale)

</div>

::right::

<div class="slide-links">
<img width="240" height="240" src="/assets/slides-url.svg" />
</div>

<style>
h1 {
  font-size: 3.5rem !important;
  font-weight: 500;
  margin-bottom: 2rem !important;
}

h2 {
  margin-top: 2rem !important;
  margin-bottom: 0.3rem;
}

.slide-links {
  padding: 4rem 0 0;
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
  gap: 1rem;
}

.left-col-content {
  font-size: 1rem;
}

</style>