<script>
  import { onMount } from "svelte";
  let data = [];
  onMount(async function() {
    const response = await fetch(
      "https://api.openweathermap.org/data/2.5/forecast/hourly?zip=34232&appid=42b79bb05ef61d3c2a78a86a3a75e6a0"
    );
    const json = await response.json();
    data = json;
    console.log(data);
  });
</script>
