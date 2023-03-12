# Java Script

- Comment : Single line and Multiple Line

In JavaScript, you can add single line comments by using `//` before your comment. You can add multiple line comments by using `/* */` before and after your comment.

# JavaScript has 8 Datatypes

```jsx
// Numbers:
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");
```

# **Conditional Statements**

```jsx
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

# **Loops**

# The For In Loop

The JavaScript `for in` statement loops through the properties of an Object:

# The For Of Loop

The JavaScript `for of` statement loops through the values of an iterable object.

It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:

```jsx
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}

const person = {fname:"John", lname:"Doe", age:25};

//for in 
let text = "";
for (let x in person) {
  text += person[x];
}

//for of
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}

```

# Object

Objects are variables too. But objects can contain many values.

```jsx
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

# Function

```jsx
let x = myFunction(4, 3);   // Function is called, return value will end up in x

function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
}
```

# Events

Examples of HTML events:

- When a user clicks the mouse
- When a web page has loaded
- When an image has been loaded
- When the mouse moves over an element
- When an input field is changed
- When an HTML form is submitted
- When a user strokes a key

The `onload`and `onunload` events are triggered when the user enters or leaves the page.

The `onchange` event is often used in combination with validation of input fields.

The `onmouseover` and `onmouseout` events can be used to trigger a function when the user mouses over, or out of, an HTML element:

The `onmousedown`, `onmouseup`, and `onclick` events are all parts of a mouse-click. First when a mouse-button is clicked, the onmousedown event is triggered, then, when the mouse-button is released, the onmouseup event is triggered, finally, when the mouse-click is completed, the onclick event is triggered.

# Let vs Var vs Const

![Untitled](Java%20Script%20780fa1f4dbf14ed7ab22fac0ed918491/Untitled.png)

- JSON
- Storage: Session and Local — How do we store JSON
- DOM - Document Object Model
- Event

# **JS HTML**

— Element - Tag Node

— ID, Class - Attribute Node

— Value/text - Text Node

- They are two way to link js in html Embedded and External.
- **External**

 

```jsx
<script src="jsExternal.js" type="text/javascript"></script>
```

- **Embedded**

```jsx
<script type="text/javascript">
        document.write("<h1>Heading 1 </h1> </br>");
    </script>
```

### **Condition**

```jsx
let num = 32;

// If Statement 
if(num > 0) document.write("<p>Positive</P>");
else if(num < 0) document.write("<p>Negative</P>");
else document.write("0");

//Switch Statment 
switch(num){
    case 1: document.write("Sunday");
            break;
    case 2: document.write("Monday");
            break;
    case 3: document.write("Tuesday");
            break;
    case 4: document.write("Wednesday");
            break;
    case 5: document.write("Thursday");
            break;
    case 6: document.write("Friday");
            break;
    case 7: document.write("Saturday");
            break;
    default: document.write("Incorrect Input");
}
```

### function

```jsx
function addTwoNum(a,b){
     return a+b;
}

document.write(addTwoNum("Mike"," Mebrate"));
```

### Array

.code

```jsx
var a = ["Mike", "Mebrate", "Degefu"];
a.push("Kaleab")
a.pop();
a.reverse();

for(var b in a){
    document.write(a[b] + " ");
}

// -- Mike Mebrate Degefu
document.write("</br> </br>")

for(var b of a){
    document.write(b+ " ");
}

// -- Mike Mebrate Degefu
document.write("</br> </br>")

for(var i=0; i <a.length; i++){
    document.write(a[i]+ " ");
}

// -- Mike Mebrate Degefu
```

# DOM Manipulation

1. getElementByID

```jsx
<button class="btn btn-primary m-5" onclick="btnClickAlert()">Click me</button>

function btnClickAlert(){
    alert("Button Clicked");
}

<button class="btn btn-primary m-5" onclick="btnClickHead()">Click me</button>
    <h2 id="h2" class="ms-5">Unclicked</h2>
function btnClickHead(){
    document.getElementById("h2").innerHTML = "Clicked";
}

```

