<script>
	export let title = "Title";
	export let count;

</script>

<div class={`container`}>
	<div class="box"><h3 class="recommendation">RECOMMENDATION {count}:</h3></div>
	<h3 class="title">{title}</h3>
</div>

<style>

	.container {
		margin-top: 50px;
		position: relative;
	}

	.box {
		position: absolute;
		width: 240px;
  		margin-left: calc(-50% + 45px - 20px);
		padding: 15px 30px 15px 30px;
		background-color: #f3f2f3;
	}

	.recommendation {
		white-space: nowrap;
		overflow: hidden;
	}

	h3 {
		margin: 0;
	}

	.title {
		padding-top: 8px;
		margin-left: -15px;
		padding-left: 15px;
		border-top: 5px solid #f3f2f3;
	}

	.box h3 {
		font-size: 22px;
		text-align: center;
	}

	@media (max-width: 1300px) {
		.container {
			display: inline;
			position: relative;
		}

		.box {
			position: relative;
			margin-top: 50px;
			width: fit-content;
			margin-left: -20px;
		}

		.box h3 {
			font-size: 20px;
		}
		
		.title {
			border-left: 5px solid #f3f2f3;
			border-top: none;
			margin-left: -20px;
		}

	}


</style>
