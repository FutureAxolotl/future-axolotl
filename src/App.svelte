<script>
  import Profile from './lib/Profile.svelte'
  import Links from './lib/Links.svelte'
</script>

<main>
  <div>
    <Profile/>
    <div class="space"></div>
    <Links/>


  <!-- <p class="read-the-docs">
    I don't really know what this will turn into.
  </p> -->
</main>
<style>
  /* .read-the-docs {
    color: #888;
  } */
  .space {
    width: auto;
    height: 16px;
    display: inline-block;
  }
</style>
