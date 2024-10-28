# Tailwind-CSS-with-Vite-Step-by-Step-Guide

If you want to start a project using only **HTML**, **Tailwind CSS**, and **Vite** without React or any other JavaScript framework, here's how you can do it:

### Step 1: Create a Vite Project (Without React)
1. **Initialize a Vite project:**
   Open your terminal and run:
   ```bash
   npm create vite@latest my-html-tailwind-project
   ```
   - When prompted, select `vanilla` as the template (this is for plain HTML, CSS, and JavaScript).

2. **Navigate to the project directory:**
   ```bash
   cd my-html-tailwind-project
   ```

3. **Install dependencies:**
   Install the project dependencies by running:
   ```bash
   npm install
   ```

### Step 2: Install and Set Up Tailwind CSS
1. **Install Tailwind CSS:**
   Run the following command to install Tailwind and its dependencies:
   ```bash
   npm install -D tailwindcss postcss autoprefixer
   ```

2. **Initialize Tailwind CSS:**
   Create the `tailwind.config.js` file by running:
   ```bash
   npx tailwindcss init
   ```

### Step 3: Configure Tailwind CSS
1. **Configure template paths:**
   Open the `tailwind.config.js` file and modify the `content` property to include your HTML files:
   ```js
   /** @type {import('tailwindcss').Config} */
   module.exports = {
     content: [ "*" ],
     theme: {
       extend: {},
     },
     plugins: [],
   };
   ```

### Step 4: Add Tailwind Directives to Your CSS
1. **Create a CSS file:**
   In the `src` folder, create a new CSS file (e.g., `style.css`), and add the following Tailwind directives:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

2. **Import the CSS file in the `index.html`:**
   Now, link this CSS file to your `index.html` by adding this in the `<head>` section:
   ```html
   <link rel="stylesheet" href="/src/style.css">
   ```

### Step 5: Add Some HTML and Tailwind Classes
1. **Modify `index.html`:**
   Open the `index.html` file and start using Tailwind classes. For example:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>My Tailwind Project</title>
     <link rel="stylesheet" href="/src/style.css">
   </head>
   <body>
     <div class="flex items-center justify-center h-screen">
       <div class="text-center">
         <h1 class="text-4xl font-bold text-blue-500">Hello Tailwind CSS!</h1>
         <p class="mt-4 text-lg text-gray-600">Start building your UI with Vite and Tailwind CSS.</p>
       </div>
     </div>
   </body>
   </html>
   ```

### Step 6: Run the Vite Development Server
1. **Start the server:**
   Run the following command in your terminal:
   ```bash
   npm run dev
   ```
   This will start the Vite development server and open your project in the browser. You should now see your HTML page styled with Tailwind CSS.

### Step 7: Build for Production
When you're ready to build the project for deployment, run:
```bash
npm run build
```
This will generate a `dist` folder with your production-ready code, which can be deployed to any static hosting service.

This setup is a simple and fast way to build an HTML project with Vite and Tailwind CSS.
