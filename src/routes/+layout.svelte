<script>
	import Header from './Header.svelte';
  	import Main from './Main.svelte';
	import '../app.css';
</script>

<div class="app">
	<Header />

	<slot/>

	<footer>

	</footer>
</div>
