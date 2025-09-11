# ShilpOneer
<<<<<<< HEAD

A MERN application that connects rural artisans (sal-leaf plates, broomsticks, wooden boxes, handicrafts, etc.) directly with buyers — promoting culture, sustainability, and self‑reliance.

## Features

- Product catalog with images (served from the backend `public/product_img`)
- Search and filter on the storefront
- Shopping cart in the frontend with per-item increment/decrement behavior
- Admin UI (basic) for managing products
- Simple in-page chatbot with quick help and command parsing
  - add <product_name> to cart
  - remove <product_name> from cart
  - Optional OpenAI responses if you provide an API key; otherwise it uses a local fallback

## Tech Stack

- Frontend: React (Create React App), Bootstrap 5
- Admin: React (Create React App) based template
- Backend: Node.js, Express, Mongoose (MongoDB)

## Repository Structure

```
ShilpOneer/
  ADMIN/           # Admin React app (runs on :3001)
  frontend/        # Customer-facing React app (runs on :3000)
  server/          # Express API and static product images (runs on :2000)
```

## Prerequisites

- Node.js 18+
- npm 9+
- MongoDB (local or cloud e.g., MongoDB Atlas)

## Backend Setup (server)

1) Install dependencies

```bash
cd server
npm install
```

2) Configure environment

Create a `.env` in `server/` (if not already present):

```env
MONGODB_URI=mongodb://localhost:27017/shilpioneer
PORT=2000
```

3) Start the API server

```bash
npm start
```

Server will be available at `http://localhost:2000`.

Key endpoints (non-exhaustive):

- GET `/product/sel` — list products
- POST `/product/add` — add a product
- DELETE `/product/del/:id` — delete a product

Static product images are served at `http://localhost:2000/product_img/<filename>`.

## Frontend Setup (storefront)

1) Install dependencies

```bash
cd frontend
npm install
```

2) Start the app

```bash
npm start
```

The app will be available at `http://localhost:3000`.

Notes:

- The storefront fetches products from `http://localhost:2000/product/sel`.
- Images are displayed from `http://localhost:2000/product_img/<filename>`.
- Cart is managed in React state. Removing an item via the UI or chatbot removes one instance at a time.

## Admin Setup (optional)

1) Install dependencies and start

```bash
cd ADMIN
npm install
npm start
```

The admin runs at `http://localhost:3001`.

## Chatbot

The chatbot is a lightweight widget injected via `frontend/public/index.html`.

- Click the floating chat button to open/close the widget.
- On first open, it shows a list of things it can help with.
- Commands supported:
  - `add <product_name> to cart` — adds the first matching product (case-insensitive; prefers exact matches) to the cart
  - `remove <product_name> from cart` — removes one matching item from the cart

OpenAI (optional):

- Click “API Key” in the chatbot header and paste your OpenAI API key to enable model replies.
- Without a key, a simple local fallback is used for responses; commands still work.

## Development Tips

- Ensure the backend (port 2000) is running before starting the storefront (port 3000) so product fetches succeed.
- Product images should be placed in `server/public/product_img/` and referenced by their filename in the database.
- If you change ports, update the frontend fetch URLs in the React code.

## License

This project is provided as-is for educational/demo purposes. See LICENSE if present or add one as needed.
=======
 A MERN stack web application for rural economic growth. Marketplace for handmade crafts (sal leaf plates, broomsticks, wooden boxes, etc.) Product CRUD &amp;amp; image uploads Cart &amp;amp; secure checkout Connects artisans with buyers, promoting culture, sustainability &amp;amp; self-reliance.

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)


# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

>>>>>>> 5eef4e357dffe4eaf67b03ae66cb8e22854b5b77
