# blog-website
# all index.html code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Blog</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Navbar -->
  <header class="navbar">
    <div class="container">
      <h1 class="logo">My Blog</h1>
      <nav>
        <ul class="nav-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
        <button class="nav-toggle" id="navToggle">&#9776;</button>
      </nav>
    </div>
  </header>

  <!-- Blog Content -->
  <main class="content">
    <div class="container">
      <article class="post">
        <h2 class="post-title">Welcome to My Blog</h2>
        <p class="post-content">This is a simple blog post. Here you can share updates, stories, and thoughts. Make it your own!</p>
      </article>
      <article class="post">
        <h2 class="post-title">Another Post Title</h2>
        <p class="post-content">Here is another example post. You can add more posts and style them with CSS for a unique look.</p>
      </article>
    </div>
  </main>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">
      <p>&copy; 2024 My Blog. All rights reserved.</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>

# STYLES.CSS
/* General reset and styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
  }
  
  /* Container */
  .container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
  }
  
  /* Navbar */
  .navbar {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
  }
  
  .navbar .logo {
    display: inline-block;
    font-size: 1.5rem;
  }
  
  .navbar nav {
    float: right;
  }
  
  .nav-links {
    list-style: none;
  }
  
  .nav-links li {
    display: inline-block;
    margin: 0 1rem;
  }
  
  .nav-links a {
    color: #fff;
    text-decoration: none;
  }
  
  .nav-toggle {
    display: none;
    background: none;
    border: none;
    color: #fff;
    font-size: 1.5rem;
  }
  
  /* Blog Content */
  .content {
    padding: 2rem 0;
  }
  
  .post {
    margin-bottom: 2rem;
  }
  
  .post-title {
    font-size: 1.8rem;
    color: #333;
  }
  
  .post-content {
    margin-top: 1rem;
  }
  
  /* Footer */
  .footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
    margin-top: 2rem;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .nav-toggle {
      display: inline-block;
    }
  
    .nav-links {
      display: none;
      width: 100%;
      text-align: center;
    }
  
    .nav-links li {
      display: block;
      margin: 1rem 0;
    }
  }


  # SCRIPT.JS
  // Toggle Navbar for mobile view
const navToggle = document.getElementById('navToggle');
const navLinks = document.querySelector('.nav-links');

navToggle.addEventListener('click', () => {
  navLinks.classList.toggle('active');
});
