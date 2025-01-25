<script>
  import { onMount } from 'svelte'; // Import the DatePicker component
  import Hero from './Hero.svelte';
    import Footer from './Footer.svelte';
  let showDatePicker = false; // Boolean to control visibility of the date picker

  // Function to toggle the date picker visibility
  function toggleDatePicker() {
    showDatePicker = !showDatePicker;
  }
</script>

<!-- Container -->
<div class="min-h-screen flex flex-col">
  <!-- Navbar Container with Padding -->
  <div class="p-4">
    <div class="navbar bg-neutral rounded-lg shadow-lg p-4 flex justify-between items-center">
      <!-- Brand or Logo -->
      <div class="flex items-center space-x-2">
        <img class="h-10 w-auto" src="logo.png" alt="Logo">
        <h1 class="text-2xl sm:text-3xl md:text-4xl leading-tight px-1">Azurro</h1>
      </div>

      <!-- Navbar Links -->
      <div class="flex space-x-4 items-center">
        <a href="/download">Download App</a>
        <a href="/login" class="btn btn-accent">Login</a> <!-- Added login button -->
      </div>
    </div>
  </div>

  <!-- Main Content -->
  <div class="flex-grow flex items-center justify-center">
    <Hero />
  </div>

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
