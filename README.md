## 🤖 EDU BOT AI Interface

This is a single-page application (SPA) frontend interface for an educational AI chatbot, designed to be clean, modern, and responsive. It simulates the user flow of login, sign-up, and interaction within a chat environment.

---

### ✨ Features

* **View Switching:** Smooth transition between **Login**, **Sign Up**, **Welcome**, and **Chat** views.
* **Responsive Design:** Adapts fluidly to desktop and mobile screens using **Tailwind CSS**.
* **Animated Inputs:** Custom CSS for a focus-based animated line under input fields.
* **Chat Simulation:** Mock functionality for sending messages and receiving simulated bot responses, including a "typing" indicator.
* **Chat History Sidebar:** Displays a mock history list grouped by date, allowing users to load past conversations.
* **Interactive Elements:** Functionality for a `New Chat` button, `Search` bar, and mobile sidebar toggling.
* **Modern Icons:** Utilizes **Lucide Icons** for high-quality, scalable SVG icons.

---

### 🎨 Design & Technology Stack

| Category | Component/Technology | Details |
| :--- | :--- | :--- |
| **Styling** | **Tailwind CSS** | Used via CDN for utility-first styling. |
| **Icons** | **Lucide Icons** | Used via CDN for all visual icons (e.g., `book-open-check`, `bot`, `menu`). |
| **Language** | **HTML5, CSS3, JavaScript** | Standard web technologies for structure, presentation, and logic. |
| **Primary Color** | **Deep Purple (`#7A1F7A`)** | Defined in a CSS variable `--primary-color`. |
| **Architecture** | **Single Page Application (SPA)** | JavaScript handles view management by toggling the `hidden` class on different view containers. |

---

### 🛠️ File Structure (welcome.html)

The entire application is contained within a single `welcome.html` file, structured as follows:

1.  **`<head>`:** Includes meta-tags, Tailwind CSS CDN, Lucide Icons CDN, and custom `<style>` block.
2.  **Custom `<style>`:** Defines **CSS variables** for colors (`--primary-color`), **animated input styles**, and **chat bubble styles** (e.g., `.user-bubble`, `.bot-bubble`), along with responsive adjustments.
3.  **`<body>`:** Contains the main `<div id="app">` container, which hosts all the different view sections (`loginView`, `signUpView`, `welcomeView`, `chatView`).
4.  **`<script>`:** The core JavaScript logic for managing state, view switching, chat simulation, and event listeners.

---

### 🚀 Key JavaScript Functionality

The main script manages the user experience through several key functions:

* **`showView(viewName)`:** Hides all view divs and displays the specified view. This is the core of the SPA logic.
* **`toggleSidebar()`:** Controls the sidebar visibility, especially on mobile, by toggling the `open` class.
* **`renderMessage(text, isUser)`:** Dynamically creates and appends chat bubbles to the `messageBox`.
* **`simulateBotResponse(userMessage)`:** Contains the simple mock logic for generating a response based on keywords (e.g., "code", "ui/ux") and includes a **1.5 second delay** with a **"typing" indicator** for realism.
* **`renderHistory()`:** Processes the `mockHistory` data to generate the list of past chats in the sidebar, grouped by date.

---

### 💻 Running the Application

This is a **pure frontend HTML/CSS/JS file**.

1.  Save the code as **`welcome.html`**.
2.  Open the file in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  The application will start on the **Login View**.
4.  Use the mock credentials or click the **Login** button (with the pre-filled values) to proceed to the **Welcome** screen, which automatically transitions to the **Chat View** after 2 seconds.

---

### 💡 Potential Enhancements

* **Backend Integration:** Connect the form submissions and chat logic to a real backend API (e.g., a **Gemini** model) instead of using mock data.
* **State Management:** Use a framework (like React, Vue, or Svelte) for more robust state management beyond plain JavaScript.
* **Local Storage:** Persist user login state and chat history using `localStorage` or `sessionStorage`.
* **Error Handling:** Implement visual feedback for form validation and login errors.