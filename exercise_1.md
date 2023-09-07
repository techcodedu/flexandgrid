# Exercise: Convert Non-Flex Design to Flexbox

In this exercise, you will be given a design that uses the older float method. Your task is to convert the entire design to utilize the power of flexbox, without changing the look and feel of the website.

## Starting Point

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Design with Semantic HTML</title>
    <!--css -->
  </head>
  <body>
    <!-- Header -->
    <header>
      <!-- Navigation Bar -->
      <nav class="navbar">
        <a href="#" class="nav-item">Home</a>
        <a href="#" class="nav-item">About</a>
        <a href="#" class="nav-item">Services</a>
        <a href="#" class="nav-item">Contact</a>
      </nav>
    </header>

    <!-- Main Content -->
    <main>
      <!-- Cards -->
      <section class="cards-container">
        <article class="card">
          <h2>Card 1</h2>
          <p>Description for Card 1.</p>
        </article>
        <article class="card">
          <h2>Card 2</h2>
          <p>Description for Card 2.</p>
        </article>
        <article class="card">
          <h2>Card 3</h2>
          <p>Description for Card 3.</p>
        </article>
      </section>
    </main>

    <!-- Optional Footer -->
    <!-- <footer>...</footer> -->
  </body>
</html>

```
Here's the current CSS design using the `float` method:

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f7f7f7;
    color: #333;
}

header {
    background-color: #333;
    padding: 15px 0;
    color: #fff;
}

.navbar {
    width: 80%;
    margin: 0 auto;
    overflow: hidden;
}

.nav-item {
    float: left;
    padding: 10px 20px;
    margin-right: 20px;
    text-decoration: none;
    color: #fff;
    border-radius: 5px;
    transition: background-color 0.2s;
}

.nav-item:hover {
    background-color: #555;
}

.cards-container {
    width: 80%;
    margin: 40px auto;
    overflow: hidden;
}

.card {
    float: left;
    width: calc(30.33% - 30px);
    padding: 20px;
    margin-right: 20px;
    margin-bottom: 20px;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
    transition: box-shadow 0.2s, transform 0.2s;
}

.card:hover {
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
    transform: translateY(-5px);
}

h2 {
    margin-top: 0;
}

p {
    margin-bottom: 0;
}
```

## Tasks:

1. **Navbar**: Convert the `.navbar` to use flexbox so the navigation items align horizontally.
2. **Cards Container**: Convert the `.cards-container` to use flexbox so the cards are displayed in rows and wrap as necessary.
3. **Card**: Adjust the `.card` properties to ensure it fits well within the flexbox design. Ensure it takes up roughly 1/3rd of the container minus some margin.

## Expected Outcome:

After you've applied the flexbox properties, the design should remain consistent with the original. The only difference will be in the underlying CSS where you'll no longer see any use of the float property for layout purposes.

## Tips:

- Remember to use `display: flex;` to activate flexbox on a container.
- Use `flex-wrap: wrap;` to allow flex items to wrap onto the next line if there's not enough space in the current line.
- Use `flex: 0 0 width;` to give a flex item a specific width.

