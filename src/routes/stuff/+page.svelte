<script>
  import { X } from "plotly.js-dist";

  let count = $state(0);
  let todos = $state(["learn django", "learn svelte"]);
</script>

<h1>Todos</h1>

<form
  onsubmit={(e) => {
    e.preventDefault();
    const input = e.target.querySelector("input");
    const val = input.value;
    console.log({ val });
    todos.push(val);
    input.value = "";
  }}
>
  <h2>Add a todo!</h2>
  <input type="text" />
  <button type="submit">Submit</button>
</form>

<ul>
  {#each todos as x, y}
    <li
      onclick={(x, y) => {
        // todos = todos.filter((a,b) => b != y)
        todos.splice(y, 1);
      }}
    >
      {x} - {y}
    </li>
  {/each}
</ul>
