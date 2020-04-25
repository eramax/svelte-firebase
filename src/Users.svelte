<script>
    import User from "./User.svelte"
    export let db;
    let users = []
    db.collection("users").onSnapshot(data => {
        users = data.docs
    })

    const removeUser = id => {
        db.collection("users").doc(id).delete();
    }
</script>


<div id="users">
{#each users as user}
    <User data={user.data()} remove={() => removeUser(user.id)} />
{/each}
</div>
