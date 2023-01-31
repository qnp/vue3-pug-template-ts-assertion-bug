This repository is a minimal reproduction example to illustrates the bug in Vue3 **pug** templates when using type assertion, as proposed by [the official documentation](https://vuejs.org/guide/typescript/overview.html#typescript-in-templates).

It was setup using `yarn create vite . --template vue-ts`

To run it:

```
yarn
yarn dev
```

You can see the runtime error in the console:
```
Uncaught SyntaxError: Unexpected identifier 'as' (at App.vue?vue&type=template&lang.js:5:63)
```

If you want to see the working example using a regular HTML template, you can uncomment it in src/App.vue.
