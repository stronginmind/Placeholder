<script lang="ts">
  let greeting: string = "Coming Soon!";
</script>

<svelte:head>
  <title>
    {greeting}
  </title>
  <meta name="description" content="Coming soon!">
</svelte:head>

<main>
  <div class="greeting">
    <h1>{greeting}</h1>
  </div>
</main>

<style>
  @media (prefers-color-scheme: light) {
    :root {
      --text: #0c0713;
      --background: #f1eff5;
      --primary: #cf6ea5;
      --secondary: #a582d4;
      --accent: #567ec2;
    }
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --text: #f1ecf8;
      --background: #0c0a10;
      --primary: #913067;
      --secondary: #4f2b7d;
      --accent: #3d64a9;
    }
  }

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

    background-color: var(--background);
    color: var(--text);
  }

  .greeting {
    font-family: 'Caveat Brush', handwriting;
    font-size: 3em;
    text-align: center;
    font-weight: 100;
  }

  .greeting h1 {
    background: linear-gradient(to right, var(--primary), var(--secondary), var(--accent));
    -webkit-text-fill-color: transparent;
    -webkit-background-clip: text;
  }
</style>
