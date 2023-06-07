# type-bug

Steps to reproduce the bug:

1. Install the project and initialize it:

```sh
npm i
npm run dev
```

2. Then go to `src/App.vue` and see if the components (`<TheWelcome />` or `<HelloWorld />`) are typed correctly by the vscode editor (they should be).

3. Close the server, go to `vite.config.ts` and uncomment the AutoImport plugin code. Run the server again `npm run dev` (it will generate the AutoImport types).

4. Go back to `App.vue` and check the types. Now, it should have lost the color highlight and have the `any` type for both components.
