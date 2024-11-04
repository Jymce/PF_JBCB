<footer class="footer">
    <div class="container">
      <p class="copyright">&copy; {new Date().getFullYear()} Jymce Brian C. Bertillo</p>
    </div>
  </footer>
  
  <style>
    .footer {
      background-color: #1E201E; /* Dark background color */
      color: #ECDFCC; /* Light text color */
      padding: 2rem 0;
      text-align: center;
      font-family: 'Roboto', sans-serif; /* Match the font from other components */
    }
  
    .container {
      max-width: 960px;
      margin: 0 auto;
    }
  
    .copyright {
      font-size: 1rem; /* Adjust font size as needed */
    }

    @media(max-width: 650px){
        .copyright{
            font-size: 0.8rem;
        }
    }
  </style>