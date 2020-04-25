<script>
    import {db} from "./firestore"
	import Users from "./Users.svelte"
	import NewUser from "./NewUser.svelte"
</script>


<Users  db={db} />
<NewUser db={db} />