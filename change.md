#Add Module
npm install typescript
npm i --save module-alias

#Add file
tsconfig.json

```ts
{
  "compilerOptions": {
    "module": "commonjs",
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "target": "es6",
    "noImplicitAny": true,
    "moduleResolution": "node",
    "sourceMap": true,
    "outDir": "dist",
    "baseUrl": "./src",
    "paths": {
      "@modules/*": ["rest/modules/*"],
      "@services/*": ["services/*"]
    }
  },
  "include": ["src/**/*"]
}

```

#changes to our package.json:

```ts
...
"_moduleAliases": {
    "@modules": "dist/rest/modules",
    "@services": "dist/services"
  }
...
```
