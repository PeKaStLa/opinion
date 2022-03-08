<script lang="ts">
	import Nested from './nested.svelte';

	var topics = ['ex_topic'];
	var opinions = ['ex_opinion'];

	var new_topic = '';
	var new_opinion = '';
 
	var _ZAHL  = 0;

	function _add_topic() {
		topics = [...topics, new_topic];
		new_topic = '';
	}

	function _add_opinion() {
		opinions = [...opinions, new_opinion];
		new_opinion = '';	}

</script>



<br/>
<br/>
<br/>
<br/>
<br/>
<input type="text" bind:value={new_topic} name="_add_topic"  placeholder="_add_topic">


<button
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
		on:click={() => {
			_add_topic();
		}}>_add_topic</button
	>

	<br/>
<br/>
    <input type="text" bind:value={new_opinion} name="_add_opinion"  placeholder="_add_opinion">


    <button
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
		on:click={() => {
			_add_opinion();
		}}>_add_opinion</button
	>

	
<br/>
<br/>
<br/>
<br/>
<br/>
topics:
{topics}
<br/>
<br/>
<br/>
<br/>
<br/>
opinions:
{opinions}