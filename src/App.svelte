<script>
	export let name;

	const changeName = () => {
		name="Another great title/name"
		return name;
	}

	
</script>

<div class="index">
	<h1>{name}</h1>
	<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nam eos, suscipit tempore placeat optio itaque magnam illum quidem voluptas molestiae sed voluptates debitis laborum eligendi, vel veniam culpa. Atque, doloremque!</p>
	<button on:click={changeName}>Change name</button>
</div>


<style>
.index{
	text-align:center;
	display:block;
	margin: 20px auto;
}
</style>