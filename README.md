# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>KT LogiVerse</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
</head>
<body>

  <header>
    <nav class="navbar">
      <div class="logo">KT LogiVerse</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">Vision</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Research</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="grid-container">
    <section class="content content-1">
      <h2>Smart Warehousing</h2>
      <p>Automation, AI, and space optimization come together in silence to move the world’s goods.</p>
    </section>
    <section class="content content-2">
      <h2>Route Optimization</h2>
      <p>Where time meets terrain mathematics and maps guide each decision toward efficiency.</p>
    </section>
    <section class="content content-3">
      <h2>Fleet Management</h2>
      <p>Machines hum along rails and roads, orchestrated by a system designed for precision and peace.</p>
    </section>
  </main>

  <footer>
    <p>Crafted with code & conviction © 2025 KT LogiVerse</p>
  </footer>

</body>
</html>

/* Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    font-family: 'Poppins', sans-serif;
    background: #fdfcfb;
    color: #333;
    line-height: 1.6;
  }
  
  /* Navbar */
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #005f73;
    padding: 1rem 2rem;
    color: white;
  }
  
  .logo {
    font-size: 1.8rem;
    font-weight: 700;
  }
  
  .nav-links {
    list-style: none;
    display: flex;
    gap: 1.5rem;
  }
  
  .nav-links a {
    color: white;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
  }
  
  .nav-links a:hover {
    color: #94d2bd;
  }
  
  /* Grid Layout */
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    padding: 2rem;
  }
  
  .content {
    background: white;
    border: 1px solid #ccc;
    border-radius: 12px;
    padding: 1.5rem;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
    transition: transform 0.3s ease;
  }
  
  .content:hover {
    transform: translateY(-5px);
  }
  
  .content h2 {
    margin-bottom: 0.5rem;
    color: #005f73;
  }
  
  .content p {
    font-size: 0.95rem;
    color: #444;
  }
  
  /* Footer */
  footer {
    background: #005f73;
    color: white;
    text-align: center;
    padding: 1rem 0;
    font-size: 0.9rem;
  }
  
  /* Responsive Layouts */
  @media (max-width: 1024px) {
    .grid-container {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  
  @media (max-width: 768px) {
    .grid-container {
      grid-template-columns: 1fr;
    }
  
    .navbar {
      flex-direction: column;
      align-items: flex-start;
    }
  
    .nav-links {
      flex-direction: column;
      gap: 0.5rem;
      margin-top: 1rem;
    }
  }
  
