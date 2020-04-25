<script>
    export let db;
    let name = ""
    let email = ""
    const addUser = () => {
        console.log("Add new user");
        db.collection("users").add({email,name});
        name = email = ""
    }
</script>

<div class="user">
<form on:submit|preventDefault={addUser}>
    <input type="text" bind:value={email}>
    <input type="text" bind:value={name} >
    <button >ADD</button>
</form>
</div>