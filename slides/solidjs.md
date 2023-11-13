---
layout: image
image: "/assets/solid-logo-full.svg"
---

<style>
  [layout="image"] {
    background-size: contain !important;
  }
</style>

---
layout: two-cols
---

<h1>What's Solid.js?</h1>

<v-clicks>

- Solid.js is a lightweight and declarative reactive library for building user interfaces.
- 5+ years of developement.
- Maintained by [Ryan Carniato](https://github.com/ryansolid).

</v-clicks>

::right::

<img class="solid-logo" width="200" height="200" src="/assets/solid-logo.svg" />

<style>
  .solid-logo {
    margin: 5rem auto 0;
  }
</style>   


---
layout: two-cols
---

<h1 class="no-margin">Features</h1>

- JSX templating
- Component based
- Fine-grained reactivity model
- Familiar api and DX for React developers
- Unidirectional data flow
- Client & Server side rendering
- Typescript support
- [Code-splitting - lazy(import(...))](https://www.solidjs.com/tutorial/async_lazy)
- [Suspense (render-as-you-fetch)](https://www.solidjs.com/tutorial/async_suspense)
- [Transitions](https://www.solidjs.com/tutorial/async_transitions)

::right::

<img class="solid-logo" width="200" height="200" src="/assets/solid-logo.svg" />

<style>
  .solid-logo {
    margin: 5rem auto 0;
  }
</style>   

---
layout: center
---

# 🍎 to 🍏 performance comparison

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">🍎 to 🍏 performance comparison / 1</h1>

<div class="mt-5 side-blocks">

## React 

```bash {4}
[...]
index.html                1.58 KiB
assets/index.f8c30131.css 51.87 KiB / gzip: 10.26 KiB
assets/index.d60afae4.js  141.33 KiB / gzip: 45.79 KiB
```

- [website](https://next-wave-fw-react.netlify.app?q=Javascript)
- [<uim-github /> - source](https://github.com/FaberVitale/next-frameworks-sample-app/blob/8a88dfa74d9e12076d120807f79317fd45445cbc/src/App.tsx)
- **[webpagetest.org test](https://www.webpagetest.org/result/231031_BiDcK5_6EM/)**

</div>

::right::

<div class="mt-5 side-blocks">

## Solid.js

```bash {4}
[...]
index.html                1.58 KiB
assets/index.f8c30131.css 51.87 KiB / gzip: 10.26 KiB
assets/index.54c59109.js  13.62 KiB / gzip: 5.75 KiB
```

- [website](https://next-wave-fw-solid.netlify.app?q=Javascript)
- [<uim-github /> - source](https://github.com/FaberVitale/next-frameworks-sample-app/blob/b79aa7c06c09d888d91e2edbb1f023cfff99323a/src/App.tsx)
- **[webpagetest.org test](https://www.webpagetest.org/result/231031_AiDcRB_6YK/)**

</div>

<style>
  .side-blocks {
    display: flex;
    flex-flow: column nowrap;
    gap: 1.5rem;
  }
</style>

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">🍎 to 🍏 performance comparison / 2</h1>

<div class="mt-16 side-blocks text-2xl">

- **[js-framework-benchmark results](https://krausest.github.io/js-framework-benchmark/2023/table_chrome_118.0.5993.70.html)**
- [<uim-github /> - source](https://github.com/krausest/js-framework-benchmark)

</div>

::right::

<img style="position: absolute; top: -140px; clip-path: polygon(0 24%, 100% 24%, 100% 80%, 0 80%);" src="/assets/mahdi-bafande.jpg" />

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">Performance: 🍎 to 🍏 comparison / 3</h1>

<div class="mt-5 side-blocks">

## React webOs TV app

[<uim-github /> - source](https://github.com/fabrizio-vitale-deltatre/next-frameworks-sample-app/blob/reactjs-tv/src/App.tsx)

### Tested on

-  LG Smart TV, webOs 4.9.7-17
-  Simulator 1.3.0

</div>

::right::

<div class="mt-5 side-blocks">

## Solid.js webOs TV app

[<uim-github /> - source](https://github.com/fabrizio-vitale-deltatre/next-frameworks-sample-app/blob/solidjs-tv/src/App.tsx)

### Tested on

-  LG Smart TV, webOs 4.9.7-17
-  Simulator 1.3.0

</div>

---
layout: center
---

# Why is Solidjs fast?

--- 
layout: two-cols
---

<style>
.solid-perf-img-wrapper {
  height: 100%;
  width: 100%;
}

.solid-perf-img {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%
}
</style>

<h1 class="solidjs-two-cols-heading">Solid.js is fast</h1>

<div class="solidjs-click-list mt-8">
<v-clicks>

- It's **just** [7.3KB min+gzip](https://bundlephobia.com/package/solid-js@1.5.1).
- At the top of UI speed and memory utilization [benchmarks](https://krausest.github.io/js-framework-benchmark/index.html).
- Blazing fast server-side rendering, based on string interpolation.
- No Virtual Dom, [components render once](https://www.solidjs.com/guides/reactivity).

</v-clicks>
</div>

::right::

<div class="absolute top-0 solid-perf-img-wrapper solid-js-bg2">
  <img class="solid-perf-img" src="/assets/christian-englmeier-J7EUjSlNQtg-unsplash.jpg" logo="speed" aria-hidden="true" />
</div>

---

<style>
  .react-recon-pos {
    right: 3rem;
    top: 12rem;
  }
  .react-recon-count {
    right: 20rem;
    top: 10.2rem;
    font-size: 1.4rem;
  }
</style>

<h1 class="absolute">React reconciliation</h1>

<div class="relative" style="padding: 2.5rem 1rem 1rem">
  <div class="absolute react-recon-count">
    count: <s>7</s>=><strong style="color: inherit;">8</strong>
  </div>
  <pre><code class="absolute react-recon-pos">setCount(n => n + 1);</code></pre>
 <img src="/assets/react-reconciliation.svg" alt="react reconciliation" />
</div>

---

<style>
  .react-recon-pos {
    right: 3rem;
    top: 12rem;
  }

  .react-recon-count {
    right: 20rem;
    top: 10.2rem;
    font-size: 1.4rem;
  }
</style>

<h1 class="absolute">Solid.js update</h1>
<div class="relative" style="padding: 2.5rem 1rem 1rem">
  <div class="absolute react-recon-count">
    count: <s>7</s>=><strong style="color: inherit;">8</strong>
  </div>
  <pre><code class="absolute react-recon-pos">setCount(n => n + 1);</code></pre>
 <img src="/assets/solidjs-update.svg" alt="react reconciliation" />
</div>

---

# React uses a Virtual DOM, Solid.js doesn't

<div class="solidjs-click-list mt-12">
<v-clicks>

- Solid.js renders each template once.
- Solid.js constructs a reactive graph to apply fine-grained changes.

</v-clicks>
</div>

---
layout: center
---

# 🍎 to 🍏 API comparison

---

# Familiar api for React developers

<div class="solidjs-click-list solidjs-gap-max">
<v-clicks>

- [useState](https://reactjs.org/docs/hooks-reference.html#usestate) <mdi-arrow-right /> [createSignal](https://www.solidjs.com/docs/latest/api#createsignal)
- [useEffect](https://reactjs.org/docs/hooks-reference.html#useeffect) <mdi-arrow-right /> [createEffect](https://www.solidjs.com/docs/latest/api#createeffect)
- [useMemo](https://reactjs.org/docs/hooks-reference.html#usememo) <mdi-arrow-right /> [createMemo](https://www.solidjs.com/docs/latest/api#creatememo)
- [useContext](https://reactjs.org/docs/hooks-reference.html#usecontext) <mdi-arrow-right /> [useContext](https://www.solidjs.com/docs/latest/api#usecontext)
- [and much more...](https://www.solidjs.com/docs/latest/api)

</v-clicks>

</div>

---
layout: center
---

# Solid.js component

```typescript
function Counter(props) {
  const [count, setCount] = createSignal(props.initialCount ?? 0);

  createEffect(() => {
    console.log(`count ${count()}`);
  });

  return (
    <button type="button" onClick={() => setCount((n) => ++n)}>
      {count()}
    </button>
  );
}
```

A standard Solid.js component it's just a function that:
- returns a DOM [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)
- receives props from the parent component
- runs **once** per instance, in other words, does not rerender

[playground](https://playground.solidjs.com/anonymous/e3e51094-6dc9-42a0-a443-29e5aef0bcbe)

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">Conditional rendering</h1>

## React

```ts
function App() {
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const toggle = () => setIsLoggedIn((val) => !val);

  return isLoggedIn ? (
    <button onClick={toggle}>Log out</button>
  ) : (
    <button onClick={toggle}>Log in</button>
  );
}
```

[playground](https://stackblitz.com/edit/react-ts-rwam95?file=index.tsx)

::right::

## Solid

```ts
function App() {
  const [isLoggedIn, setIsLoggedIn] = createSignal(false);
  const toggle = () => setIsLoggedIn((val) => !val);

  return (
    <Show 
      when={isLoggedIn()} 
      fallback={<button onClick={toggle}>Log in</button>}
    >
      <button onClick={toggle}>Log out</button>
    </Show>
  );
}
```

[playground](https://playground.solidjs.com/anonymous/8545f7ef-7088-45b2-bc44-8b2804e8a660)

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">Render lists</h1>

## React

```ts
const palette = [
  '#26547C', '#EF476F', '#FFD166', '#06D6A0'
];

function Palette({ palette }: { palette: string [] }) {
  return (
    <ul className="color-list">
      {palette.map((color) => (
        <li key={color} style={{ background: color }} />
      ))}
    </ul>
  );
}
```

[playground](https://stackblitz.com/edit/react-ts-7m7cen?file=index.tsx)

::right::

## Solid

```ts
const palette = [
  '#26547C', '#EF476F', '#FFD166', '#06D6A0'
];

function Palette(props: { palette: string[] }) {
  return (
    <ul class="color-list">
      <For each={props.palette}>
        {(color) => <li style={{ background: color }} />}
      </For>
    </ul>
  );
}
```

[playground](https://stackblitz.com/edit/solidjs-templates-zqyzcv?file=src%2Findex.tsx)

---

# Ecosystem | Libraries

<div class="solidjs-click-list">

- [react-use](https://github.com/streamich/react-use) <mdi-arrow-right /> [solid-primitives](https://github.com/solidjs-community/solid-primitives)
- [react-router](https://reactrouter.com/en/main) <mdi-arrow-right /> [solid-router](https://github.com/solidjs/solid-router)
- [react-transition-group](https://reactcommunity.org/react-transition-group/) <mdi-arrow-right />  [solid-transition-group](https://github.com/solidjs/solid-transition-group)
- [react-testing-library](https://testing-library.com/docs/react-testing-library/intro/) <mdi-arrow-right /> [solid-testing-library](https://github.com/solidjs/solid-testing-library)
- [@tanstack/react-query](https://tanstack.com/query/v4/docs/adapters/react-query) <mdi-arrow-right /> [@tanstack/solid-query](https://tanstack.com/query/v4/docs/adapters/solid-query)
- [react-window](https://react-window.vercel.app/#/examples/list/fixed-size) <mdi-arrow-right />  [@tanstack/solid-virtual](https://tanstack.com/virtual/v3/docs/adapters/solid-virtual)
- [...and much more](https://www.npmjs.com/search?q=solidjs)

</div>

---
layout: center
---

# Create a new project

---
layout: two-cols
---

<style>
  .asterisk {
    position: fixed;
    left: 4rem;
    bottom: 3rem;
    z-index: 2;
  }
</style>

<h1 class="solidjs-two-cols-heading">Create new project | Vite template</h1>

<img style="width: 60%; margin: 2rem auto 0;" src="/assets/vite-logo-shadow.png" alt="vite logo" aria-hidden="true" />

::right::

<section style="padding: 1rem 2rem 0;">

```bash
npx degit solidjs/templates/ts my-solid-app
```

<div style="padding-top: 2rem;" />

## Rendering

- Client-side rendering - [solid-router](https://github.com/solidjs/solid-router).
- [Server-side rendering \*](https://www.solidjs.com/guides/server) 

## Guides

- [List of available templates](https://github.com/solidjs/templates/blob/master/README.md#solid-templates-using-vite)
- [Vite docs](https://vitejs.dev/)


<div style="padding-top: 2rem;" />

### Examples

- [barcode-generator](https://fabervitale.github.io/solid-bricks/examples/barcode-generator/)

</section>

<div class="asterisk"> 
<a href="https://vitejs.dev/guide/ssr.html#server-side-rendering" target="_blank">* some assembly required</a>
</div>

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">Create new project | Astro</h1>

 <img style="margin: 5rem 1rem 0" src="/assets/astro-logo-dark.svg" alt="astro logo" />

::right::

<section style="padding: 2rem; ">


```bash
npm create astro@latest
```

<br />

## Rendering

- [SSG - island architecture](https://docs.astro.build/en/concepts/islands)
- [SSR - node app o Edge functions](https://docs.astro.build/en/guides/server-side-rendering/)

## Guides

- [Getting started](https://docs.astro.build/en/getting-started/)
- [Integrate Solid](https://docs.astro.build/en/guides/integrations-guide/solid-js/)

<div style="padding-top: 2rem;" />

### Examples

- [romajs.org](https://romajs.org/)

</section>

---
layout: two-cols
---

<h1 class="solidjs-two-cols-heading">Create new project | SolidStart</h1>

 <img style="margin: 2rem 0 0" src="/assets/solid-bg-1.svg" alt="solid logo" />

::right::

Meta-framework developed by the [Solid.js team](https://www.solidjs.com/contributors),
powered by [vite](https://vitejs.dev/) and currently in **beta**.

<section style="padding: 2rem; ">

## Rendering

- Client-side rendering (CSR)
- Server-side rendering (SSR)
- Streaming SSR
- Static site generation (SSG)

## Guides

- [What's SolidStart](https://start.solidjs.com/getting-started/what-is-solidstart)
- [Project setup](https://start.solidjs.com/getting-started/project-setup)

</section>
