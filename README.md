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
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="navbar">
    <h1 class="logo">MySite</h1>
    <nav>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <section class="box">Box 1</section>
    <section class="box">Box 2</section>
    <section class="box">Box 3</section>
    <section class="box">Box 4</section>
  </main>

  <footer class="footer">
    &copy; 2025 MySite. All rights reserved.
  </footer>
</body>
</html>
 CSS (styles.css)

/* Base styles */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  color: white;
  padding: 1rem;
}

.logo {
  margin: 0;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  padding: 1rem;
}

.box {
  background-color: #f4f4f4;
  padding: 2rem;
  text-align: center;
  border: 1px solid #ccc;
}

.footer {
  text-align: center;
  padding: 1rem;
  background-color: #333;
  color: white;
}

/* Responsive: Tablet */
@media (max-width: 768px) {
  .container {
    grid-template-columns: repeat(2, 1fr);
  }

  .nav-links {
    flex-direction: column;
    gap: 0.5rem;
  }
}

/* Responsive: Mobile */
@media (max-width: 480px) {
  .container {
    grid-template-columns: 1fr;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    width: 100%;
    padding-left: 0;
  }
}
