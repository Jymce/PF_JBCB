<script>
    let isMenuOpen = false;
  
    const toggleMenu = () => {
      isMenuOpen = !isMenuOpen;
    };
  
    const scrollToSection = (sectionId) => {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
      //Close the menu after clicking a link
      isMenuOpen = false
    };
  </script>
  
  <header class="header">
    <div class="container">
  
      <img src="image/logo.png" alt="Jymce Logo" title="Jymce Logo" />
  
      <button class="menu-toggle" on:click={toggleMenu}>
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>
      <nav class="nav" class:open={isMenuOpen}>
        <ul>
          <li>
            <a href="/" on:click={() => scrollToSection('home')}>Home</a>
          </li>
          <li>
            <a href="#about" on:click={() => scrollToSection('about')}>About</a>
          </li>
          <li>
            <a href="#skills" on:click={() => scrollToSection('skills')}>Skills</a>
          </li>
          <li>
            <a href="#Projects" on:click={() => scrollToSection('Projects')}>Projects</a>
          </li>
          <li>
            <a href="#contact" on:click={() => scrollToSection('contact')}>Contact</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
  
  <style>
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
  
    .menu-toggle {
      display: none; /* Hide the menu toggle for larger screens */
      background: none;
      border: none;
      cursor: pointer;
    }
  
    .bar {
      display: block;
      width: 25px;
      height: 3px;
      margin: 5px auto;
      background-color: #ECDFCC; /* Light bar color */
      transition: transform 0.3s ease-in-out;
    }
  
    .menu-toggle:hover .bar {
      transform: scale(1.1);
    }
  
    .nav {
      display: flex;
      align-items: center;
    }
  
    .nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      display: flex;
    }
  
    .nav li {
      margin-left: 15px;
    }
  
    .nav a {
      text-decoration: none;
      color: inherit; /* Inherit color from header */
      font-weight: bold;
      transition: color 0.3s ease-in-out;
    }
  
    .nav a:hover {
      color: #697565; /* Darker color on hover */
    }
  
    /* Responsive Styling */
    @media (max-width: 650px) {
      .menu-toggle {
        display: block;
      }
  
      .nav {
        position: fixed;
        top: 50px; /* Adjust based on header height */
        left: 0;
        width: 100%;
        background-color: #1E201E; /* Dark background */
        padding: 1rem;
        flex-direction: column;
        align-items: flex-start;
        opacity: 0;
        transform: translateY(-10px);
        transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
      }
  
      .nav.open {
        opacity: 1;
        transform: translateY(0);
      }
  
      .nav ul {
        flex-direction: column;
        position: absolute;
        top: -3px; /* Adjust top position based on header height */
        right: 2rem; /* Position the menu to the right of the menu-toggle */
        width: 150px; /* Square box width */
        height: 170px; /* Square box height */
        background-color: #262626;
        padding: 1rem;
        border-radius: 8px;
      }
  
      .nav li {
        margin-bottom: 10px;
        margin-left: 0;
        text-align: center;
      }
  
      /* Adjust logo and menu-toggle positions for screens smaller than 600px */
      .container {
        justify-content: space-between; /* Space between logo and menu-toggle */
      }
  
      img {
        padding-left: 2rem; /* Add padding to the left of the logo */
      }
  
      .menu-toggle {
        padding-right: 2rem; /* Add padding to the right of the menu-toggle */
      }
    }
  </style>