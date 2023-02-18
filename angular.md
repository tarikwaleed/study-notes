# Import JSON Array from local file to typescript array

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
