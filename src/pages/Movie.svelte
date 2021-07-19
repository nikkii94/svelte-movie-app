<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';
  // Components
  import Navigation from '../components/Navigation.svelte';
  import Spinner from '../components/Spinner.svelte';
  import MovieInfo from '../components/MovieInfo.svelte';
  import MovieInfoBar from '../components/MovieInfoBar.svelte';
  import Actor from '../components/Actor.svelte';
  import Grid from '../components/Grid.svelte';

  export let params;

  let isLoading;
  let error;
  let movie;

</script>

Movie
<div transition:fade={{ duration: 300 }}>
  <Navigation />
  <MovieInfo />
  <MovieInfoBar />
  <Grid>

  </Grid>
  <Actor />
  <Spinner />
</div>

<style>

</style>