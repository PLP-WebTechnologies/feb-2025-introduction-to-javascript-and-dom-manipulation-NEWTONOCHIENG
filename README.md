# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to external CSS -->
</head>
<body>
    <header>
        <h1>DOM Manipulation Example</h1>
    </header>

    <main>
        <section id="content">
            <p id="text">This is some text content.</p>
            <button id="changeTextBtn">Change Text</button>
        </section>

        <section id="styleSection">
            <button id="changeStyleBtn">Change Background Color</button>
        </section>

        <section id="addRemoveSection">
            <button id="addElementBtn">Add New Element</button>
            <button id="removeElementBtn">Remove Last Element</button>
        </section>
    </main>

    <footer>
        <p>Example created for learning purposes.</p>
    </footer>

    <script src="script.js"></script> <!-- Link to external JavaScript -->
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    padding: 20px;
}

header {
    text-align: center;
    margin-bottom: 30px;
}

button {
    padding: 10px 15px;
    margin: 10px;
    cursor: pointer;
}

button:hover {
    background-color: #007bff;
    color: white;
}

#addRemoveSection {
    margin-top: 20px;
}

footer {
    text-align: center;
    margin-top: 30px;
    font-size: 0.9em;
    color: gray;
}
// Select buttons and other elements by their ID
const changeTextButton = document.getElementById("changeTextBtn");
const changeStyleButton = document.getElementById("changeStyleBtn");
const addElementButton = document.getElementById("addElementBtn");
const removeElementButton = document.getElementById("removeElementBtn");

// Change text content dynamically
changeTextButton.addEventListener("click", () => {
    const textElement = document.getElementById("text");
    textElement.textContent = "The text content has been changed!";
});

// Modify CSS styles dynamically
changeStyleButton.addEventListener("click", () => {
    document.body.style.backgroundColor = "#d1e7ff";  // Change background color
});

// Add or remove elements dynamically
addElementButton.addEventListener("click", () => {
    const newElement = document.createElement("p");
    newElement.textContent = "This is a new element added to the page.";
    document.getElementById("addRemoveSection").appendChild(newElement);
});

removeElementButton.addEventListener("click", () => {
    const elements = document.getElementById("addRemoveSection").getElementsByTagName("p");
    if (elements.length > 0) {
        elements[elements.length - 1].remove(); // Remove the last <p> element
    }
});
Happy Coding! 💻✨
