# React All Setup Information

### [React Dev](https://react.dev/)

## Installation

npm:

```
npm create vite@latest my-react-app -- --template react
```

```
cd my-react-app
npm run dev
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
            path: '/about,
            element: <About />,
            loader: () => fetch('https://jsonplaceholder.typicode.com/users'),
        }
    ]
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>
);
```

### [React Icons](https://react-icons.github.io/react-icons/)
