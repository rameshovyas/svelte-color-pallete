<script>
	let r = 255;
	let g = 255;
	let b = 255;



const fillPicker = () => {
	document.getElementById("picker").style.backgroundColor = "rgba("+r+","+g+","+b+",1)";

}
</script>

<main>
	<div class="pallete">
		<div id="picker"></div>
		<div class="controls">
			<label> Red
				<input type=number bind:value={r} min=0 max=255 on:change={fillPicker}>
				<input type=range bind:value={r} min=0 max=255 on:change={fillPicker}>
			</label>
			
			<label> Green
				<input type=number bind:value={g} min=0 max=255 on:change={fillPicker}>
				<input type=range bind:value={g} min=0 max=255 on:change={fillPicker}>
			</label>

			<label> Blue
				<input type=number bind:value={b} min=0 max=255 on:change={fillPicker}>
				<input type=range bind:value={b} min=0 max=255 on:change={fillPicker}>
			</label>
		</div>
	</div>
	<div class="hexCode"></div>
</main>

<style>
	.hexCode{
		margin:0 auto;
		text-align: center;
		color:#000;
		font-size: 16px;		
	}
	label{
		display: table-cell;
    	vertical-align: middle;
   		height: 50px;
    	
	}
	#picker{
		width:800px;
		height:400px;
		border:1px solid #000;
		margin:0 auto;
		margin-bottom: 20px;
	}

	.controls{
		margin:0 auto;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}


	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>