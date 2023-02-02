# Setup new clasp Project

- make sure `nodejs` installed
- initialize an npm package
```
npm init -y
```

- install `clasp` as a dev dependency
```
npm install -D @google/clasp
```
- Login to clasp
```
clasp login
```
- Create a directory inside your project root directory to hold AppsScript related files
```
mkdir apps-script
```
- Create the AppsScript Project
```shell
clasp create --title "your descriptive title here" --rootDir apps-script/
```

- for autocomplete
```
npm install -D @types/google-apps-script
```
- Now everything is setup, you can add the standart `doGet()` function to your script
```js
function doGet() {
  return HtmlService.createTemplateFromFile("index")
    .evaluate()
    .addMetaTag("viewport", "width=device-width, initial-scale=1.0");
}
```

- Then deploy!