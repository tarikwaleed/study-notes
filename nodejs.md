## Cheat Sheet
### CommonJs import/export style

**export**

```js
module.exports = {
  alias: functionName,
  //OR, Directly and PREFERED
  functionName,
}
```

**import**

```js
const db = require("../assignment1/db")
//then use
db.functionName()
```

---
### ES6 import/export style

> :bulb: First of all, you have to add this property to the nearest `package.json`

```json
{
  "type": "module"
}
```

**export**

```js
export function functionName() {
  //body
}
```

**import**

```js
import { functionName, secondFunctionName } from "moduleName"
```

---
### To write PrettyPrinted JSON to a file

```js
fs.writeFileSync(FILE_PATH, JSON.stringify([], null, 2))
```
---
### To generate random string(commonly used as TOKEN_KEY for jwt authentication)
```shell
require('crypto').randomBytes(64).toString('hex)
```
