## 1. Aim

To create three differently styled cards using CSS backgrounds, borders, rounded corners, and dimensions. To demonstrate the practical use of `display: block`, `display: inline`, and `display: inline-block`.

## 2. Project Structure

Create a folder named `Assignment-6.2` with the following files:

```text
Assignment-6.2/
├── index.html
└── style.css
```

## 3. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.2 - Backgrounds, Borders & Display</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>Choose Your Plan</h1>
        <p>Explore our Basic, Standard, and Premium plans.</p>
    </header>

    <main class="container">

        <!-- Basic Card -->
        <section class="card basic-card">
            <h2>Basic</h2>
            <p class="price">Free</p>
            <p>Perfect for beginners who want to learn the basics.</p>

            <ul>
                <li>Basic features</li>
                <li>Limited resources</li>
                <li>Community support</li>
            </ul>

            <a href="#display-demo" class="button basic-button">
                Get Started
            </a>
        </section>

        <!-- Standard Card -->
        <section class="card standard-card">
            <span class="popular">POPULAR</span>
            <h2>Standard</h2>
            <p class="price">₹499/month</p>
            <p>Suitable for students who need more learning resources.</p>

            <ul>
                <li>All basic features</li>
                <li>More resources</li>
                <li>Priority support</li>
            </ul>

            <a href="#display-demo" class="button standard-button">
                Choose Standard
            </a>
        </section>

        <!-- Premium Card -->
        <section class="card premium-card">
            <h2>Premium</h2>
            <p class="price">₹999/month</p>
            <p>Designed for users who want the complete experience.</p>

            <ul>
                <li>All standard features</li>
                <li>Advanced resources</li>
                <li>Dedicated support</li>
            </ul>

            <a href="#display-demo" class="button premium-button">
                Go Premium
            </a>
        </section>

    </main>

    <!-- CSS Display Demonstration -->
    <section class="display-section" id="display-demo">
        <h2>CSS Display Property Demonstration</h2>

        <p>
            The display property controls how an element appears in the
            webpage layout.
        </p>

        <div class="demo-box">
            <h3>1. Display: Block</h3>
            <p>
                Block elements start on a new line and normally take the
                available width of their parent.
            </p>

            <div class="block-example">Block Element 1</div>
            <div class="block-example">Block Element 2</div>
        </div>

        <div class="demo-box">
            <h3>2. Display: Inline</h3>
            <p>
                Inline elements stay within the same line when space allows.
                Their width and height cannot be controlled in the same way
                as block or inline-block elements.
            </p>

            <span class="inline-example">Inline Element 1</span>
            <span class="inline-example">Inline Element 2</span>
            <span class="inline-example">Inline Element 3</span>
        </div>

        <div class="demo-box">
            <h3>3. Display: Inline-Block</h3>
            <p>
                Inline-block elements can sit next to each other while
                allowing width and height to be set.
            </p>

            <div class="inline-block-example">Box 1</div>
            <div class="inline-block-example">Box 2</div>
            <div class="inline-block-example">Box 3</div>
        </div>
    </section>

    <footer class="footer">
        <p>Assignment 6.2 | Web Development Practice</p>
    </footer>

</body>
</html>
```

## 4. CSS Code — `style.css`

```css
/* Universal Styles */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
    line-height: 1.6;
}

/* Header */
.header {
    background-color: #172554;
    color: white;
    text-align: center;
    padding: 35px 20px;
}

.header h1 {
    margin: 0 0 10px;
    font-size: 36px;
}

.header p {
    margin: 0;
}

/* Cards Container */
.container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 25px;
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
}

/* Common Card Design */
.card {
    width: 100%;
    max-width: 330px;
    min-height: 420px;
    padding: 25px;
    border: 2px solid;
    border-radius: 18px;
    text-align: center;
    position: relative;
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-6px);
}

.card h2 {
    margin-top: 5px;
    font-size: 28px;
}

.card p {
    margin-bottom: 18px;
}

.price {
    font-size: 24px;
    font-weight: bold;
}

/* Basic Card */
.basic-card {
    background-color: #eff6ff;
    border-color: #60a5fa;
}

.basic-card h2 {
    color: #1d4ed8;
}

.basic-button {
    background-color: #2563eb;
}

/* Standard Card */
.standard-card {
    background-color: #f0fdf4;
    border-color: #22c55e;
}

.standard-card h2 {
    color: #15803d;
}

.standard-button {
    background-color: #15803d;
}

.popular {
    display: inline-block;
    background-color: #dcfce7;
    color: #166534;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
}

