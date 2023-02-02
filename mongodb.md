# Lecture2 - Jan/24/2023 

**Crud Operations**

**Embeded object projection**

`db.instructors.find({},{"address.city":1})`

**update**
> {condition,update,[options]}

**to add new property on all documetns**
```


ins.updateMany(
    {}
,{})
```