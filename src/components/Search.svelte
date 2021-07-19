<script>
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();
  let searchText;
  let timeOut;

  // reactive declaration
  // $: test = searchText + ' this is what we want...';
  $: {
    if (searchText !== undefined) {
      clearTimeout(timeOut);
      timeOut = setTimeout(() => {
        dispatch('search', {searchText})
      }, 500);
    }
  }

</script>

<div  class='wrapper'>
  <div class='content'>
    <i class='fas fa-search fa-2x' name='search'></i>
    <input bind:value={searchText} type='text' placeholder='Search movie' />
  </div>
</div>

Search

<style>
  .wrapper {
      width: 100%;
      height: 105px;
      background: #1c1c1c;
      padding: 25px 20px 0 20px;
      box-sizing: border-box;
      color: #fff;
  }

  .content {
      max-width: 1280px;
      width: 100%;
      height: 55px;
      background: #353535;
      margin: 0 auto;
      border-radius: 40px;
      position: relative;
      color: #fff;
  }
</style>