<!-- src/routes/__layout.svelte -->
<script lang="ts">
  import "../app.css";
	var _MOBILE_MENU_VISIBLE = false;
	var _PAGE;


</script>

<div class="min-h-screen relative  bg-gray-200">
	<header>
		<div
			class=" md:pb-0  bg-gray-200  
	{_MOBILE_MENU_VISIBLE ? 'pb-52' : 'pb-14'}"
		>
			<nav class="bg-blue-700 fixed w-full z-50  ">
				<div class=" px-8 sm:px-8 lg:px-8 ">
					<div class="flex items-center justify-between h-16  ">
						<div class="flex items-center ">
							<div class="flex-shrink-0 ">
								<a href="." on:click={() => (_PAGE = 1)}>
									<!-- <img class="h-12 w-12" src={_LOGO} alt="World" />-->
								</a>
							</div>
							<div class="hidden md:block">
								<div class="ml-10 flex items-baseline space-x-4">
									<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->

									<a
										href="."
										on:click={() => (_PAGE = 1)}
										class="{_PAGE === 1
											? 'bg-blue-900 text-white '
											: 'text-gray-300  hover:bg-blue-600 hover:text-white'} px-3 py-2 rounded-md text-sm font-medium"
										>Startseite</a
									>

									<a
										href="flat1"
										on:click={() => (_PAGE = 2)}
										class="{_PAGE === 2
											? 'bg-blue-900 text-white '
											: 'text-gray-300  hover:bg-blue-600 hover:text-white'} px-3 py-2 rounded-md text-sm font-medium"
										>flat1</a
									>

									<a
									href="flat2"
									on:click={() => (_PAGE = 3)}
									class="{_PAGE === 3
										? 'bg-blue-900 text-white '
										: 'text-gray-300  hover:bg-blue-600 hover:text-white'} px-3 py-2 rounded-md text-sm font-medium"
									>flat2</a
								>

									<a
										href="info"
										on:click={() => (_PAGE = 4)}
										class="{_PAGE === 4
											? 'bg-blue-900 text-white '
											: 'text-gray-300  hover:bg-blue-600 hover:text-white'} px-3 py-2 rounded-md text-sm font-medium "
										>Info</a
									>
								</div>
							</div>
						</div>
						<div class="-mr-2 flex md:hidden">
							<!-- Mobile menu button -->
							<button
								type="button"
								on:click={() => (_MOBILE_MENU_VISIBLE = !_MOBILE_MENU_VISIBLE)}
								class="bg-blue-600 inline-flex items-center justify-center p-2 rounded-md
							 text-gray-400 hover:text-white hover:bg-blue-600 focus:outline-none  ring-offset-blue-500
							 focus:ring-2 focus:ring-offset-2 focus:ring-offset-blue-400 focus:ring-white"
								aria-controls="mobile-menu"
								aria-expanded="false"
							>
								<span class="sr-only">Open main menu</span>
								<!--
              Heroicon name: outline/menu
              Menu open: "hidden", Menu closed: "block"
            -->

								<svg
									class="{_MOBILE_MENU_VISIBLE ? 'hidden' : 'block'} h-6 w-6"
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke="currentColor"
									aria-hidden="true"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										stroke-width="2"
										d="M4 6h16M4 12h16M4 18h16"
									/>
								</svg>

								<!--
              Heroicon name: outline/x
              Menu open: "block", Menu closed: "hidden"
            -->

								<svg
									class=" h-6 w-6 {_MOBILE_MENU_VISIBLE ? 'block' : 'hidden'}"
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke="currentColor"
									aria-hidden="true"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										stroke-width="2"
										d="M6 18L18 6M6 6l12 12"
									/>
								</svg>
							</button>
						</div>
					</div>
				</div>

				<!-- Mobile menu, show/hide based on menu state. -->

				<div class="md:hidden  {_MOBILE_MENU_VISIBLE ? 'block' : 'hidden'} " id="mobile-menu">
					<div class="px-2 pt-2  pb-3 space-y-1 sm:px-3">
						<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->

						<a
							href="."
							on:click={() => (_PAGE = 1)}
							class=" {_PAGE === 1
								? 'bg-blue-900 text-white '
								: 'text-gray-300  hover:bg-blue-600 hover:text-white'} 
				 px-3 py-2 block rounded-md text-base font-medium">Startseite</a
						>

						<a
							href="flat1"
							on:click={() => (_PAGE = 3)}
							class=" {_PAGE === 3
								? 'bg-blue-900 text-white '
								: 'text-gray-300  hover:bg-blue-600 hover:text-white'} block px-3 py-2 rounded-md text-base font-medium"
							>flat1</a
						>

						<a
							href="flat2"
							on:click={() => (_PAGE = 2)}
							class=" {_PAGE === 2
								? 'bg-blue-900 text-white '
								: 'text-gray-300  hover:bg-blue-600 hover:text-white'} block px-3 py-2 rounded-md text-base font-medium"
							>flat2</a
						>

						<a
							href="info"
							on:click={() => (_PAGE = 4)}
							class=" {_PAGE === 4
								? 'bg-blue-900 text-white '
								: 'text-gray-300  hover:bg-blue-600 hover:text-white'} block px-3 py-2 rounded-md text-base font-medium"
							>Info</a
						>
					</div>
				</div>
			</nav>
		</div>
	</header>
	<main class="   w-full pt-6 md:pt-20 pb-10">
	<!-- xl:w-1/2 lg:w-2/3  lg:mx-auto   -->
		<div
	class="shadow-xl mx-2  p-4 
border-2 border-gray-300 bg-white rounded-md"
>
<!--
<a
href="."
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
        >goto Index</a>
        <a
href="/first_test"
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
        >goto Test</a>
        <a
href="/about"
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
        >goto About</a>
 <a       
href="/opinions"
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
        >goto Opinions</a>
    
 <a       
href="/slider"
		class="bg-gray-800 text-white rounded-md p-1 m-1 
				hover:bg-gray-200  hover:text-black"
        >goto slider</a>
        -->


		<slot />

		</div>
		<div class="pb-20 bg-transparent">
		</div>
	</main>
		<footer class="bg-blue-500 w-full absolute   bottom-0 
		 border-t-2 border-gray-300 p-4
		">
		<p>Andreas und Michaela Stadler
		
		</p>
		<p>
			Hauptstraße 69
		</p>
		<p>
			67433 Neustadt
		</p>
	</footer>
</div>
