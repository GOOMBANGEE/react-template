# React Template

### Vite + Typescript + Tailwind + Prettier

```js

npm create vite@latest

cd projectName

npm intall


// tailwind
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

// tailwind.config.js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

// index.css
@tailwind base;
@tailwind components;
@tailwind utilities;

// test App.jsx
export default function App() {
  return (
    <>
      <h1 className="text-3xl font-bold underline">Hello world!</h1>
    </>
  );
}


// prettier
npm install --save-dev --save-exact prettier

// tailwind prettier
npm install -D prettier prettier-plugin-tailwindcss

// .prettierrc.json
{
  "plugins": ["prettier-plugin-tailwindcss"]
}

// test code
<button className="text-white px-4 sm:px-8 py-2 sm:py-3 bg-sky-700 hover:bg-sky-800">...</button>

<!-- Before -->
export default function App() {
  return (
    <>
      <h1 className="text-3xl font-bold underline">Hello world!</h1>
      <button className="text-white px-4 sm:px-8 py-2 sm:py-3 bg-sky-700 hover:bg-sky-800">...</button>
    </>
  );
}


<!-- After -->
export default function App() {
  return (
    <>
      <h1 className="text-3xl font-bold underline">Hello world!</h1>
      <button className="bg-sky-700 px-4 py-2 text-white hover:bg-sky-800 sm:px-8 sm:py-3">
        ...
      </button>
    </>
  );
}

```

#### Reference

###### Scaffolding Your First Vite Project

https://vitejs.dev/guide/#scaffolding-your-first-vite-project

###### Install Tailwind CSS with Vite

https://tailwindcss.com/docs/guides/vite

###### Install Prettier

https://prettier.io/docs/en/install

###### Automatic Class Sorting with Prettier

https://tailwindcss.com/blog/automatic-class-sorting-with-prettier
