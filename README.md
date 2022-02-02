## core-code
Core Code bootcamp
## Week1 Tuesday

##### 2.Java can be considered both a compiled and an interpreted language.

##### 3. monedaGT * monedaUS = tipoCambio

##### 5.PseudoCode = algoritms, it helps to explain what we want to do in a simple way 

##### 6.const yearOfBirth = 1990; const edge = (yearOfBirth) =>{ actualYear = 2022; console.log('your edge is: ', actualYear - yearOfBirth);} 

##### 8.the flowcharts are important because it allow us to plan and think about our project before starting.

## Week1 Wednesday

##### 2.Year of birth in decimal 1990, in binary 11111000110, in hexa 7c6.

##### 3. 51966 in binary 1100101011111110, in hexa cafe and 16fe.


.data
	msg: .asciiz "Ingrese el primer numero: \n"
	msg2: .asciiz "Ingrese el segundo numero: \n"
	msg3: .asciiz "El resultado es: \n"	
.text
	main:
		li $v0, 4
		la $a0, msg
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, msg2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0

		
      		
      		add $t2, $t0, $t1
      		
      		li $v0,4
      		la $a0, msg3
      		syscall
      		
      		li $v0,1
      		move $a0,$t2
      		syscall
      		

## Week2 challenges (Tuesday)
###### 1 Solution
````
function multiply(a, b){
  return a * b
}

###### 2 Solution
function uniTotal (string) {
let counter = 0;
  for(let i = 0, length = string.length; i<length; i++){
    counter+=string.charCodeAt(i);
  }
  return counter;
}
````

###### 3 Solution
````
function getChar(c){
  return String.fromCharCode(c);
}
````

###### 4 Solution
````
function addBinary(a,b) {
 let c = a+b;
  let cBinary = c.toString(2);
  return cBinary;
}
````

##### 5 Solution
````
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10) {
    
    return 100;
  }
  
  if(exam > 75 && projects >= 5) {
     return 90;
  }
  
  if(exam > 50 && projects >= 2) {
    return 75;
  }
  
  return 0;   
  
}
````

## Week2 challenges (Wednesday)
###### 1 Solution
````
function dutyFree(normPrice, discount, hol){
  let realDiscount = (normPrice/100)*discount;
return Math.floor(hol/realDiscount);
}
````

###### 2 Solution
````
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs((sonYearsOld*2)-dadYearsOld);
}
````

###### 3 Solution
````
function validSpacing(s) {
  if(s.length == 0) return true;
  if(s[0]== ' ' || s[s.length-1]== ' ') return false;
  
  let aSpaces0 = s.split(' ');
  
  for(let i =0, length = aSpaces0.length; i<length; i++){
      if(aSpaces0[i] == '') return false;
  }
  return true;
}
````

###### 4 Solution
````
function fakeBin(x){  
  let array=[];
  for(let i = 0, length = x.length; i< length; i++){
    let numero = Number(x[i]);    
    if(numero < 5){
    array.push('0');
      console.log(array);
    }
    if(numero >= 5){
      array.push('1');
    console.log(array);
  }
  }
  return array.join('');
}
````

## Week 2 challenges (Thursday)
###### 1 Solution
````
function remove (string) {  
  while(string && string.slice(-1)=='!'){
   string = string.slice(0,-1);
 }
  return string;
}
````

###### 2 Solution
function shortcut (string) {
  return string.replace(/[aeiou]/g, '');
}

###### 3 Solution
````
const rps = (p1, p2) => {
  if(p1==p2)
    return 'Draw!';
  if(p1=='rock' && p2=='scissors')
    return 'Player 1 won!';
  if(p1=='scissors' && p2=='paper')
    return 'Player 1 won!';
  if(p1=='paper' && p2=='rock')
    return 'Player 1 won!';
  else
    return 'Player 2 won!';
};
````

###### 4 Solution
````
function persistence(num) {
   for (var i = 0; num > 9; i++) {
     num = num.toString().split('').reduce((valorAnterior, valorActual) => valorAnterior * valorActual);
   }
   return i;
}

````
###### 5 Challenge
````
1 - I'm Jorge Gómez, I currently work as a software developer.
2 - my skills include, html5, css3, jquery, bootstrap, php, javascript, nodejs, angularjs, ionic, mysql and mongodb.
3 - I want to lead large projects, contribute and execute effectively.
4 - I want to continue specializing in new and demanded technologies, after that my goal is to direct large important projects for important people and companies.
5 - Responsibility, Loyalty, Commitment, Honesty.
````

