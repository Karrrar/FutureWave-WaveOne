# Getting Started with Next.js

This guide will help you set up a new Next.js project using Yarn and TypeScript. It also covers key concepts like routing, `useState`, handling click events, and using array methods like `map` and `reduce`.

---

## Initializing a New Next.js Project

To create a new Next.js project with TypeScript, follow these steps:

1. Open your terminal and run the following command:

   ```bash
   yarn create next-app --typescript wave-one-front
   ```

2. Navigate to the newly created project directory:

   ```bash
   cd wave-one-front
   ```

3. Start the development server:

   ```bash
   yarn dev
   ```

4. Open your browser and go to `http://localhost:3000` to see your Next.js app running.

---

## What is Next.js?

Next.js is a React framework for building modern web applications. It provides features like:

- **Server-Side Rendering (SSR):** Render pages on the server for better performance and SEO.
- **Static Site Generation (SSG):** Pre-render pages at build time for fast loading.
- **API Routes:** Build backend APIs directly within your Next.js app.
- **File-Based Routing:** Create routes by adding files to the `pages` directory.
- **Built-in CSS and Sass Support:** Style your app with ease.
- **TypeScript Support:** Write type-safe code with TypeScript.

Next.js is widely used for building scalable, production-ready web applications.

---

## How Routing Works in Next.js

Next.js uses a file-based routing system. Each folder in the `app` directory automatically becomes a route. The new routing system is folder-based, where you create a folder for each route and include a `page.tsx` file inside it.

### What is `tsx`?

The `.tsx` file extension is used for TypeScript files that include JSX syntax. JSX allows you to write HTML-like code within JavaScript/TypeScript. This is commonly used in React components to define the structure of the UI.

### Using `{}` in JSX

In JSX, curly braces `{}` are used to embed JavaScript expressions inside the HTML-like syntax. For example, you can use `{}` to display variables, call functions, or evaluate expressions.

### Example:

```tsx
// app/example/page.tsx
import React from 'react';

const Example = () => {
  const name = "Next.js";
  const getGreeting = () => `Welcome to ${name}!`;

  return (
    <div>
      <h1>{name}</h1> {/* Displaying a variable */}
      <p>{getGreeting()}</p> {/* Calling a function */}
      <p>{2 + 2}</p> {/* Evaluating an expression */}
    </div>
  );
};

export default Example;
```

In this example:
- `{name}` displays the value of the `name` variable.
- `{getGreeting()}` calls a function and displays its return value.
- `{2 + 2}` evaluates an expression and displays the result.

### Empty Page Template

Here’s a basic template for creating a new page:

```tsx
// app/new-page/page.tsx
import React from 'react';

const NewPage = () => {
  return (
    <div>
      <h1>New Page</h1>
      <p>This is a new page.</p>
    </div>
  );
};

export default NewPage;
```

### Example:

1. Create a folder `food` inside the `app` directory and add a `page.tsx` file:

   ```tsx
   // app/food/page.tsx
   import React from 'react';

   const Food = () => {
     return <h1>Food Page</h1>;
   };

   export default Food;
   ```

2. Navigate to `http://localhost:3000/food` to see the Food page.

### Dynamic Routes:

You can create dynamic routes by using square brackets for folder names.

Example:

```tsx
// app/post/[id]/page.tsx
import { useParams } from 'next/navigation';

const Post = () => {
  const params = useParams();
  const { id } = params;

  return <h1>Post ID: {id}</h1>;
};

export default Post;
```

Navigate to `http://localhost:3000/post/123` to see `Post ID: 123`.

---

## `useState` Hook

The `useState` hook is used to manage state in functional components.

### Example:

```tsx
import React, { useState } from 'react';

const Counter = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
};

export default Counter;
```

In this example:
- `count` is the state variable.
- `setCount` is the function to update the state.
- The `increment` function updates the state when the button is clicked.

---

## Handling Click Events

In React, you can handle click events using the `onClick` attribute.

### Example:

```tsx
import React from 'react';

const ClickExample = () => {
  const handleClick = () => {
    alert('Button clicked!');
  };

  return <button onClick={handleClick}>Click Me</button>;
};

export default ClickExample;
```

When the button is clicked, the `handleClick` function is executed, and an alert is shown.

---

## Using `map`

The `map` method is used to render lists in React.

### Example:

```tsx
import React from 'react';

const ItemList = () => {
  const items = ['Apple', 'Banana', 'Cherry'];

  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
};

export default ItemList;
```

In this example:
- The `map` method iterates over the `items` array.
- Each item is rendered as a `<li>` element.
- The `key` prop ensures efficient rendering.

---

## Using `reduce`

The `reduce` method is used to calculate a single value from an array.

### Example:

```tsx
import React from 'react';

const Total = () => {
  const numbers = [10, 20, 30];
  const total = numbers.reduce((acc, num) => acc + num, 0);

  return <p>Total: {total}</p>;
};

export default Total;
```

In this example:
- The `reduce` method calculates the sum of the `numbers` array.
- `acc` is the accumulator, and `num` is the current value.
- The initial value of the accumulator is `0`.

---

## Next Steps

1. Explore the [Next.js Documentation](https://nextjs.org/docs) for more features.
2. Learn about advanced topics like API routes, middleware, and deployment.
3. Build your first Next.js project and experiment with the concepts covered in this guide.

Happy coding! 🚀