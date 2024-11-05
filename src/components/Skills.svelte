<script>
  const skills = [
    {
      name: "Python",
      description: "Proficient in Python for  web development.",
      image: "image/PYTHON.png" 
    },
    {
      name: "Svelte",
      description: "Experienced in building performant and reactive user interfaces with Svelte.",
      image: "image/SVELTE.png" 
    },
    {
      name: "Java",
      description: "Skilled in Java for developing robust and scalable applications.",
      image: "image/JAVA.png" 
    }
    // Add more skills here...
  ];
</script>

<section class="skills" id="skills">
  <div class="skills-container">
    <h3>Skills</h3>
    <div class="skills-grid">
      {#each skills as skill}
        <div class="skill-item">
          <div class="image-container">
            <img src={skill.image} alt={skill.name} />
          </div>
          <div class="skill-text">
            <h4>{skill.name}</h4>
            <div class="skill-description">
              <p style="overflow: hidden;">{skill.description}</p>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .skills {
    padding: 40px;
    background-color: #1E201E; /* Dark background from AboutMe */
    color: #ECDFCC; /* Light text color from AboutMe */
    text-align: center;
  }

  .skills-container {
    max-width: 900px; /* Adjust as needed */
    margin: 0 auto; /* Center the container */
  }
  .skills-container h3{
      font-size: 4rem;
      padding-bottom: 50px;
  }
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Responsive grid */
    gap: 30px;
  }

  .skill-item {
    background-color: #697565; /* Darker background from AboutMe */
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow */
    text-align: left; /* Align text to the left */
    position: relative; /* For absolute positioning of text */
  }

  .image-container {
    width: 100%;
    /* height: 150px;  Remove height to allow image to adjust */
    position: relative; /* For absolute positioning of text */
    border-radius: 10px; /* Add rounded corners to the image container */
  }

  .skill-item img {
    width: 100%; /* Image takes up full width of container */
    height: auto; /* Maintain aspect ratio */
    transition: transform 0.3s ease-in-out; /* Smooth transition */
    border-radius: 10px; /* Add rounded corners to the image */
    overflow: hidden; /* Hide overflowing parts of the image */
  }

  .skill-item:hover img {
    transform: scale(1.1); /* Zoom in on hover */
  }

  .skill-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%); /* Center the text */
    width: calc(100% - 40px); /* Adjust width as needed */
    height: calc(100% - 40px); /* Adjust height as needed */
    background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent overlay */
    color: #ECDFCC; /* Light text color from AboutMe */
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center; /* Center text horizontally */
    justify-content: center; /* Center text vertically */
    opacity: 0; /* Initially hidden */
    transition: opacity 0.3s ease-in-out; /* Smooth transition */
    text-align: center; /* Center the text within the skill-text container */
  }

  .skill-item:hover .skill-text {
    opacity: 1; /* Show text on hover */
  }

  .skill-item h4 {
    font-size: 1.2rem;
    margin-bottom: 10px;
    font-weight: bold;
  }

  .skill-item p {
    line-height: 1.6; /* Adjust line height for better readability */
  }

  /* Responsive Styling */
  @media (max-width: 650px) {
    .skills-grid {
      grid-template-columns: 1fr; /* One column for mobile */
      gap: 20px; /* Adjust gap as needed */
    }

    .skill-item {
      width: 70%; /* Adjust width as needed */
      margin: 0 auto; /* Center the skill item */
    }

    .image-container {
      width: 100%;
    }

    .skill-item img {
      width: 100%;
      height: auto;
    }

    /* Prevent image overflow on hover */
    .skill-item:hover img {
      transform: scale(1.05); /* Reduced scale for mobile */
    }
  }
</style>