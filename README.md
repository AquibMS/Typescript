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
### 3. Traversing an HTML table with JavaScript and DOM Interfaces
```Javascript
function generateTable() {
  // creates a <table> element and a <tbody> element
  const tbl = document.createElement("table");
  const tblBody = document.createElement("tbody");

  // creating all cells
  for (let i = 0; i < 2; i++) {
    // creates a table row
    const row = document.createElement("tr");

    for (let j = 0; j < 2; j++) {
      // Create a <td> element and a text node, make the text
      // node the contents of the <td>, and put the <td> at
      // the end of the table row
      const cell = document.createElement("td");
      const cellText = document.createTextNode(`cell in row ${i}, column ${j}`);
      cell.appendChild(cellText);
      row.appendChild(cell);
    }

    // add the row to the end of the table body
    tblBody.appendChild(row);
  }

  // put the <tbody> in the <table>
  tbl.appendChild(tblBody);
  // appends <table> into <body>
  document.body.appendChild(tbl);
  // sets the border attribute of tbl to '2'
  tbl.setAttribute("border", "2");
}
```
### 4. Implementation of Insertion sort in Javascript
```Javascript
const insertionSort = (arr) => {
    for (let i = 1 ; i < arr.length ; i++){
        let currentValue = arr[i];
        let j = i - 1;
        while(j >= 0 && arr[j] > currentValue){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1] = currentValue;
    }
    return arr;
};
```
