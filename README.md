# React All Setup Information

### [React Dev](https://react.dev/)

## Installation

npm:

```
npm create vite@latest my-react-app -- --template react
```

```
cd my-react-app
npm i
npm run dev
```

### [Tailwind](https://tailwindcss.com/docs/installation)

```
npm install -D tailwindcss postcss autoprefixer
```

```
npx tailwindcss init -p
```

#### Add the paths to `tailwind.config.js` file.

```js
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
```

#### Add the Tailwind directives in `index.css` file

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### [Daisy UI](https://daisyui.com/docs/install/)

```
npm i -D daisyui@latest
```

### [React Router](https://reactrouter.com/en/main)

```
npm install react-router-dom
```

```js
import { createBrowserRouter, RouterProvider } from "react-router-dom";

const router = createBrowserRouter([
  {
    path: "/",
    element: <MainLayout />,
    errorElement: <ErrorPage />,
    children: [
      {
        index: true,
        element: <Home />,
      },
      {
        path: "/about",
        element: <About />,
        loader: () => fetch("https://jsonplaceholder.typicode.com/users"),
      },
    ],
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>
);
```

```js
import { useLoaderData } from "react-router-dom";

const About = () => {
  const data = useLoaderData();
  return (
    <div>
      <h1>Data Length: {data.length}</h1>
    </div>
  );
};

export default About;
```

### [React Icons](https://react-icons.github.io/react-icons/)