1.1. Value of Input Box

```jsx
//Value of Input

function valueOfInput(){
    var nameValue = document.getElementById("nameId").value;
    var ageValue = document.getElementById("ageId").value;
    var print = document.getElementById("print");
    print.innerHTML = nameValue + " " + ageValue; 
}

<div class="conainer m-3">
    <input type="text" name="" id="nameId" placeholder="Name">
    <input type="number" name="" id="ageId" placeholder="Age">
    <button type="submit" onclick="valueOfInput()" class="btn btn-primary">Submit</button>

    <p id="print"></p>
   </div>
```

1.2. Value of Input Value

```jsx
<div class="container m-3">
        <input type="radio" value="JS" name="rd" id="rd1"> JS
        <input type="radio" value="CS" name="rd" id="rd2"> CS <br>
        <button type="submit" class="btn btn-primary" onclick="valueOfRadio()">Submit</button>
    </div>

function valueOfRadio(){
    var rd1 = document.getElementById("rd1");
    var rd2 = document.getElementById("rd2");

    if(rd1.checked == true){
        alert(rd1.value);
    }else if(rd2.checked == true){
        alert(rd2.value);
    }else alert("Non of them selected");
}
```

1.3. Select Option Box Value

```jsx
div class="container m-3">
        <select name="" id="selectBtn">
            <option value="Select One">Select One</option>
            <option value="Select TWo">Select Two</option>
            <option value="Select Three">Select Three</option>
        </select>
        <button type="submit" class="btn btn-primary" onclick="valueOfSelect()">Submit</button>
    </div>

function valueOfSelect(){
    var selectOption = document.getElementById("selectBtn");
    alert(selectOption.options[selectOption.selectedIndex].value);
}

```

1. getElementByTagName

```jsx
div class="container mt-3">
        <p>This is paragraph 1</p>
        <p>This is paragraph 2</p>
        <p>This is paragraph 3</p>
        <p>This is paragraph 4</p>
        <p>This is paragraph 5</p>
        <p>This is paragraph 6</p>
    
        <button type="button" class="btn btn-primary" onclick="changeStyle()" >Increase Font</button>
    </div>

function changeStyle(){
    var incFont = document.getElementsByTagName("p");
    incFont[1].style.fontSize ='25px';

    for(let a in incFont){
       incFont[a].style.fontSize = '40px';
    }
}
```

1. getElementByClassName

```jsx
<div class="container mt-3">
        <p class="pp">This is paragraph 1</p>
        <p>This is paragraph 2</p>
        <p>This is paragraph 3</p>
        <p class="pp">This is paragraph 4</p>
        <p>This is paragraph 5</p>
        <p>This is paragraph 6</p>
    
        <button type="button" class="btn btn-primary" onclick="changeStyleByClass()" >Increase Font</button>
    </div>

function changeStyleByClass(){
    var elem = document.getElementsByClassName('pp');
    elem[0].style.fontSize = '30px';

    for(let i in elem){
        elem[i].style.color = 'tomato';
    }
}
```

Event - OnHover

- Also change the image when it’s hover document.getElementByID(”imgMike”).src();

```jsx

<div class="container mt-3">
       <img src="Image/myPic.jpg" alt="" id="imgMike" width="200px" onmouseout="hoverOut()" onmouseover="hoverMouse()">
    </div>

function hoverMouse(){
    var imgHover = document.getElementById("imgMike");
    imgHover.style.width="300px";
}

function hoverOut(){
    var imgHoverOut = document.getElementById("imgMike");
    imgHoverOut.style.width="200px";
}
```

## Form Validation

```jsx
<div class="container mt-3">
       <form onsubmit="return validate()" action="welcome.html"  >
    Username: <input type="text" class="mt-3" name="" id="uname"> <br>
       Password: <input type="password"  class="mt-3"  name="" id="pass"> <br>
       <button type="submit" class="btn btn-primary ms-3 mt-3">Login</button>
    </form>
    </div>

function validate(){
    var username = document.getElementById("uname");
    var password = document.getElementById("pass");

    if(username.value.trim() == "" || password.value.trim() == ""){
       alert("Empty");
       return false;
    }else return true;
}
```

