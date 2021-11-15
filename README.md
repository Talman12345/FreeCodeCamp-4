# FreeCodeCamp-4


61  // Setup
const myArr = [2, 3, 4, 5, 6];

// Only change code below this line
let total = 0;
for(let i=0;  i< myArr.length; i++){
  total += myArr[i] ;
}



62  function multiplyAll(arr) {
  let product = 1;
  // Only change code below this line
for (let i = 0; i < arr.length; i++) {
  for (let j = 0; j < arr[i].length; j++){
product *= arr[i][j]  }
}  
  // Only change code above this line
  return product ;
  

}

multiplyAll([[1, 2], [3, 4], [5, 6, 7]]);



63  // Setup
const myArray = [];
let i = 10;

// Only change code below this line
do{
  myArray.push(i);
  i++
} while(i<10)


64   function sum(arr, n) {
  // Only change code below this line
if(n<= 0){
  return 0;
}else{
  return sum (arr, n - 1) + arr[n-1] ;
}
  // Only change code above this line
}


65  // Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line

  for (let x = 0; x < contacts.length; x++) {
    if (contacts[x].firstName === name) {
      if (contacts[x].hasOwnProperty(prop)) {
        return contacts[x][prop];
      } else {
        return "No such property";
      }
    }
  }
  return "No such contact";

  // Only change code above this line
}

lookUpProfile("Akira", "likes");


66   function randomFraction() {

  // Only change code below this line

  return Math.random();

  // Only change code above this line
}

67  function randomWholeNum() {

  // Only change code below this line

  return Math.floor(Math.random()*10);
}

68   function convertToInteger(str) {
  return parseInt(str)
  }
  
  convertToInteger("56");


69   function convertToInteger(str) {
  return parseInt(str, 2)
 }
 
 convertToInteger("10011");


 70  function checkEqual(a, b) {
  return a===b ?"Equal":"Not Equal"
 }
 
 checkEqual(1, 2);


 71  function checkSign(num) {
  return num>0 ? "positive" : num<0 ? "negative": "zero"
  }
  
  checkSign(10);


  72  function rangeOfNumbers(startNum, endNum) {
    if(startNum == endNum){
      return [startNum]
    }else{
      var numbers = rangeOfNumbers(startNum, endNum - 1);
        numbers.push(endNum);
        return numbers;
    }
    
     };


     73  function checkScope() {
      let i = 'function scope';
       if (true) {
         let i = 'block scope';
         console.log('Block scope i is: ', i);
       }
       console.log('Function scope i is: ', i);
       return i;
     }



     74  const s = [5, 7, 2];
     function editInPlace() {
       // Only change code below this line
     s[0] = 2;
     s[2] = 7;
     s[1] = 5;
     
     
       // Using s = [2, 5, 7] would be invalid
     
       // Only change code above this line
     }
     editInPlace();




     75   function freezeObj() {
      const MATH_CONSTANTS = {
        PI: 3.14
      };
      // Only change code below this line
    Object.freeze(MATH_CONSTANTS)
    
      // Only change code above this line
      try {
        MATH_CONSTANTS.PI = 99;
      } catch(ex) {
        console.log(ex);
      }
      return MATH_CONSTANTS.PI;
    }
    const PI = freezeObj();


    76 const magic = () => new Date();

    77   const myConcat=(arr1, arr2) => arr1.concat(arr2);

    console.log(myConcat([1, 2], [3, 4, 5]));


    78  // Only change code below this line
    const increment = (number, value = 1) => number + value;
    // Only change code above this line


    79   const sum = (...args) => {
 
      return args.reduce((a, b) => a + b, 0);
    }
    console.log(sum(1,2,3))


    80   const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
let arr2;

arr2 = [...arr1];  // Change this line

console.log(arr2);
