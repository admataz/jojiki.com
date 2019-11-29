<script>
  export let segment;
</script>

<style>
  main {
    height: 100%;
  }
  a.home-link {
    display: block;
    padding: 0 8px;
    text-decoration-line: none;
    text-decoration: none;
  }
  .page-container {
    height: 100%;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
  }
  .content-container {
    flex: 1 0 100px;
    padding: 20px;
  }
  .header,
  .footer {
    flex: 0 1 90px;
    min-height: 90px;
    background-image: url(/images/workdesk/workdesk.jpg);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    box-shadow: 0 4px 10px 2px rgba(0, 0, 0, 0.4);
  }
</style>

<main>
  <div class="page-container">
    <a href="/">
      <div class="header" />
      {#if segment}
        <a href="/" class="home-link">home</a>
      {/if}
    </a>
    <div class="content-container">
      <slot />
    </div>
    <a href="/">
      <div class="footer" />
    </a>
  </div>
</main>
