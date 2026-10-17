# React Product Dashboard

A small React app built with Vite that shows a list of products
and greets the user by name.

## File Organization

- `src/main.jsx`: entry point, renders the App component.
- `src/App.jsx`: root component. Holds the `showProducts` and `name` state,
  the toggle button, the controlled input, and conditionally renders ProductList.
- `src/components/ProductList.jsx`: holds the static products array and renders
  one Product per item using `.map()` with `id` as the key.
- `src/components/Product.jsx`: shows a product's title and price from props,
  wrapped inside Card. It has no state.
- `src/components/Card.jsx`: a reusable wrapper that renders `children` with a
  border, padding and margin.

## Challenges I Faced

1. **PowerShell blocked npm.** PowerShell refused to run `npm` because running
   scripts was disabled. I fixed it with
   `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned`.
   I also had a typo (`creat` instead of `create`), so I learned to read errors carefully.

2. **GitHub login failed on the first push.** The browser sign-in ended with
   "127.0.0.1 refused to connect". I retried the push and signed in again,
   and then it worked.

3. **Working in small commits.** I built the project step by step (Card, Product,
   ProductList, state, toggle button) and tested each part in the browser
   before committing.

4. **Understanding React concepts.** The hardest parts were why `key` should be
   a stable id and not the array index, how `children` works in Card, and how a
   controlled input works (`value={name}` with `onChange`).

## Run

```bash
npm install
npm run dev
```