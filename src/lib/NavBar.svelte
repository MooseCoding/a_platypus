<script>
    let menuOpen = false;
  
    const toggleMenu = () => {
      menuOpen = !menuOpen;
    };

    import nav from '$lib/pages/navbar.json'; 
</script>

<style>
    nav {
        @apply shadow-md;
    }
    .container {
        @apply flex items-center justify-between;
    }

    .gradient-text {
    font-size: 1.7rem;
    font-weight: bold;
    background: linear-gradient(90deg, var(--navbar-gradient-from) 0%, var(--navbar-gradient-from) 10%, var(--navbar-gradient-via) 25%, var(--navbar-gradient-to) 50%, var(--navbar-gradient-via) 75%, var(--navbar-gradient-from) 82%, var(--navbar-gradient-from) 100%);
    background-size: 600%;  /* Makes the gradient wider for smooth scrolling */
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
    animation: gradient-animation var(--navbar-timer) infinite linear;
  }

    @keyframes gradient-animation {
        from {
            background-position: 0% 50%;
        }
        to {
            background-position: 100% 50%;
        }
    }

    .menu_item {
        color: var(--menu-text-color);
    }

    .menu_item:hover {
        color: var(--menu-hover-color); 
    }
</style>
  
<nav class="bg-black shadow-md px-4 py-4" style="background-color: {nav.NavBar.NavBarBackgroundColor}">
<div class="container mx-auto flex justify-between">
    <!-- Logo -->
    <div class="text-xl font-semibold gradient-text"
         style="
         --navbar-gradient-from: {nav.NavBar.NavBarGradientFrom};
         --navbar-gradient-via: {nav.NavBar.NavBarGradientVia};
         --navbar-gradient-to: {nav.NavBar.NavBarGradientTo};
         --navbar-timer: {nav.NavBar.NavBarTimer};
         "
    >
        <a href="/">{nav.NavBar.NavBarName}</a>
    </div>

    <!-- Desktop Navigation -->
    <div class="hidden md:flex space-x-6">
        <a href="/about" class="menu_item" style="
        --menu-text-color: {nav.NavBar.NavBarAboutColor};
        --menu-hover-color: {nav.NavBar.NavBarAboutColorHover};
        ">About</a>
        <a href="/contact" class="menu_item"
        style="
        --menu-text-color: {nav.NavBar.NavBarContactColor};
        --menu-hover-color: {nav.NavBar.NavBarContactColorHover};
        ">Contact</a>
    </div>

    <!-- Mobile Menu Button -->
    <button class="md:hidden text-black" on:click={toggleMenu}>
    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
    </svg>
    </button>
</div>

<!-- Mobile Navigation -->
{#if menuOpen}
    <div class="md:hidden flex flex-col items-center space-y-4 mt-4">
        <a href="/about" class="menu_item" style="
        --menu-text-color: {nav.NavBar.NavBarAboutColor};
        --menu-hover-color: {nav.NavBar.NavBarAboutColorHover};
        ">About</a>
        <a href="/contact" class="menu_item"
        style="
        --menu-text-color: {nav.NavBar.NavBarContactColor};
        --menu-hover-color: {nav.NavBar.NavBarContactColorHover};
        ">Contact</a>
    </div>
{/if}
</nav>