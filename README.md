# tech-up-skill-assignment
This is an assignment from techUp Skill training.
## Questions
### Q1. By Using HTML and CSS try to replicate as possible the following User Interface(UI)

![image](https://github.com/Abou-Shadadi/tech-up-skill-assignment/blob/5f7c924de91903b4a5a316b9496d9d3d7102a16e/img/sample.jpeg)


### Q2. As array of product to be bought given names of product and price in dollars below try answer all questions Use your favorite programming.

```js 
 const item = [ 
 {name: 'Bike', price:100},
 {name: 'TV', price:200},
 {name: 'Album', price:10},
 {name: 'Book', price:5},
 {name: 'Phone', price:500},
 {name: 'Computer', price:1000},
 ], 
```
#### 1 . Filter and show the product that will be bought when you don't have much money I mean Cheap one
// let's get the produnct with min value
  min = Math.min.apply(null, item.map(function(itemValue) {
    return itemValue.price;
  }));
 // let's get the object
 var newObj = item.filter(function (el)
{
  return el.price == min ;
}
);
console.log(newObj);
#### 2 . Filter and show the product that will be expensive in the array
```js
// let's get the min value
  max = Math.max.apply(null, item.map(function(itemValue) {
    return itemValue.price;
  }));
  // let's get the object containing the item with max price
  var newObj = item.filter(function (el)
{
  return el.price == max ;
}
);
console.log(newObj);   // display the object
```
#### 3 . Calculate the full price of all product combined
```js
let total = 0;
for (const totalItem of item) {
    const productTotal = totalItem.price;
    total = total + productTotal;
}
console.log(total); // display the total
```
#### 4 . Calculate the full price of all product combined and remove product that are under the 10 dollar
```js
let total = 0;
for (const totalItem of item) {
    if(totalItem.price > 10){ // calculate the price for the items with price above 10 Dollars
    const productTotal = totalItem.price;
    total = total + productTotal;
    }
}
console.log(total); // display the total
```

