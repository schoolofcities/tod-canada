<script>
	import '../assets/global-styles.css';
    export let title = "";
    export let location = "";
    export let keyQuestion = "";
    export let description = "";
    export let image = "";
</script>

<div class="card">
    <p class="title">{title}</p>
    <p class="location">{location}</p>
    <img src={image}/>

    <div>
        <p>Key Question: {keyQuestion}</p>

        <p>{description}</p>
    </div>

</div>

<style>
    p {
        font-family: PoppinsRegular;
    }

    .card {
        background-color: grey;
        border-radius: 50px;
    }
</style>