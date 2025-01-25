<script>
  import Login from "./Login.svelte";
</script>

<div id="container">
  <!-- Login Section -->
  <div id="wrap">
    <Login></Login>
  </div>

  <!-- Image Section -->
  <!-- svelte-ignore a11y_img_redundant_alt -->
  <img src="logim4.png" alt="Background Image" id="image">
</div>

<style>
  /* Root container */
  #container {
    display: grid; /* Using CSS Grid */
    grid-template-columns: 40% 1fr; /* 40% for login, remaining for image */
    width: 100%; /* Full width */
    height: 100vh; /* Full viewport height */
  }

  /* Login Section */
  #wrap {
    display: flex;
    justify-content: center;
    align-items: center; /* Center content vertically */
    padding: 20px;
  }

  /* Image Section */
  #image {
    width: 100%; /* Ensure the image fills the container's width */
    height: 100%; /* Ensure the image fills the container's height */
    object-fit: cover; /* Keeps the aspect ratio while covering the space */
    display: block; /* Default is visible */
  }

  /* Media query to hide the image on mobile */
  @media (max-width: 768px) {
    #image {
      display: none; /* Hides the image on smaller screens */
    }

    #container {
      grid-template-columns: 1fr; /* Make the login section take full width */
    }
  }
</style>
