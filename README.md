# Tailwind-Node.js
This repository demonstrates how to integrate Tailwind CSS with a Node.js application using Express and Pug (formerly known as Jade).

Here’s a GitHub README file based on the linked guide for using Tailwind CSS with Node.js, Express, and Pug:

---

# Using Tailwind CSS with Node.js, Express, and Pug

This repository demonstrates how to integrate **Tailwind CSS** with a Node.js application using **Express** and **Pug** (formerly known as Jade).

---

## 🚀 Getting Started

Follow the instructions below to set up the project and integrate Tailwind CSS into your Node.js app.

### Prerequisites

Make sure you have the following installed:

- **Node.js** (v14 or later)
- **npm** or **yarn**

---

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Install Tailwind CSS

Run the following commands to add Tailwind CSS and its dependencies:

```bash
npm install tailwindcss postcss autoprefixer
npx tailwindcss init
```

This will generate a `tailwind.config.js` file in your project.

### 4. Configure Tailwind CSS

Update your `tailwind.config.js` file to specify where Tailwind should look for class names:

```js
module.exports = {
  content: ['./views/**/*.pug'], // Add the path to your Pug files
  theme: {
    extend: {},
  },
  plugins: [],
};
```

---

## 📂 Project Structure

```plaintext
.
├── public/
│   └── styles/
│       └── tailwind.css  // Tailwind's generated CSS file
├── views/
│   └── layout.pug        // Example Pug template
├── app.js                // Main application file
├── tailwind.config.js    // Tailwind configuration
└── package.json          // Dependency management
```

---

## 🌈 Usage

### 1. Create a Base CSS File

Create a `styles.css` file in your `public/styles/` directory:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 2. Build Tailwind CSS

Generate your final CSS file:

```bash
npx tailwindcss -i ./public/styles/styles.css -o ./public/styles/tailwind.css --watch
```

The `--watch` flag automatically rebuilds the CSS when you make changes.

### 3. Link Tailwind in Pug Templates

In your `layout.pug` file, include the compiled Tailwind CSS file:

```pug
head
  link(rel="stylesheet", href="/styles/tailwind.css")
```

---

## 🖥️ Running the Server

Start the development server:

```bash
node app.js
```

Visit the app in your browser at `http://localhost:3000`.

---

## ✨ Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Express Documentation](https://expressjs.com/)
- [Pug Documentation](https://pugjs.org/api/getting-started.html)

---

## 🤝 Contributions

Feel free to fork this repo, submit issues, or create pull requests. Contributions are welcome!

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

--- 

Let me know if you want additional customization! 😊
