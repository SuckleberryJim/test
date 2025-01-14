<script>
  import { onMount } from "svelte";

  export const ssr = false;

  onMount(async () => {
    const { newPlot } = await import("plotly.js-dist");
    let data = { x: [1, 2, 3, 4, 5], y: [1, 2, 3, 4, 5] };
    let layout = { title: "Svelte/Plotly.js Graph" };
    newPlot("1", [data], layout);

    newPlot("2", [{ ...data, mode: "markers" }], {
      ...layout,
      title: "Scatter plot",
    });
  });
</script>

<h1>About page</h1>
<p>This is the super cool about page</p>
<div class="graphs">
  <div id="1"></div>
  <div id="2"></div>
  <div id="3"></div>
  <div id="4"></div>
</div>
