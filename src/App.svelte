<script lang="ts">
  // export let name;
  let Counter: number = 0;

  const modifyCounter = (Value: number): number => (Counter += Value);
  const reset = (): number => (Counter = 0);

  // const add = (): number => Counter++;

  // const dim = (): void => {
  //   Counter--;
  // };

  // const reset = (): void => {
  //   Counter = 0;
  // };
</script>

<main>
  <!-- <h1>Hello Work!</h1> -->
  <!-- {name}!</h1> -->

  <h1>Counter App</h1>

  <hr />

  <h2 class={Counter < 0 ? "negative" : "positive"}>Counter: {Counter}</h2>

  <button class="add" on:click={() => modifyCounter(1)}>+1</button>

  <button class="dim" on:click={() => modifyCounter(-1)}>-1</button>

  <button class="reset" on:click={reset}>Reset</button>

  <!-- <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p> -->
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  h2 {
    font-size: 2rem;
  }

  .positive {
    color: olivedrab;
  }

  .negative {
    color: crimson;
  }

  button {
    font-size: 2rem;
    margin: 0 0.4rem;
    border-radius: 5px;
  }

  button:hover {
    cursor: pointer;
  }

  .add {
    background-color: #26d231;
  }

  .add:active {
    background-color: #19b623;
  }

  .dim {
    background-color: #3a9aea;
  }

  .dim:active {
    background-color: #1e6dad;
  }

  .reset {
    background-color: tomato;
  }

  .reset:active {
    background-color: #b64531;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
