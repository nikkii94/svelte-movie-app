<script>
  const svelteLogo = '/favicon.png';
  const tmdbLogo = '/images/tmdb_logo.svg';

</script>


<header class='wrapper'>
  <div class='content'>
    <a href='/' aria-label='Go Home'>
      <img alt='svelte logo' class='svelte-logo' src={svelteLogo} />
    </a>
    <img class='tmdb-logo' alt='tmdb logo' src={tmdbLogo} />
  </div>
</header>

<style>
  .wrapper {
      background: #1c1c1c;
      padding: 0 20px;
  }

  .content {
      display: flex;
      align-items: center;
      justify-content: space-between;
      max-width: 1280px;
      min-height: 80px;
      padding: 20px 0;
      margin: 0 auto;
      box-sizing: border-box;
  }

  .svelte-logo {
      max-height: 40px;
  }
</style>