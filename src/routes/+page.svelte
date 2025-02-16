<script lang="ts">
  let greeting: string = "Coming Soon.";
</script>

<svelte:head>
  <title>
    {greeting}
  </title>
  <meta name="description" content="Coming soon!">
  <link rel="preconnect" href="https://fonts.bunny.net">
  <link href="https://fonts.bunny.net/css?family=caveat-brush:400" rel="stylesheet" />
</svelte:head>
<main>
  <div class="greeting">
    <h1>{greeting}</h1>
  </div>
</main>

<style>
  main {
    align-content: center;
    font-family:
      system-ui,
      -apple-system,
      BlinkMacSystemFont,
      "Segoe UI",
      Roboto,
      Oxygen,
      Ubuntu,
      Cantarell,
      "Open Sans",
      "Helvetica Neue",
      sans-serif;
    height: 100%;
  }

.greeting {
    font-family: 'Caveat Brush', handwriting;
    font-size: 3em;
    text-align: center;
    font-weight: 100;
}

</style>
