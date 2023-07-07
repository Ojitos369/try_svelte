<script>
// @ts-nocheck

  import GeneralState from './lib/GeneralState.svelte';
  import Counter from './lib/Counter.svelte';
  let s, f;
  // original s = {}

</script>

<main>
  <GeneralState bind:s bind:f />

  <div class="card">
    <Counter bind:s />
  </div>
  <button on:click={f.upgradeLvl2('test', 'counter', 'number', (s?.test?.counter?.number || 0) + 1)}>
    Add
  </button>
  <button on:click={f.upgradeLvl2('test', 'counter', 'number', (s?.test?.counter?.number || 0) - 1)}>
    quit
  </button>
  <br>
  <button on:click={f.upgradeLvl2('test', 'counter', 'number2', (s?.test?.counter?.number2 || 0) + 1)}>
    Add2
  </button>
  <button on:click={f.upgradeLvl2('test', 'counter', 'number2', (s?.test?.counter?.number2 || 0) - 1)}>
    quit2
  </button>
  <br>
  <!-- s?.test?.counter?.number -->
  <input 
    type="text"
    value={s?.test?.counter?.number ?? 0}
    on:input={e => f.upgradeLvl2('test', 'counter', 'number', parseFloat(e.target.value || 0))} 
    />

  {#if s?.test?.counter?.number > 10}
    <p>Number is greater than 10</p>
  {:else if s?.test?.counter?.number < 0}
    <p>Number is less than 0</p>
  {:else}
    <p>Number is between 0 and 10</p>
  {/if}
</main>