- With Labels

```jsx
<div class="container mt-3">
       <form onsubmit="return validate()" action="welcome.html"  >
    Username: <input type="text" class="mt-3" name="" id="uname">
    <label for="uname" id="labeluname"  style=" color: tomato; visibility: hidden; " >Invalid</label> <br>
       Password: <input type="password"  class="mt-3"  name="" id="pass"> <br>
       <button type="submit" class="btn btn-primary ms-3 mt-3">Login</button>
    </form>
    </div>

function validate(){
    var username = document.getElementById("uname");
    var password = document.getElementById("pass");
    
    if(username.value.trim()=="" && password.value.trim()==""){
        username.style.border ="solid 2px tomato";
        password.style.border = "solid 2px tomato";
        return false;
    }
    else if(username.value.trim()==""){
        username.style.border ="solid 2px tomato";
        document.getElementById("labeluname").style.visibility="visible"
        return false;
    }else if(password.value.trim()==""){
        password.style.border = "solid 2px tomato";
        return false;
    }else return true;
}
```

## Pattern Checking

```jsx

<div class="container m-4">
        <input type="text" name="" id="usernamePatter" placeholder="username">
        <label for="usernamePatter" id="lebelus" style="color:tomato; visibility: hidden;">Invalid</label>
        <button type="button" class="btn btn-primary" onclick="return patternCheck()">Login</button>
    </div>

function patternCheck(){
    var username = document.getElementById("usernamePatter").value;
    var pattern = /E00/;    // /[a-x]00 the word contain a-x and followed by 00
// /E00/i  -> for capital and small letters
// /[^ws]abd/  -> to exlcude ws 

    if(pattern.test(username)){
        document.getElementById("lebelus").innerHTML="Success";
        document.getElementById("lebelus").style.visibility="visible";
    }else{
        document.getElementById("lebelus").style.visibility="visible";
    }
}
```

- **Practice Questions**

```jsx
function incrementPara(){
    var paragraph = document.getElementById("paraInc");
    var getFontSize = getComputedStyle(paragraph,null).getPropertyValue("font-size")
    var size = parseInt(getFontSize);

    paragraph.style.fontSize = size + 1 + "px";
}

function getValueOfAttribute(){
    var anchor = document.getElementById("hrefLink").getAttribute("href");
    alert(anchor);
}

function printDiv(){
    var org = document.body.innerHTML;
    var content = document.getElementById("printThisDiv").innerHTML;

    document.body.innerHTML = content;
    window.print();
    document.body.innerHTML = org;
}

function getDateTime(){
    var getDate = new Date();
    var day = getDate.getDay();
    var CurreDay = getDate.getDate();
    var CurreMonth = getDate.getMonth();
    var CurreYear = getDate.getFullYear();
    var returnDay="";

    if(day == 1) returnDay = "Monday";
    else if(day == 2) returnDay = "Tuesday";
    else if (day == 3) returnDay = "Wednesday";
    else if (day == 4) returnDay = "Thursday";
    else if (day == 5) returnDay = "Friday";
    else if (day == 6) returnDay = "Saturday";
    else returnDay = "Sunday";

   document.getElementById("day").innerHTML = returnDay;
   document.getElementById("Cutime").innerHTML = CurreMonth + "/" + CurreDay+ "/"+CurreYear;

}

var arrayStore = new Array();
function arrayItem(sign){
 var inputItem = document.getElementById("inputIntoArray");

 if(sign == "add"){
    arrayStore.push(inputItem.value);
    inputItem.value="";
 }else{
    var prinedItem ="";
    for(let i=0; i < arrayStore.length; i++){
      prinedItem+="Element "+ i +"= " + arrayStore[i]+"</br>";
    }

    document.getElementById("displayArrayItem").innerHTML=prinedItem;
 }
}
```
