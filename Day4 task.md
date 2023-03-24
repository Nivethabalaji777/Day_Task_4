**1.How to compare two JSON have the same properties without order**
```js
let obj = {name : "person 1", age : 5};
let obj1 = {age : 5, name : "person 1"};

function isEqual(obj, obj1){

  var objkeys = Object.keys(obj);
  var obj1keys = Object.keys(obj1);
    
    if (objkeys.length != obj1keys.length) {
        return false;
    }
    for (var objkey of objkeys) {
        if (obj[objkey] != obj1[objkey]) {
            return false;
        }
    }
    return true;
}
console.log(isEqual(obj, obj1));
```
** **

**2.Use the rest countries API URL-->https://restcountries.com/v3.1/all and display all the      countries flag in the console.**
```js
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function(){
    var resObj = xhr.response;
    for(var i = 0; i<resObj.length; i++){
        //console.log(resObj[i].length);
        console.log(resObj[i].flag);
    }
}
```
** **

**3.Use the same rest countries and print all the countries *names*, *regions*, *sub-region* and *population*.**
```js
//countries names
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function(){
    var resObj = xhr.response;
    for(var i = 0; i<resObj.length; i++){
        console.log(resObj[i].name);
    }
}

//countries region
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function(){
    var resObj = xhr.response;
    for(var i = 0; i<resObj.length; i++){
        console.log(resObj[i].region);
    }
}

//countries sub-region
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function(){
    var resObj = xhr.response;
    for(var i = 0; i<resObj.length; i++){
        console.log(resObj[i].subregion);
    }
}

//countries population
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function(){
    var resObj = xhr.response;
    for(var i = 0; i<resObj.length; i++){
        console.log(resObj[i].name.common);
        console.log(resObj[i].population);
    }
}

```
** **
4.https://medium.com/@reach2arunprakash/www-guvi-io-zen-d395deec1373

**Task 1**
** **
**1.Declare four variables without assigning values and print them in console**
```js
var a;
var b;
var c;
var d;

console.log(a);
console.log(b);
console.log(c);
console.log(d);
```

**2. How to get value of the variable myvar as output**
```js
var myvar= 1;
console.log(myvar);
```

**3. Declare variables to store your first name, last name, marital status, country and age in multiple lines**
```js
var firstName = "Nivetha";
var lastName ="Bharathi";
var maritalStatus = "Married";
var country = "India";
var age = 28;

console.log("My Firstname is "+ firstName);
console.log("My Lastname is "+ lastName);
console.log("My MaritalStatus is "+ maritalStatus);
console.log("My country is "+ country);
console.log("My age is "+ age);
```

**4. Declare variables to store your first name, last name, marital status, country and age in a single line**
```js
var firstName = "Nivetha", lastName ="Bharathi", maritalStatus = "Married", country = "India", age = 28;
```

**5.Declare variables and assign string, boolean, undefined and null data types**
```js
var myName = "Nivetha";
var age = 28;
var married = true;

console.log("My Name is "+ myName);
console.log("I am "+ age+ " years old");
console.log(married);

var a=null;
var b;

console.log(a);
console.log(b);
```

**6.Convert the string to integer
i)parseInt**
```js
var a=parseInt("10");
var b=parseInt("20");

console.log(a);
console.log(b);
console.log(parseInt("10.80"));
console.log(parseInt("10.00"));
console.log(parseInt("10.33")) ;
console.log(parseInt("34 45 66"));
console.log(parseInt("   60   "));
console.log(parseInt("40 years"));
console.log(parseInt("He was 40"));
console.log(parseInt("10", 10));
console.log(parseInt("010"));
console.log(parseInt("10", 8));
console.log(parseInt("0x10"));
console.log(parseInt("10", 16));
```
**ii)Number**
```js
console.log(Number(true)); //For booleans, Number() returns 0 or 1.
console.log(Number(false));

// console.log(Number(new Date())); //For dates, Number() returns milliseconds since January 1, 1970 00:00:00

console.log(Number("999 888"));
console.log(Number([9,9]));
console.log(Number([9.9]));
```
**iii)plus sign(+)**
```js
const x = "10";
let y;
y = +x;//It converts a string into a number.

console.log(y);
console.log(typeof y);
console.log(+'');
console.log(+'hello');
```

