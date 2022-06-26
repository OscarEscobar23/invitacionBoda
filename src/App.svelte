<script>
import { src_url_equal } from 'svelte/internal';

import Cover from './components/Cover.svelte'
import Audio from './components/Audio.svelte'
import Timer from './components/Timer.svelte'

let days;
let hours;
let minutes;
let seconds;


</script>

<Audio/>
<main>
	
	<Cover/>
	<Timer bind:days={days}/>

	

</main>

<style>


	
</style>