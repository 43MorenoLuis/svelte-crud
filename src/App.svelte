<script>
	// https://www.youtube.com/watch?v=7wo0zZur_Yk

	let product= { id:'', name:'', description:'', category:'', imageURL:''}

	const handleOnSubmit = e => {
		e.preventDefault();
		console.log(product, 'Fields Form');
	}
</script>

<main>
	<form on:submit={handleOnSubmit}>
		<input 
			bind:value={product.name} 
			type="text" 
			placeholder="Product Name" 
			id="product-name"
		/>
		<textarea
			bind:value={product.description} 
			id="product-description" 
			rows="3" 
			placeholder="Product Description"
		/>
		<input
			bind:value={product.imageURL} 
			type="url" 
			id="product-image-url" 
			placeholder="www.google.com" 
		/>
		<select 
			id="category"
			bind:value={product.category}
		>
			<option 
				value="laptops"
			>
				Laptops
			</option>
			<option 
				value="paripherials"
			>
				Paripherials
			</option>
			<option 
				value="servers"
			>
				Servers
			</option>
		</select>

		<button>
			Save Product
		</button>
	</form>
</main>

<style>
</style>