**7.Write 6 statement which provide truthy & falsey values**
    *undefined ,
     null , 
     NaN , 
     0 , 
     "" (empty string), and 
     false*


** **
**Task2**
** **
**1.Square of a number**
```js
console.log(Math.pow(3, 2));

console.log(Math.pow(12, 2));

console.log(Math.pow(4, 3));
```
**2.swapping two numbers**
```js
//using temporary variable
var a=99;
var b=10;
var temp = a;
a = b;
b = temp;

console.log(`The value of a after swapping: ${a}`);
console.log(`The value of b after swapping: ${b}`);

//using destructuring assignment
var x = 20;
let y = 55;
[x, y] = [y, x];

console.log(`The value of x after swapping: ${x}`);
console.log(`The value of y after swapping: ${y}`);
```
**3.Addition of 3 numbers**
```js
var a=10;
var b=20;
var c=30;
var k=a+b+c;

console.log("The sum of a,b,c are "+ k);
```
**4.Celsius to Fahrenheit conversion**
```js
var cTemp = 60;
var cToF = cTemp * 9 / 5 + 32;
var message =(`${cTemp}\xB0C is ${cToF}\xB0F`);

console.log(message);

//Fahrenheit conversion to Celsius
var fTemp = 140;
var fToC = (fTemp - 32) * 5 / 9;
var mes = (`${fTemp}\xB0F is ${fToC}\xB0C`);

console.log(mes);
```
**5.Meter to miles**
```js
var meter=12700;
var mile=meter/1609;

console.log(`${meter}m is ${mile}mi`);
```
**6.Pounds to kg**
```js
var p=5;
var kg=p*0.453592;

console.log(`${p}ibs is equal to ${kg}kg`);
```
**7.Calculate Batting Average**
```js
var runs = 10000;
var matches = 250;
var notOut = 50;
var battingAverage = runs/(matches-notOut);

console.log(battingAverage);
```
**8.Calculate five test scores and print their average**
```js
var s1 = 88;
var s2 = 89;
var s3 = 96;
var s4 = 92;
var s5 = 98;
var sum = s1+s2+s3+s4+s5;
var average = sum/5;

console.log(`The average of 5 test score is ${average}`);
```
**9.Power of any number x ^ y**
```js
var x = 5;
var y = 3;

console.log(Math.pow(x, y));
```
**10.Calculate Simple Interest**
```js
var p = 3000;
var n = 1;
var r = 7;
var sI = (p*n*r)/100;

console.log(`The Simple Interest is ${sI}`);
```
**11.Calculate area of an equilateral triangle**
```js
var a=20;
var area = (1.73*a*a)/4;

console.log(`The area of equilateral triangle is ${area}`);
```
**12.Area Of Isosceles Triangle**
```js
var base = 10;
var height = 20;
var area = (base*height)/2;

console.log(`The area of isosceles triangle is ${area}`);
```
**13.Volume of Sphere**
```js
var radius = 5;
volume = (4/3) * Math.PI * Math.pow(radius, 3);
volume = volume.toFixed(4);

console.log(`The volume of sphere is ${volume}`);
```
**14.Volume Of Prism**
```js
//volume of triangular prism = (l*b*h)/2
//volume of rectangular prism = l*w*h
//volume of square prism = a*a*l
//volume of pentagonal prism = (a*b*h)/5
//volume of triangular prism = 3*a*b*h
var l = 18;
var b = 12;
var h = 9;
volume = (l * b * h) / 2;

console.log(`The volume of triangular prism is ${volume}`);
```
**15.Area of triangle**
```js
var l = 10;
var b = 12;
var area = (l*b)/2;

console.log(`The area of triangle is ${area}`);
```
**16.Give the Actual cost and Sold cost, Calculate Discount Of Product**
```js
var actual = 100;
var sold = 50;
var discount =((actual-sold)*100)/actual;

console.log(`Discount of a product is ${discount}%`);
```
**17.Given their radius of a circle and find its diameter, circumference and area.**
```js
var r = 5;
var diameter = 2 * r;
var circumference = 2 * Math.PI * r;
circumference = circumference.toFixed(3);

var area = Math.PI * r * r;
area = area.toFixed(4);

console.log(`The diameter of circle is ${diameter}`);
console.log(`The circumference of circle is ${circumference}`);
console.log(`The area of circle is ${area}`);
```
**18.Given two numbers and perform all arithmetic operations**
```js
//Addition
var a=10;
var b=2;
var x=a+b;
console.log(`Addition of ${a} and ${b} is ${x}`);

//subtraction
var y=a-b;
console.log(`subtraction of ${b} from ${a} is ${y}`);

//Multiply
var z =a*b;
console.log(`Multiply of ${a} and ${b} is ${z}`);

//Division
var d=a/b;
console.log(`Division of ${a} by ${b} is ${d}`);

//Modulus
var m = a%b;
console.log(`Remainder is ${y}`);

//Exponentiation
console.log(a**b);//a ** b produces the same result as Math.pow(a,b)
```
**19.Display the asterisk pattern as shown below(No loop needed):
```js
var str = "*****\n*****\n*****\n*****\n*****";
console.log(str);

//with loop
let n = 5; // row or column count
let string = "";// defining an empty string

for(let i = 0; i < n; i++) { // external loop
  for(let j = 0; j < n; j++) { // internal loop
    string += "*";
  }
  string += "\n";// newline after each row
}
console.log(string);
```
**20.Calculate electricity bill? For example, a consumer consumes 100 watts per hour daily for one month. Calculate the total energy bill of that consumer if per unit rate is 10?**
```js
var p=0.1; //1unit = 1000watts 0r 1kw
var t=1; //per hour daily
var e=p*t; //energy consumed per day
var emonth=30*e; //total energy consumed per month
var cost=10;
var bill=cost*emonth;

console.log(`Total electricity bill per month is Rs.${bill}`);
```
**21.Calculate CGPA**
```js
var percentage=70;
var cgpa = percentage/9.5;
cgpa=cgpa.toFixed(1);

console.log(`${cgpa}CGPA`);
```

