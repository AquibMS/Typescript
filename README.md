# Typescript   

### 1. In Javascript values assigned to const can be mutated and hence it is not the perfect CONSTANT. For example   
```Javascript
const username = "Aquib";

const userObj = {
    username: "Aquib"
}

const userArray = ["Aquib", 26]

userObj.another = 30;
console.log(userObj)

userArray.push("Mohammad")
console.log(userArray)

#The above code will log the below results:
{ username: 'Aquib', another: 30 }
[ 'Aquib', 26, 'Mohammad' ]
```

But in Typescript we can avoid this by adding assertion property stating these variables are CONSTANT.   
```Typescript
const username = "Aquib";

const userObj = {
    username: "Aquib"
}

const userArray = ["Aquib", 26] as const

userObj.another = 30;

userArray.push("Mohammad")

```
### 2.How to Convert JS Object to JSON String in JQuery/Javascript?
```Javascript
const geeks = {
	name: "Shubham",
	age: 21,
	Intern: "Geeksoforgeeks",
	Place: "Work from Home"
};
const gfg = JSON.stringify(geeks);
console.log(gfg);

# The above code will print as below
{"name":"Shubham","age":21,"Intern":"Geeksoforgeeks","Place":"Work from Home"}
```
