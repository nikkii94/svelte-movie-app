<script>
  const svelteLogo = '/images/logo.png';
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
      width: 250px;
      margin-top: 20px;
  }
  .tmdb-logo {
      width: 122px;
      margin-top: 25px;
  }
  @media screen and (max-width: 500px) {
      .content {
          max-width: 1280px;
          min-height: 0px;
      }
      .svelte-logo {
          width: 150px;
          margin-top: 5px;
      }
      .tmdb-logo {
          display: inline-block;
          width: 80px;
          margin-top: 0px;
      }
  }
</style>