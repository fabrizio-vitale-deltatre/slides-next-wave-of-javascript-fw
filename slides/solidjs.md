---
layout: cover
---

<img src="/assets/solid-logo-full.svg"/>

---
layout: two-cols
---

<header>
<h1>What's SolidJS?</h1>
</header>

<p class="no-margin">Solid is a lightweight and declarative reactive library for building user interfaces.</p>

<h2 class="no-margin">Features</h2>

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

<header>
<h1>SolidJS is fast</h1>
</header>

<div class="relative solid-perf-img-wrapper solid-js-bg2">
  <img class="solid-perf-img" src="/assets/christian-englmeier-J7EUjSlNQtg-unsplash.jpg" logo="speed" aria-hidden="true" />
</div>

::right::

<div class="solidjs-click-list">
<v-clicks>

- It's **just** [7.3KB min+gzip](https://bundlephobia.com/package/solid-js@1.5.1).
- At the top of UI speed and memory utilization [benchmarks](https://krausest.github.io/js-framework-benchmark/index.html).
- Blazing fast server-side rendering, based on string interpolation.
- No Virtual Dom, [components render once](https://www.solidjs.com/guides/reactivity).

</v-clicks>
</div>

---
layout: two-cols
---

<header>
<h1>Smaller bundles | A demo app</h1>
</header>

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

</div>

::right::

<div class="mt-5 side-blocks">

## SolidJS

```bash {4}
[...]
index.html                1.58 KiB
assets/index.f8c30131.css 51.87 KiB / gzip: 10.26 KiB
assets/index.54c59109.js  13.62 KiB / gzip: 5.75 KiB
```

- [website](https://next-wave-fw-solid.netlify.app?q=Javascript)
- [<uim-github /> - source](https://github.com/FaberVitale/next-frameworks-sample-app/blob/b79aa7c06c09d888d91e2edbb1f023cfff99323a/src/App.tsx)

</div>

<style>
  .side-blocks {
    display: flex;
    flex-flow: column nowrap;
    gap: 1.5rem;
  }
</style>

---
layout: center
---

# Solid component

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

A standard Solid component it's just a function that:
- returns a DOM [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)
- receives props from the parent component
- runs **once** per instance, in other words, does not rerender

[playground](https://playground.solidjs.com/?version=1.4.1#NobwRAdghgtgpmAXGGUCWEwBowBcCeADgsrgM4Ae2YZA9gK4BOAxiWGjIbY7gAQi9GcCABM4jXgF9eAM0a0YvADo1aAGzQiAtACsyAegDucAEYqA3EogcuPfr2ZCouOAGU0Ac2hqps+YpU6DW09CysrZloIMj5ItW4yXgBeXmAVSMYIGXjjRhM1ejgVLGUwQgwAa2LSwiZCNSLsUrI0NQA3cRUAXUsIBtj1bgBJEQpk3gAGXqsZeghmXDQo3gBhBggXRgAKQnlCMgBKfiteByiY1Mi53BKyOFw1667xxzhnN09vHb2yADoMNCLKBqR4bXgAfnBkwO0wgpxEtGY9HgG1+JloInwvxi+AaaKgzAqHnkcxEL0GjDIwDiw1GPROvAA1IyaYwRhRYadItF1HBfvEPFsQAyuRT2VgRbwTB41vFGIheAikSjcGiMVicXiTASiSTRBK4VIYeFDUJcEw4VtJQAeEz0XC4ZYEYhJFR2h1RFS8KIrDSEpIgLZHJIAPl4dwe61wWy2EGDYeZcckIclpxAVw2QckNv07sdEBThuNEGzECsQlE4hj8d41tBm14+hDJSVyOEqo89wAog0VQAhfAjK1gKCEQgqA4AQmLrZVasx2IIeJkUVw7gAXnBxioAIwAJgmhAoYUwki6QA)

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

<h1 class="absolute">SolidJS update</h1>
<div class="relative" style="padding: 2.5rem 1rem 1rem">
  <div class="absolute react-recon-count">
    count: <s>7</s>=><strong style="color: inherit;">8</strong>
  </div>
  <pre><code class="absolute react-recon-pos">setCount(n => n + 1);</code></pre>
 <img src="/assets/solidjs-update.svg" alt="react reconciliation" />
</div>


---

# Automatic dependency tracking

```typescript {all|2,5-7,12|3,5-7,15}
function Sum() {
  const [a, setA] = createSignal(0);
  const [b, setB] = createSignal(0);

  createEffect(() => {
    console.log(`a + b = ${a() + b()}`);
  });

  return (
    <>
      <button type="button" onClick={() => setA((n) => ++n)}>
        a + 1 ({a()})
      </button>
      <button type="button" onClick={() => setB((n) => ++n)}>
        b + 1 ({(b())})
      </button>
    </>
  );
}
```

[playground](https://playground.solidjs.com/?version=1.4.1#NobwRAdghgtgpmAXGGUCWEwBowBcCeADgsrgM4Ae2YZA9gK4BOAxiWGjIbY7gAQi9GcCABM4jXgF9eAM0a0YvADo1aAGzQiAtACsyAegDucAEYqA3EogcuPfr2ZCouOAGU0Ac2hqsDpy4BRGRk4Zj5pOQVlVQ1tPQsrKxl6CDC0WgheV3oYAAoASn4rXgcMsj5gKF8yOFwAQQBdXgBePzhnN09vXIAGfMtM0ohy3mATatqAISbWx3aXdy8oNV7+xMG5jqCQsNyCloA+IsGS5jL1OAA6NVoPXIADKF4Aal4TFt4AEhAofdeTAqSe5rQaSEHFQS1JiZXIQkoAHgOcJKvHhJnouFwGV4BGIzRU6MxGRUvAyAGENMwANbNED7ZpHGr1PYQQoMl7PVmSJEnFElJ6vACMvFyP0B+WRCP0hKxEB5fIRMuxuLg+LASogJPJlJpdLZjKmLP1HK58oVJXeQpFdIB+XyYMlqOlGNlZr58MIboVIEeLzeH2+v0K-0B90kA3N8P0nuRUbNIMk6yEonEe2N8Oyin0B18IlozBywlwlw8tQCajg8AguEm+AAkiJYWAoIRCCp8gBCcGifOF6uXEy0ET4S7lfAVy4yDK4dwALzgHxUABYAByECgJTCSBpAA) - [reactivity guide](https://www.solidjs.com/guides/reactivity)

---


# Fine-Grained reactivity

<div class="solidjs-click-list pt-6 pb-6">
<v-clicks>

- Signals are **observables** that notify whenever their value changes.
- Effects are automatically **subscribed** to signals they read.
- Before an Effect executes (or re-executes) it is marked as **current listener**.
- Any Signal that is read adds the **current listener** to its subscribers. 

</v-clicks>
</div>

[reactivity guide](https://www.solidjs.com/guides/reactivity)

---
layout: center
---

# Side by side API comparison

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
layout: two-cols
---

<header>
<h1>Conditional rendering</h1>
</header>

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

<header>
<h1>Render lists</h1>
</header>

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

<header class="flex">
<h1>Create new project | Vite template</h1>
</header>

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

<header class="flex">
<h1>Create new project | Astro</h1>
</header>

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

<header class="flex">
<h1>Create new project | SolidStart</h1>
</header>

 <img style="margin: 2rem 0 0" src="/assets/solid-bg-1.svg" alt="solid logo" />

::right::

Meta-framework developed by the [SolidJS team](https://www.solidjs.com/contributors),
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

---
layout: image-right
image: /assets/mahdi-bafande.jpg
---

## Resources

- [SolidJS intro (100 Seconds)](https://www.youtube.com/watch?v=hw3Bx5vxKl0)
- [SolidJS Tutorial](https://www.solidjs.com/tutorial/introduction_basics)
- [API Reference](https://www.solidjs.com/docs/latest/api)
- [FAQ: Why doesn't my early return work in Solid?](https://www.youtube.com/watch?v=Ilf34WjMBkU)
- [Benchmarks](https://krausest.github.io/js-framework-benchmark/index.html)

## Community

- [<uim-twitter /> - twitter](https://twitter.com/solid_js)
- [<uim-discord /> - discord](https://discord.com/invite/solidjs)
- [<uim-github /> - github](https://github.com/solidjs/solid)
- [<uim-youtube /> - youtube](https://www.youtube.com/channel/UCXsRnrbzIX8KHdf86PE241Q)