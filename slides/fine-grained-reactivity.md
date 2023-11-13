---
layout: center
---

# Fine-grained reactivity

---

# Fine-grained reactivity / 1

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

[playground](https://playground.solidjs.com/anonymous/7829c949-e57a-49b5-bb30-06a1a7657724) - [reactivity guide](https://www.solidjs.com/guides/reactivity)

---

# Fine-grained reactivity / 2

<div class="solidjs-click-list pt-6 pb-6">
<v-clicks>

- Signals are like **observables** that notify whenever their value changes.
- Effects are automatically **subscribed** to signals they read.
- Before an Effect executes (or re-executes) it is marked as **current listener**.
- Any Signal that is read adds the **current listener** to its subscribers. 

</v-clicks>
</div>

[reactivity guide](https://www.solidjs.com/guides/reactivity)

