# type-bug

Steps to reproduce the bug:

1. Install trhe project and initialize:

```sh
npm i
npm run dev
```

2. Then go to `src/App.vue` and see if the components (`<TheWelcome />` or `<HelloWorld />`) are typed correctly by the editor.

3. Close the server, go to `vite.config.ts` and uncomment the AutoImport plugin. Run the server again `npm run dev`.

4. Go back to `App.vue` and check the types. It should now lose the color highlight and have the types as `any` for both components.
