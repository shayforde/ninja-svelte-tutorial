<script>

	/*
		https://www.youtube.com/watch?v=9PfCZFqYsYA&list=PL4cUxeGkcC9hlbrVO_2QFVqVPhlZmz7tO&index=8
	*/
 let people = [
    { name: 'yoshi', beltColour: 'black', age: 25, id: 1 },
    { name: 'mario', beltColour: 'orange', age: 45, id: 2 },
    { name: 'luigi', beltColour: 'brown', age: 35, id: 3 }
   ];

	const handleClick = (id) => {
		people= people.filter(person=> person.id != id )
	}
	
</script>
<div class="main">
{#each people as person (person.id)}
<div >
  <h4>{person.name}</h4>
  <p>{person.age} years old,<span > {person.beltColour} </span>belt.</p>
  <button on:click={()=>handleClick(person.id)}>delete</button>
</div>
{:else}
<p>There are no people to show...</p>
{/each}
</div>

<style>
	
		.main {
			
			text-align: center;
		}
		h1 {
			color: #ff3e00;
			text-transform: uppercase;
			font-size: 4em;
			font-weight: 100;
		}
	

</style>