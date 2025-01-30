<script>
  import { onMount } from 'svelte'; // Import the DatePicker component
  import Hero from './landing_comps/Hero.svelte';
    import Footer from './landing_comps/Footer.svelte';
    import Workflow from './landing_comps/workflow.svelte';
    import Ending from './landing_comps/ending.svelte';
    import Navbar from './landing_comps/navbar.svelte';
  let showDatePicker = false; // Boolean to control visibility of the date picker

  // Function to toggle the date picker visibility
  function toggleDatePicker() {
    showDatePicker = !showDatePicker;
  }
</script>

<!-- Container -->
<div class="min-h-screen flex flex-col" style="background-color: #0f0b0d;">
  <!-- Navbar Container with Padding -->
  <div class="py-4 px-8">
    <div class="navbar bg-neutral rounded-xl shadow-lg px-4 flex justify-between items-center">
      <!-- Brand or Logo -->
      <div class="flex items-center space-x-2">
        <img class="h-10 w-auto ml-4" src="logo.png" alt="Logo">
        <h1 class="text-2xl sm:text-3xl md:text-4xl leading-tight px-1">Azurro</h1>
      </div>
  
      <!-- Desktop Navbar Links -->
      <div class="hidden md:flex space-x-6 items-center">
        <a href="/download" class="text-white hover:text-gray-300">Download App</a>
        <a href="/login" class="text-[#FF5252] hover:text-accent-content">Login</a>
      </div>
  
      <!-- Mobile Menu Button -->
      <label for="menu-toggle" class="md:hidden btn btn-ghost btn-circle">
        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" stroke-width="2"
          viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </label>
    </div>
    <!-- <Navbar></Navbar> -->
  
    <!-- Mobile Dropdown Menu -->
    <input type="checkbox" id="menu-toggle" class="peer hidden">
    <div class="hidden peer-checked:flex flex-col md:hidden bg-neutral mt-2 rounded-lg shadow-lg p-4">
      <a href="/download" class="block py-2 text-white hover:text-gray-300">Download App</a>
      <a href="/login" class="block py-2 text-accent hover:text-accent-content">Login</a>
    </div>
  </div>
  

  <!-- Main Content -->
  <Hero></Hero>
  <div class="flex flex-col items-center justify-evenly bg-base-100 text-center py-6 border-t-2 border-b-2 border-secondary">
    <h1 class="text-3xl lg:text-5xl mt-6">Here's what we are building:</h1>
    <Workflow></Workflow>
    
</div>

<Ending></Ending>

  

  <!-- Footer -->
  <Footer></Footer>
</div>

<style>
  html, body {
    margin: 0;
    padding: 0;
    height: 100%; /* Ensure full height for the viewport */
  }

  .min-h-screen {
    min-height: 100vh; /* Full viewport height */
  }

  .flex-grow {
    flex: 1; /* Main content grows to push the footer to the bottom */
  }

  h1 {
    font-family: 'Bebas Neue';
  }

  a {
    padding: 10px 20px;
    border-radius: 5px;
    text-decoration: none;
    font-size: 20px;
    transition: background-color 0.3s, color 0.3s;
    font-family: 'Montserrat';
    font-weight: normal;
  }

  a:hover {
    color: white;
  }
</style>