## Week 3 challenges (Monday)
###### 1 Solution
````
function likes(names) {
   if(names.length==0){
     return 'no one likes this';
   }
  if(names.length==1){
    return names[0]+' likes this';
  }
  
  if(names.length==2){
    return names[0]+' and '+names[1]+' like this';
  }
  
  if(names.length==3){
    return names[0]+', '+names[1]+' and '+names[2]+' like this';
  }
 
  if(names.length>3){
    let num = names.length-2;
    return names[0]+', '+names[1]+' and '+num+' others like this';
  }
  
}
````

###### 2 Solution
````
var countBits = function(n) {
  let binary = n.toString(2);
  let counter = 0;
  for(let i=0, length = binary.length; i<length; i++){
    if(binary[i]=='1'){
      counter+=1;
    }
  }
  
  return counter;
  
  
};
````

###### 3 Solution
````
decodeMorse = function(morseCode){
  let string = '';
  let counterWords = 1;
  let arrayWords = morseCode.trim().split('   ');
  
  arrayWords.forEach(word => {
    let letters = word.split(' ');
    
    letters.forEach(letter =>{
      string+=MORSE_CODE[letter]
    })
    if(counterWords != arrayWords.length){
      string+=' ';
    }
    
    counterWords++;
    
  });
  
  return string;
}
````

## Week 3 challenges (Tuesday)
###### 1 Solution
````
function order(words){  
  return words.split(' ').sort((a,b)=>{
    return a.match(/\d/) - b.match(/\d/);
  }).join(' ');
}
````

###### 2 Solution
````
function duplicateCount(text){
  return (text.toLowerCase().split('').sort().join('').match(/([^])\1+/g) || []).length;
}
````

###### 3 Solution
````
function pigIt(str){
 return arr = str.split(' ').map(word => `${word.substr(1)}${word.substr(0, 1)}ay `).join('').trim();  
}
````

## Week 3 challenges (Wednesday)
###### 1 Solution
````
function validParentheses(parens){
  let res = 0;  
  for (var i = 0; i < parens.length; i++) {
    if(parens[i]=='(') res+=1;
    if(parens[i]==')') res-=1;
         if(res<0) return false;
  }  
    return res==0;
}
````

###### 2 Solution
````
function toCamelCase(str){
  let words = str.split('');  
  return words.map(function(elemento, indice){
    if(elemento == '-' || elemento == '_'){
      elemento = words[indice+1].toUpperCase();
      words.splice(indice+1, 1);
    }
    return elemento;
  }).join('');
}
````

###### 3 Solution
````
function uniqueInOrder(iterable){

  const res = [ ]

  for(let i = 0; i < iterable.length; i++){
  
    if(iterable[i] !== iterable[i+1]){
      res.push(iterable[i])
    }
  
  }

  return res
}
````


## Week 3 challenges (Thursday)
###### 1 Solution
````

````

###### 2 Solution
````
function encryptThis(text) {
  let strArr = text.split(' ');
  let output = [];
  
  strArr.forEach(str => {
    if (str.length === 1) {
      output.push(str.charCodeAt(0));
    } 
    else {
      let tempStr = str.split('');
      tempStr[0] = str.charCodeAt(0);
      tempStr[1] = str[str.length - 1];
      tempStr[str.length - 1] = str[1];
      output.push(tempStr.join(''));
    }
  });
  
  return output.join(' ');
}

````

###### 3 Solution
````
function list(arr){  
  const coma = ', ';
  const sign =' & ';
 return arr.reduce((pre, curr, indice)=>`${pre}${(indice==arr.length-1 ? sign : coma)}${curr.name}`, '').slice(2).trim();
}
````

###### Friday Test 1 Solution 
````
function computeCheckDigit(identificationNumber) {  
  var string = identificationNumber.toString();
  arrayPar=[];
  arrayInpar=[];  
  for(let i=0, length=string.length; i<length; i++){
    if(i%2==0){
      arrayPar.push(string[i]);
    }else{
      arrayInpar.push(string[i]);
    }    
  }
 
  arrayPar = arrayPar.map(x => parseInt(x));
  arrayInpar = arrayInpar.map(x=> parseInt(x));
 
  arrayPar = arrayPar.reduce((pre, act)=>{
    return pre+act;
  });
  
  resPar = arrayPar*3;
  
  arrayInpar = arrayInpar.reduce((pre, act) => {
    return pre+act;
  });
  
  resInpar = arrayInpar+resPar;
  
  resInpar = String(resInpar).split("").map((resInpar)=>{
  return Number(resInpar)
})
  
  return 10-resInpar.pop();
  
  
}
````

## Week 4 challenges (Tuesday)
###### challenge => [exercise 1](https://typescript-exercises.github.io/#exercise=1 "Exercise 1")
###### 1 Solution
````

export interface User {
    name: string,
    age: number,
    occupation: string
};

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
````
