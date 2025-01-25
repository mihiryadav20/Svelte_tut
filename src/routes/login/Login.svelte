<script>
    let email = '';
    let password = '';
  
    function handleSubmit() {
      // Handle the form submission here (e.g., send a request to your backend)
      console.log('Email:', email);
      console.log('Password:', password);
    }
  </script>
  
  <!-- svelte-ignore css_unused_selector -->
  <style>
    /* General body styling */
   
  
    /* Login form container */
    .login-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      /* background-color: white; */
      padding: 40px;
      border-radius: 10px;
      /* box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1); */
      /* width: 350px; */
      box-sizing: border-box;
    }
  
    h2 {
  font-size: 40px;
  font-family: 'Alexandria';  /* Ensure the text is centered horizontally */
}
  
    /* Styling for the form inputs */
    input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      /* border: 1px solid #ddd; */
      border-radius: 3px;
      font-size: 20px;
      box-sizing: border-box;
      transition: border-color 0.3s ease;
      font-family: 'Montserrat';
    }
  
    /* Focus effect for inputs */
    input:focus {
      outline: none;
    }
  
    /* Button styling */
    button {
      width: 100%;
      padding: 12px;
      color: white;
      border: 1px #3d4451;
      border-radius: 5px;
      border-color: white;
      font-size: 20px;
      font-family: 'Montserrat';
      font-weight: 500;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
  
    /* Button hover effect */
    button:hover {
      background-color: #3d4451;
      font-family: 'Montserrat';
      
    }
    a{
      margin-top: 10px;
      font-family: 'Montserrat';
      font-weight: 400;
      font-size: 20px;
      border-radius: 5px;
    }
  
    
  </style>
  
  <div class="login-container">
    <form on:submit|preventDefault={handleSubmit}>
      <h2>Enter your credentials</h2>
  
      <input 
        type="email" 
        placeholder="Enter your email" 
        bind:value={email} 
        required 
      />
      <input 
        type="password" 
        placeholder="Enter your password" 
        bind:value={password} 
        required 
      />
  
      <a href="/main/dashboard" class="btn btn-secondary btn-outline">Login to dashboard</a>

      
      <!-- Optional: Forgot Password Link -->
      
    </form>
  </div>
  