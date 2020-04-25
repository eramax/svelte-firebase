<script>
    export let data = {}
    export let remove;
</script>

<input type="text" value={data.email} >

<input type="text" value={data.name} >

<button on:click={remove}>Remove</button>

