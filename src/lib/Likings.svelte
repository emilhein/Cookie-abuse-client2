<script>
  let likes = []
  const ilike = (topic) => {
    if(!likes.includes(topic)){
      likes = [...likes, topic]
      
      fetch(`https://fake-ad-server.herokuapp.com/cookie/${topic}`,{
          credentials: 'include' 
        })
        .then(response => {
            console.log('got it ', response)
        })
        .catch(error => {
          console.error('Panic at the disco:', error);
        })
    }
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
{likes}
</p>
