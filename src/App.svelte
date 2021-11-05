<script>
	let firstName  = "";
	let lastName = "";
    let src = "download.png";
	let count= 0;
	$: fullName =`${firstName} ${lastName}`
	$: {
		console.log(firstName);
		console.log(lastName);
	}
   const resetName = () =>{
	   firstName= "unknown";
	   lastName= "unknown";
   }
</script>

<main>
	<h1>hello {fullName}</h1>
	<label for="firstName">First Name</label>
    <input type="text" bind:value={firstName}>
	<label for="lastName">Last Name</label>
	<input type="text" bind:value={lastName}>
	<button on:click={resetName}>set name to unknown</button>
	<img src="src" alt="svelte logo">
</main>

<style>
	main{
			display: flex;
	flex-direction: column;
	align-items: center;
	}
	h1{
		font-size: 72px;
		text-align: center;
	}
	
</style>