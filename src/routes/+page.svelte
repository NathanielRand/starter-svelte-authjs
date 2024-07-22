<script lang="ts">
	import { signIn, signOut } from "@auth/sveltekit/client"
	import { page } from "$app/stores"
</script>

<h1>Welcome to SvelteKit!!</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<nav>
	<img
	  src={$page.data.session?.user?.image ?? 'https://source.boringavatars.com/marble/120/'}
	  alt="User Avatar"
	  width="100"
	  height="100"
	/>
</nav>

<div>
   <img src="https://placehold.co/150x150" alt="Company Logo" />
   <button on:click={signIn}>Signin</button>
   <button on:click={signOut}>Signout</button>
</div> 
