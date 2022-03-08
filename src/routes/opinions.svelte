<script lang="ts">
	import Nested from './nested.svelte';

	var topics = ['ex_topic'];
	var opinions = ['ex_opinion'];

	var new_topic = '';
	var new_opinion = '';
 
	var _ZAHL  = 0;

	function _add_topic() {
		if (new_topic != ""){
			topics = [...topics, new_topic];
			new_topic = '';
		}
	}

	function _add_opinion() {
		if (new_opinion != ""){
		opinions = [...opinions, new_opinion];
		new_opinion = '';	}
	}

</script>



<br/>
<br/>
<br/>
<br/>
<br/>
<input type="text" bind:value={new_topic} name="_add_topic"  placeholder="_add_topic">


<button
class="btn-primary"
		on:click={() => {
			_add_topic();
		}}>_add_topic</button
	>

	<br/>
<br/>
    <input type="text" bind:value={new_opinion} name="_add_opinion"  placeholder="_add_opinion">


    <button
	class="btn-primary"
			on:click={() => {
			_add_opinion();
		}}>_add_opinion</button
	>

	
<br/>
<br/>
topics:
{#each topics as item}
		<Nested {item} />
	{/each}
<br/>
<br/>
opinions:
{#each opinions as item}
		<Nested {item} />
	{/each}