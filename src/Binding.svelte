<script>
  let state = {
    name: '',
    kelas: '',
    umur: '',
  }
  let option = false
  $: console.log(state)

  const handleClick = () => {
    option = !option
    console.log(state)
  }
</script>

<input bind:value={state.name} placeholder="masukan nama..." />
<input bind:value={state.kelas} placeholder="masukan kelas..." />
<input bind:value={state.umur} placeholder="masukan umur..." />
<button on:click={handleClick}>Submit</button>

{#if option}
  <p>Hello mas {state.name || 'nama'}</p>
  <p>kelas {state.kelas || 'kelas'}</p>
  <p>umur {state.umur || 'umur'}</p>
{/if}
