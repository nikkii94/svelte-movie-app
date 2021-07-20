<script>
  export let image = '';
  export let movieId = '';
  export let clickable = false;

  const noImage = '/images/no_image.jpg';
</script>

<div class='wrapper'>
  {#if clickable}
    <a href={`/movie/${movieId}`}>
      <img class='clickable' src='{image ?? noImage}'  alt=''/>
    </a>
  {:else}
    <img src='{image ?? noImage}'  alt=''/>
  {/if}
</div>


<style>
  img {
      width: 100%;
      height: 100%;
      transition: all .3s;
      object-fit: cover;
      border-radius: 20px;
  }

  img:hover {
      opacity: .8;
  }

  .clickable {
      cursor: pointer;
  }
</style>