**Import JSON Array from local file to typescript array**

- Enable those two options in `tsconfig.json`
```json
"resolveJsonModule": true,
"esModuleInterop": true,
```
- import the JSON File
```typescript
import data from 'path/to/data.json'
``` 
- make interface that suits the data
```typescript
export interface Book{
    id:number;
    titile:string;
}
```
- use the data as you want, for example:
```typescript
@Component({...})
class Foo {
   books: Book[] = data;
}
```

---
**To rendre images from a node.js app running on `localhost:3000`**

- make sure that the images are in `public` or  `uploads`  directories in the root directory
- make sure that `app.js` includes those lines
```js
app.use(cors());
app.use(express.static(path.join(__dirname, "..", "public")));
app.use(express.static(path.join(__dirname, "..", "uploads")));
```
- make sure that the image path in the src of your image tag is
```shell
http://localhost:3000/1678295679109-Linux_logo.jpg
```
>:bulb: note that it's `http` not `https`

- image name should be `image-name.jpg` not `uploads/image-name.jpg`