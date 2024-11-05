<script>
    import { goto } from '$app/navigation';
  </script>
  
  <div class="projects-container" id="Projects">
    <h2 class="projects-header">Projects</h2>
    <div class="project">
      <img src="Project1_Files\SariStock.png" alt="Sari Stock Logo" class="project-image" />
      <div class="project-description">
        <h3>Sari Stock - POS</h3>
        <p>A simple local device based POS that utilizes CRUD commands. </p>
      </div>
      <button class="see-more-button" on:click={() => goto('/Project1')}>See More <span class="arrow">→</span></button>
    </div>
  </div>
  

<style>
  .projects-container {
    padding: 2rem;
    background-color: #1E201E; /* Dark background color */
    color: #ECDFCC; /* Light text color */
    font-family: 'Roboto', sans-serif; /* Match the font from other components */
    display: flex;
    flex-direction: column;
    align-items: center; /* Center the content horizontally */
  }

  .projects-header {
    font-size: 4rem;
    margin-bottom: 2rem;
    text-transform: uppercase; /* Capitalize the title */
    font-weight: bold;
  }

  .project {
    display: flex;
    flex-direction: column; /* Stack image, description, and button vertically */
    align-items: center;
    margin-bottom: 2rem;
    width: 100%; /* Make the project container take full width */
    justify-content: center; /* Center the project content horizontally */
  }

  .project-image {
    width: 200px;
    height: auto;
    margin-bottom: 1rem; /* Add space below the image */
    border-radius: 8px;
  }

  .project-description {
    /* Add your desired styling for the project description */
    text-align: center; /* Center the description */
  }

  .project-description h3 {
    color: #b90e0a; /* Accent color for project titles */
    margin-bottom: 1rem;
    font-size: 2rem;
  }

  .project-description p {
    font-size: 1rem;
    line-height: 1.5;
  }

  .see-more-button {
    background-color: #b90e0a; /* Accent color for the button */
    color: #ECDFCC; /* Light text color */
    padding: 0.8rem 2rem;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    margin-top: 1rem;
  }

  .arrow {
    font-size: 1.2rem;
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

    .projects-header{
      font-size: 3.5rem;
    }
  }
</style>