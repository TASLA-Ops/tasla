<script>
	import logo from '$lib/images/TASLA logo.png';
	let isMenuOpen = false; // State to track if the mobile menu is open
  
	function toggleMenu() {
	  isMenuOpen = !isMenuOpen;
	}
  
	function closeMenu() {
	  isMenuOpen = false;
	}
  </script>
  
  <header class="flex justify-between items-center bg-black py-2 px-4 relative">
	<img src={logo} alt="Logo" class="w-[138px] h-[34px]" />
  
	<!-- Mobile menu button -->
	<button class="md:hidden text-white text-2xl" on:click={toggleMenu}>
	  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
		<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
	  </svg>
	</button>
  
	<!-- Navigation menu (Desktop) -->
	<nav class="hidden md:flex flex-grow absolute top-0 right-0 mt-2 mr-4">
	  <ul class="flex list-none gap-4">
		<li><a href="/" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80">Home</a></li>
		<li><a href="/our-organization" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80">Our Organization</a></li>
		<li><a href="/scholars" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80">Scholars</a></li>
		<li><a href="/sponsors" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80">Sponsors</a></li>
	  </ul>
	</nav>
  
	<!-- Mobile menu items -->
	<nav class={`md:hidden fixed top-0 right-0 bg-black w-1/2 h-screen shadow-lg transition-transform transform ${isMenuOpen ? 'translate-x-0' : 'translate-x-full'}`}>
	  <div class="flex flex-col items-center h-full pt-16">
		<button class="self-end p-4 text-white text-2xl" on:click={closeMenu}>
		  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
		  </svg>
		</button>
		<ul class="flex flex-col items-center flex-grow gap-6">
		  <li><a href="/" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80" on:click={closeMenu}>Home</a></li>
		  <li><a href="/our-organization" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80" on:click={closeMenu}>Our Organization</a></li>
		  <li><a href="/scholars" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80" on:click={closeMenu}>Scholars</a></li>
		  <li><a href="/sponsors" class="text-white text-lg font-normal no-underline font-primary hover:opacity-80" on:click={closeMenu}>Sponsors</a></li>
		</ul>
	  </div>
	</nav>
  </header>  