<script>
  import router from 'page';
	import Home from './pages/Home.svelte';
  import Header from './components/Header.svelte';
  import Movie from './pages/Movie.svelte';
  import NotFound from './pages/NotFound.svelte';

  let page;
  let params;

  router('/', () => page = Home);

  router('/movie/:id', (context, next) => {
    params = context.params;
    next();
  }, () => page = Movie);

  router('/*', () => page = NotFound);

  router.start();
</script>

<Header />
<svelte:component this={page} {params} />

<style>
	:global(body) {
		font-family: 'Abel', sans-serif;
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	/*main {*/
	/*	text-align: center;*/
	/*	padding: 1em;*/
	/*	max-width: 240px;*/
	/*	margin: 0 auto;*/
	/*}*/

	/*h1 {*/
	/*	color: #ff3e00;*/
	/*	text-transform: uppercase;*/
	/*	font-size: 4em;*/
	/*	font-weight: 100;*/
	/*}*/

	/*@media (min-width: 640px) {*/
	/*	main {*/
	/*		max-width: none;*/
	/*	}*/
	/*}*/
</style>