** **
**Task 3**
** **
**1. Write a loop that makes seven calls to `console.log` to output the following triangle:**
    #
    ##
    ###
    ####
    #####
    ######
    #######
```js
let n = 7;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < i; j++) {
    string += "#";
  }
  string += "\n";
}

console.log(string);
```

**2.write a code to count the elements in the array . Don’t use length property**
```js
var a=[11,22,33,44,55];

function arrayLength(){
  var length=0;
    while(a[length]!=undefined){
      length++;
    }
  return length;
}

console.log(arrayLength(a));
```

**2. ii) Declare an empty array**
```js
let arr= [9,5,4,3,7];
arr=[];
console.log(arr);

let g= [9,5,4,3,7];
g.length=0;
console.log(g);
```

**3.Create an array called foods holds the names of your top 20 favorite foods, starting with the best food.**
```js
let food = ["Fish Curry", "Fish Fry", "Chicken65", "Mutton Chukka", "Briyani", "Dhosa", "Chappathi", "Poori", "Parotta", "Naan", "Idly", "Paneer", "Gopi65", "Maggie", "Sambar", "Dry Fish", "Aviyal", "Rasam", "Idiyappam", "Appam"]

console.log(food.length);

//find your fifth favorite food
console.log(food[4]);
```

**4.Starting from the existing friends variable below, change the element that is currently “Mari” to “Munnabai”.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

function dataHandling(input){
    let index = input.indexOf('Mari');
    input[index]="Munnabai";
    console.log(input);
}
dataHandling(friends);
```
**5.Starting from the friends variable below, Loop and Print the names till you meet CaptianAmerica.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

function dataHandling(input){
    for(let i=0; i<input.length; i++){
        console.log(input[i]);
        if(input[i] == "CaptianAmerica"){
            break;
        }
    }
}
dataHandling(friends);
```
**6.Find the person is ur friend or not.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

function dataHandling(input, frnd){
    for(let i=0; i<input.length; i++){
        if(input[i] == frnd){
          return true
        }
    }
}
let res=dataHandling(friends, "Jeff");
console.log(res);
```
**7.We have two lists of friends below. Use array methods to combine them into one alphabetically-sorted list.**
```js
var friends1 = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];
var friends2 = ["Gabbar", "Rajinikanth", "Mass", "Spiderman", "Jeff", "ET"];

