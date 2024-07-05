### <p align="center">Coding guidelines for formatting</p>

This document focuses on good coding conventions that we have implemented for our code bases. In order for these to work properly you need to have the following setup on your computer

- [EsLint VScode extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Error lens VScode extension](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
- You should also have some general understanding of eslint

We have made standard guidelines for frontend and backend. The lint files for both of these can be found in the documentation

> :warning: These are rules for only typescript based projects

Copy these and paste in your source code and auto fixable issues will be fixed automatically. The command to lint your code is usually found in your package.json

``` bash
$ npm run lint
# npx eslint \"{src,apps,libs,test}/**/*.ts\ (Or similiar command)
```

This will output all issues. To fix the auto fixable issues, you can run
``` bash
$ npx eslint \"{src,apps,libs,test}/**/*.ts\" --fix #(Or similiar command)
```

Rest of the things, you'll have to fix it yourself. It is however better to add these files in the start of the project so that the code is developed correctly right from the start

- [React Frontned linting rules](/react-frontend.md)
- [Nest Backend linting rules](/nest-backend.md)