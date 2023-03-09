-  to rename all `.js` files in directory to `name.model.js`:

```shell
for file in *.js; mv $file (echo $file | sed 's/\.js$/\.model.js/'); end
``` 
