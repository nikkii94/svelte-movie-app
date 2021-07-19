<script>
  import { createEventDispatcher } from 'svelte';
  const dispatcher = createEventDispatcher();
</script>

<button on:click={() => dispatcher('loadMore')}>
  <slot />
</button>

<style>
  button {
      background: #000;
      width: 25%;
      min-width: 200px;
      height: 70px;
      color: #fff;
      cursor: pointer;
      transition: all .3s;
      border-radius: 40px;
      font-size: 28px;
      max-width: 1280px;
      display: block;
      margin: 20px auto;
      padding: 0 20px;
      outline: none;
  }

  button:hover {
    opacity: .8;
  }
</style>