function dataHandling(input){
    var combine = input[0].concat(input[1]);
    combine.sort();
    return combine;
}
let result= dataHandling([friends1, friends2]);
console.log(result);
```

** **
**1.Get the first item, the middle item and the last item of the array**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];
//first item
console.log(friends[0]);

//last item
last = friends.length - 1;
console.log(friends[last]);

//middle item
var middle = friends[Math.floor(friends.length / 2)];
console.log(middle);
```
**2. Add your name to the end of the friends array, and add another name to beginning.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];
//add at end
friends.push("Nivetha");
console.log(friends);

//add at beginning
friends.unshift("Balaji");
console.log(friends);
```
**3.Add Mr or Ms to the names in the friends array.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

const modify =friends.map(name=>`Mr.${name}`);

console.log(friends);
console.log(modify);
```
**4. Concat all the names the friends array and return as comma “,” seperated string.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];
let j=friends.join();

console.log(j);
```
**5. Find the friends names who has letter ‘a’ and return the list.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

for(var i = 0; i < friends.length; i++)
{
    if(friends[i].indexOf('a') != -1)
    {
        console.log(friends[i]);
    }
}
```
**6.Find the avg length of all the friends names. Get the individual length of the names and do the avg.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

avg = friends.join('').length / friends.length;

console.log(avg);
```
**7. Find the names and return the list starting with letter M.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

for(var i = 0; i < friends.length; i++)
{
    if(friends[i].startsWith("M") == true)
    {
        console.log(friends[i]);
    }
}
```
**8. Find the name with max characters and return the name.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

var lgth = 0;
var longest;

for (var i = 0; i < friends.length; i++) {
  if (friends[i].length > lgth) {
    var lgth = friends[i].length;
    longest = friends[i];
  }
}
```
**9. Find the name with min characters and return the name.**
```js
let friends = ["Mari", "MaryJane", "CaptianAmerica", "Munnabai", "Jeff", "AAK chandran"];

console.log(
    friends.reduce((a, b) => a.length <= b.length ? a : b)
  )
```
**1.Print the contents of the input variable**
```js
var input = [
    ['0001', 'Roman Alamsyah', 'Bandar Lampung', '21/05/1989', 'Membaca'],
    ['0002', 'Dika Sembiring”', 'Medan', '10/10/1992', 'Bermain Gitar'],
    ['0003', 'Winona', 'Ambon', '25/12/1965', 'Memasak'],
    ['0004', 'Bintang Senjaya', 'tMartapura', '6/4/1970', 'Berkebun']
    ]
    
    function dataHandling(input){
    for (var i = 0; i < input.length; i++) {
    //Your code goes here
    var x=input[i];
    var num=x[0];
    var name=x[1];
    var city=x[2];
    var dob=x[3];
    var hobby=x[4];
    console.log(`The rollno. is ${num}`);
    console.log(`The name is ${name}`);
    console.log(`The city is ${city}`);
    console.log(`The date of birth is ${dob}`);
    console.log(`The hobby is ${hobby}`);
    }
    }
    
    dataHandling(input);
```
**2.Add a new key value pair to myobject  
  key : ten  
  value : ten**
```js
myobject = {1:"one","11":1,"name":"arun"};
myobject["ten"]="ten";
console.log(myobject);
```
**3.Write out an object literal to represent the data below.
  Guvi, Geek, 6, IIT-M RP,Chennai.**
```js
var addr= {
    Name : "guvi, geek",
    location : "6, IIT-M RP",
    city : "Chennai"
};
console.log(addr);
```
**4.How would you represent the following data using a combination of object literals and arrays? (You can describe a strategy without typing or writing out the whole thing.)**

Guvi, Geek, 6, IIT-M RP,Chennai.  
Amazon, Inc, 31, SP Infocity, Chennai.  
Google, Alphabet, 34 Amphitheater Parkway, MountainView.  
Tesla, Inc , 32, 333 Santana Row,San Jose.
```js

var addr=[{
    Name : "guvi, geek",
    location : "6, IIT-M RP",
    city : "Chennai."
},
{
    Name : "Amazon, Inc",
    location : "31, SP Infocity",
    city : "Chennai."
},
{
    Name : "Google, Alphabet",
    location : "34 Amphitheater Parkway",
    city : "MountainView."
},
{
    Name : "Tesla, Inc ",
    location : "32, 333 Santana Row",
    city : "San Jose."
}];

console.log(addr);

```