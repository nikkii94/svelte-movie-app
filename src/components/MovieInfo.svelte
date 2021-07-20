<script>
  import Thumb from './Thumb.svelte';
  import { POSTER_SIZE, IMAGE_BASE_URL, BACKDROP_SIZE } from '../helpers/config';

  const noImage = '/no_image.jpg';

  export let movie;
</script>

<div class='wrapper'
     style="--backdrop:{movie.backdrop_path ? `url(${IMAGE_BASE_URL}${BACKDROP_SIZE}${movie.backdrop_path})` : '#000'}">
  <div class='content'>
    <div class='thumb'>
      <Thumb image={movie.poster_path ? `${IMAGE_BASE_URL}${POSTER_SIZE}${movie.poster_path}` : noImage} />
    </div>
    <div class='text'>
      <h1>{movie.title}</h1>
      <h3>PLOT</h3>
      <p>{movie.overview}</p>
      <div class='rating-director'>
        <div>
          <h3>IMDB RATING</h3>
          <div class='score'>{movie.vote_average}</div>
        </div>
      </div>
      <div class='director'>
        <h3>DIRECTOR{movie.directors.length > 1 ? 'S' : ''}</h3>
        {#each movie.directors as director}
          <p>{director.name}</p>
        {/each}
      </div>
    </div>
  </div>
</div>

<style>
  .wrapper {
      background: var(--backdrop);
      background-size: cover;
      background-position: center;
      padding: 40px 20px;
  }

  .content {
      display: flex;
      max-width: 1280px;
      max-height: 700px;
      margin: 0 auto;
      background: rgba(0,0,0,0.7);
      border-radius: 20px;
  }

  .text {
      width: 70%;
      padding: 40px;
      color: #fff;
      overflow: hidden;
  }

  h1 {
      font-family: 'Abel', sans-serif;
      font-size: 48px;
      margin: 0;
  }
</style>