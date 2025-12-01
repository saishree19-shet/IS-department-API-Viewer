# 📘 IS Department API Viewer

A simple frontend interface that simulates interacting with a REST API. This project demonstrates how to handle JSON data, map specific endpoints to functions, and display structured responses dynamically on a webpage.

## 🌟 Features

* **Mock API Simulation:** Mimics the behavior of fetching data from a backend server using local JSON objects.
* **Dynamic JSON Rendering:** Displays raw JSON data in a readable, formatted structure using `JSON.stringify`.
* **Endpoint Navigation:** Features buttons acting as API endpoints (e.g., `/hod`, `/facilities`) to retrieve specific data subsets.
* **Clean UI:** A user-friendly interface styled with CSS for clear data visualization.

## 🛠️ Tech Stack

* **HTML5:** Structure and button controls.
* **CSS3:** Styling for the layout, buttons, and JSON output formatting.
* **JavaScript (ES6):**
    * **Object Handling:** Storing data in a structured `const` object.
    * **DOM Manipulation:** Updating the `textContent` of the output block dynamically.
    * **JSON Formatting:** Using `JSON.stringify(data, null, 2)` for pretty-printing.

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone <YOUR_REPO_LINK_HERE>
    ```
2.  **Navigate to the project folder:**
    ```bash
    cd <YOUR_PROJECT_FOLDER>
    ```
3.  **Open the file:**
    Double-click `apii.html` to launch it in your default web browser.

## 📸 Usage Guide

1.  **Click `/cs-info`**: Retrieves general information about the Computer Science department (Programs, Focus Areas).
2.  **Click `/hod`**: Fetches details about the Head of Department.
3.  **Click `/facilities`**: Lists available labs, libraries, and seminar halls.
4.  **Click `/ec`**: Displays extracurricular activities like Hackathons and Coding Clubs.
5.  **Click `/getapi`**: Returns the complete dataset (Full JSON object).

## 🧠 Code Highlights

This project simulates backend endpoints using JavaScript functions:

```javascript
const csData = { ... }; // The "Database"

function getHOD() {
  // Simulates GET /hod
  render(csData.hod);
}

function render(data) {
  // Formats JSON for display
  document.getElementById("apiOutput").textContent = JSON.stringify(data, null, 2);
}
