<script>
</script>


  <div class="home-container">
    <div class="text-container">
      <h2 class="title">BSCS UNDERGRADUATE</h2>
      <p class="greeting">Hi, I'm <span class="accent">Jymce</span></p>
    </div>
    <div class="image_holder">
      <img src="image/background.png" alt="Jymce Bertillo Photo" title="Jymce Bertillo Photo" class="profile-picture" />
    </div>
    </div>



<style>

  .home-container {
    display: flex;
    justify-content: center; /* Center the content */
    align-items: center;
    height: 100vh;
    padding: 22rem 5rem;
    background-color: #1E201E; /* Dark background from AboutMe */
    color: #ECDFCC; /* Light text color from AboutMe */
    font-family: 'Roboto', sans-serif; /* Add a clean font */
    width: 100%;
  }

  .image_holder{
    padding-right: 1rem;
  }
  .profile-picture {
    width: 290px;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Add a subtle shadow */
    animation: float 2s ease-in-out infinite;
  }

  @keyframes float {
    0% {
      transform: translateY(0px); /* Start position */
    }
    50% {
      transform: translateY(-10px); /* Move up slightly */
    }
    100% {
      transform: translateY(0px); /* Back to start position */
    }
  }

  
  .text-container {
    text-align: left; /* Align text to the left */
    padding: 1rem; /* Increase padding for better spacing */
  }

  .title {
    font-size: 2rem; /* Make the title slightly larger */
    font-weight: bold;
    margin-bottom: 1rem;
    text-transform: uppercase; /* Capitalize the title */
  }

  .greeting {
    font-size: 2.5rem; /* Increase font size */
    font-weight: 600; /* Make it slightly bolder */
  }

  .accent {
    color: #b90e0a; /* Add the accent color */
  }

  /* Responsive Styling */
  @media (max-width: 650px) {
    .home-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      height: 100vh;
      padding: 2rem; /* Reduce padding for mobile */
    }

    .profile-picture {
      width: 200px; /* Make the image smaller */
      height: auto;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Add a subtle shadow */
      margin-bottom: 1rem;
    }

    .text-container {
      text-align: center; /* Align text to the left */
      padding-right: 0; /* Increase padding for better spacing */
      padding-bottom: 15px;
    }

    .title {
      font-size: 1.5rem; /* Adjust title size for mobile */
      font-weight: bold;
      margin-bottom: 1rem;
      text-transform: uppercase; /* Capitalize the title */
    }

    .greeting {
      font-size: 2rem; /* Adjust greeting size for mobile */
      font-weight: 600; /* Make it slightly bolder */
    }

    .accent {
      color: #b90e0a; /* Add the accent color */
    }
  }
</style>