<script>
  const ilike = (topic) => {
       fakeAdserver.insertAdIntoDiv(topic)

  }
</script>

<button on:click={() => ilike('cats')}>
  I like cats 
</button>
<button on:click={() => ilike('dogs')}>
  I like dogs 
</button>
<button on:click={() => ilike('flowers')}>
  I like flowers 
</button>
<button on:click={() => ilike('Phones')}>
  I like Phones 
</button>
<p>
</p>
