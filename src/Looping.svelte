<script>
  let cats = [{ name: 'test 1' }, { name: 'test 2' }, { name: 'test 3' }]
</script>

<h1>Looping Test with svelte</h1>

<ul>
  {#each cats as { name }, i}
    <li>
      <a>{name}</a>
    </li>
  {/each}
</ul>