/* Premium Card */
.premium-card {
    background-color: #faf5ff;
    border-color: #c084fc;
}

.premium-card h2 {
    color: #7e22ce;
}

.premium-button {
    background-color: #7e22ce;
}

/* Lists Inside Cards */
.card ul {
    text-align: left;
    padding-left: 25px;
    margin-bottom: 25px;
}

.card li {
    margin-bottom: 8px;
}

/* Buttons */
.button {
    display: inline-block;
    color: white;
    text-decoration: none;
    padding: 11px 18px;
    border-radius: 8px;
    font-weight: bold;
    margin-top: 10px;
}

.button:hover {
    opacity: 0.85;
}

/* Display Demonstration Section */
.display-section {
    width: 100%;
    max-width: 1000px;
    margin: 50px auto;
    padding: 25px;
    background-color: white;
    border: 1px solid #cbd5e1;
    border-radius: 14px;
}

.display-section > h2 {
    color: #172554;
}

.demo-box {
    margin: 25px 0;
    padding: 20px;
    background-color: #f8fafc;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
}

.demo-box h3 {
    margin-top: 0;
}

/* 1. Block Example */
.block-example {
    display: block;
    width: 100%;
    max-width: 350px;
    height: 50px;
    margin: 10px 0;
    padding: 12px;
    background-color: #dbeafe;
    border: 2px solid #2563eb;
    border-radius: 6px;
}

/* 2. Inline Example */
.inline-example {
    display: inline;
    background-color: #fef3c7;
    color: #92400e;
    border: 1px solid #d97706;
    padding: 4px;
}

/* 3. Inline-Block Example */
.inline-block-example {
    display: inline-block;
    width: 100px;
    height: 70px;
    margin: 8px 5px 0 0;
    padding: 20px 5px;
    text-align: center;
    background-color: #f3e8ff;
    border: 2px solid #9333ea;
    border-radius: 8px;
}

/* Footer */
.footer {
    background-color: #172554;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 40px;
}

/* Responsive Design */
@media (max-width: 700px) {
    .header h1 {
        font-size: 28px;
    }

    .container {
        gap: 20px;
        margin: 25px auto;
    }

    .card {
        max-width: 100%;
    }

    .display-section {
        width: 92%;
        padding: 18px;
    }

    .inline-block-example {
        width: 85px;
    }
}
```

## 5. Explanation of CSS Properties

| Property | Purpose |
|---|---|
| `background-color` | Sets the background color of an element. |
| `border` | Adds a boundary around an element. |
| `border-radius` | Rounds the corners of an element. |
| `width` | Sets the width of an element. |
| `height` | Sets the height of an element. |
| `max-width` | Sets the maximum allowed width. |
| `display: block` | Starts on a new line and normally uses the available width. |
| `display: inline` | Places content in the text flow without block-style width and height control. |
| `display: inline-block` | Places boxes on the same line while allowing width and height. |
| `padding` | Adds space inside the element's border. |
| `margin` | Adds space outside the element's border. |

## 6. Difference Between the Display Values

**Block:** Each block element starts on a new line. Its width and height can be set.

**Inline:** Inline elements appear within the same line when space permits. Setting `width` and `height` does not work like it does for block elements.

**Inline-block:** Elements can appear next to each other, and their width, height, padding, and margins can be controlled.

## 7. How to Run the Project

1. Open Visual Studio Code.
2. Create the folder `Assignment-6.2`.
3. Create `index.html` and `style.css` inside the folder.
4. Paste the HTML code into `index.html`.
5. Paste the CSS code into `style.css`.
6. Save both files.
7. Open `index.html` with the Live Server extension.
8. Check the three cards and scroll down to view all display examples.
9. Resize the browser window to test the responsive layout.

## 8. Expected Output

- Three differently styled cards: Basic, Standard, and Premium.
- Distinct background colors and border colors for each card.
- Rounded corners created with `border-radius`.
- A title, description, feature list, and button on every card.
- A practical demonstration of `block`, `inline`, and `inline-block`.
- Examples of `width`, `height`, and `max-width`.
- A responsive layout that adjusts to smaller screens.

## 9. Result

A webpage containing three differently styled cards was created successfully using CSS backgrounds, borders, rounded corners, and sizing properties. The practical differences between `display: block`, `display: inline`, and `display: inline-block` were demonstrated.

## 10. Conclusion

CSS background and border properties improve the appearance of webpage elements. The `border-radius` property creates rounded corners, while `width`, `height`, and `max-width` control element dimensions. The `display` property determines how elements participate in the page layout.
