<script>
  import { goto } from '$app/navigation';
</script>

<header class="header">
  <div class="container">
    <img src="image/logo.png" alt="Jymce Logo" title="Jymce Logo" />
    <button class="return-button" on:click={() => goto('/#Projects')}>Return</button>
  </div>
</header>

<div class="project-details">
  <h2 class="project-title">Sari Stock - POS</h2>

  <div class="project-content">
    <img src="Project1_Files\SariStock.png" alt="Sari Stock Logo" class="project-image logo" />
    <div class="project-description">
      <p>A simple local device based POS system that utilizes CRUD commands. This project was developed using Python and features basic product management, transaction processing, and sales report generation.</p>
    </div>
  </div>

  <div class="project-content">
    <img src="Project1_Files\Login.png" alt="Login Page" class="project-image" />
    <div class="project-description">
      <p>This is the Login page of SariStock, enabling users to access the system's full capabilities.</p>
    </div>
  </div>
  <div class="project-content">
    <img src="Project1_Files\Home.png" alt="Home Page" class="project-image" />
    <div class="project-description">
      <p>This is the Home page of SariStock, which lets users utilize its capabilities.</p>
    </div>
  </div>
  <div class="project-content">
    <img src="Project1_Files\Products.png" alt="Manage Product Page" class="project-image" />
    <div class="project-description">
      <p>This is the Manage Product Page of SariStock, where users can register products into the system.</p>
    </div>
  </div>
  <div class="project-content">
    <img src="Project1_Files\Cart.png" alt="Transaction Page" class="project-image" />
    <div class="project-description">
      <p>This is the Transaction Page of SariStock, where product transactions and deductions from the database occur.</p>
    </div>
  </div>
  <div class="project-content">
    <img src="Project1_Files\Sales.png" alt="Sales Record Page" class="project-image" />
    <div class="project-description">
      <p>This is the Sales Record Page of SariStock, accessible only to administrators.</p>
    </div>
  </div>
  <div class="project-content">
    <img src="Project1_Files\Database.png" alt="Database Design" class="project-image" />
    <div class="project-description">
      <p>And finally, this is the database design of SariStock.</p>
    </div>
  </div>
</div>

<footer class="footer">
  <div class="footer_container">
    <p class="copyright">&copy; {new Date().getFullYear()} Jymce Brian C. Bertillo</p>
  </div>
</footer>

<style>
  .project-details {
    padding: 2rem;
    background-color: #1E201E;
    color: #ECDFCC;
    font-family: 'Roboto', sans-serif;
    text-align: center;
    padding-top: 60px; /* Add padding to account for the fixed header */
  }

  .project-title {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    font-weight: bold;
    text-transform: uppercase;
  }

  .project-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 2rem;
  }

  .project-image.logo {
    width: 250px;
  }

  .project-image {
    width: 300px;
    height: auto;
    margin-bottom: 1rem;
    border-radius: 3px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Add subtle shadow */
  }

  .project-description {
    margin-top: 1rem;
    line-height: 1.6;
    max-width: 600px;
    text-align: center;
  }

  .project-description p {
    margin-bottom: 1rem;
  }

  /* Header Styles */
  .header {
    background-color: #1E201E; /* Dark background */
    color: #ECDFCC; /* Light text color */
    padding: 0.5rem 0;
    position: fixed; /* Fix the header to the top */
    top: 0;
    left: 0;
    width: 100%;
    z-index: 10; /* Ensure header stays on top */
  }

  .container {
    display: flex;
    justify-content: space-between; /* Space between logo and menu-toggle */
    align-items: center;
    max-width: 520px;
    margin: 0 auto;
  }

  img {
    height: 40px;
  }

  .return-button {
    background-color: #b90e0a; /* Accent color for the button */
    color: #ECDFCC; /* Light text color */
    padding: 0.6rem 2rem;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    margin-left: 1rem; /* Add space between button and logo */
  }

  .footer {
      background-color: #1E201E; /* Dark background color */
      color: #ECDFCC; /* Light text color */
      padding: 2rem 0;
      text-align: center;
      font-family: 'Roboto', sans-serif; /* Match the font from other components */
    }
  
    .footer_container {
      max-width: 960px;
      margin: 0 auto;
    }
  
    .copyright {
      font-size: 1rem; /* Adjust font size as needed */
    }

  /* Media Query for Mobile Devices (650px or less) */
  @media (max-width: 650px) {
    .project-content {
      flex-direction: column; /* Stack content vertically */
      align-items: center; /* Center items within the column */
    }

    .project-image {
      width: 250px; /* Adjust image width for mobile */
    }

    .project-description {
      max-width: 90%; /* Make description wider for mobile */
    }
    .container{
      max-width: 400px;
    }
  }
</style>