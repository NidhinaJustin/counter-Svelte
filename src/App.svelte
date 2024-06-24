<script>
  // Counter state and validation constraints
  let count = 0;
  const minCount = 0;
  const maxCount = 10;

  // Increment function with validation
  function increment() {
    if (count < maxCount) {
      count += 1;
    } else {
      alert(`Count cannot be more than ${maxCount}`);
    }
  }

  // Decrement function with validation
  function decrement() {
    if (count > minCount) {
      count -= 1;
    } else {
      alert(`Count cannot be less than ${minCount}`);
    }
  }
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    font-family: 'Arial', sans-serif;
  }

  button {
    font-size: 1.5em;
    margin: 0.5em;
    padding: 0.5em 1em;
  }

  p {
    font-size: 2em;
  }
</style>

<main>
  <h1>Counter App</h1>
  <p>{count}</p>
  <button on:click={decrement}>-</button>
  <button on:click={increment}>+</button>
</main>
