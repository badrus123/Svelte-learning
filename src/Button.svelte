<script>
  let count = 0

  // the `$:` means 're-run whenever these values change'
  $: doubled = count * 2

  function handleClick() {
    count += 1
  }

  export let name
</script>

<style>
  .flex {
    display: flex;
    flex-direction: column;
  }
</style>

<section>
  <div class="flex">
    <button variant="raised" on:click={handleClick}>Clicked</button>
    <a>{name} : {count}</a>
    <a>{name + 'dengan doubled count'} : {doubled}</a>
  </div>
</section>
