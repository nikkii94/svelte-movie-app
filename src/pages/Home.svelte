<script>

  // Components
  import Header from '../components/Header.svelte';
  import Hero from '../components/Hero.svelte';
  import Search from '../components/Search.svelte';
  import Grid from '../components/Grid.svelte';
  import Thumb from '../components/Thumb.svelte';
  import LoadMoreButton from '../components/LoadMoreButton.svelte';
  import Spinner from '../components/Spinner.svelte';

  // State
  let movies = {
    movies: []
  };
  let isLoading;
  let searchTerm = '';
  let error;


</script>

<Header />
<Hero />
<Search />
<Grid />
<Thumb />
<LoadMoreButton />
<Spinner />

<style>

</style>