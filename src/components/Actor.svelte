<script>
  import {POSTER_SIZE, IMAGE_BASE_URL} from '../helpers/config';

  const noImage = '/no_image.jpg';

  export let actor;
</script>

<div class='wrapper'>
  <img src={actor.profile_path ? `${IMAGE_BASE_URL}${POSTER_SIZE}${actor.profile_path}` : noImage} alt='{actor.name}' />
  <span class='name'>{actor.name}</span>
  <span class='character'>{actor.character}</span>
</div>

<style>
  .wrapper {
      background: #1c1c1c;
      color: #fff;
      border-radius: 20px;
      padding: 5px;
      text-align: center;
  }

  img {
      display: block;
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 15px;
  }

  span.name {
      font-size: 22px;
      margin-top: 10px;
  }

  span {
      display: block;
      margin-bottom: 5px;
  }

</style>