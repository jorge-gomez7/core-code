## Core Code BootCamp

## Week1 Tuesday

##### 2.Java can be considered both a compiled and an interpreted language.

##### 3. monedaGT * monedaUS = tipoCambio

##### 5.PseudoCode = algoritms, it helps to explain what we want to do in a simple way 

##### 6.const yearOfBirth = 1990; const edge = (yearOfBirth) =>{ actualYear = 2022; console.log('your edge is: ', actualYear - yearOfBirth);} 

##### 8.the flowcharts are important because it allow us to plan and think about our project before starting.

## Week1 Wednesday

##### 2.Year of birth in decimal 1990, in binary 11111000110, in hexa 7c6.

##### 3. 51966 in binary 1100101011111110, in hexa cafe and 16fe.

````
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
````

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

###### challenge => [exercise 2](https://typescript-exercises.github.io/#exercise=2 "Exercise 2")
###### 2 Solution
````

interface User {
    name: string;
    age: number;
    occupation: string; 
}

interface Admin {
    name: string;
    age: number;
    role: string;
}



export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
````

###### challenge => [exercise 3](https://typescript-exercises.github.io/#exercise=3 "Exercise 3")
###### 3 Solution
````

interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(person: Person) {
    let additionalInformation: string;
    if ('role' in person) {
        additionalInformation = person.role;
    } else {
        additionalInformation = person.occupation;
    }
    console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
}

persons.forEach(logPerson);
````

###### challenge => [exercise 4](https://typescript-exercises.github.io/#exercise=4 "Exercise 4")
###### 4 Solution
````

interface User {
    type: 'user';
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    type: 'admin';
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    { type: 'user', name: 'Max Mustermann', age: 25, occupation: 'Chimney sweep' },
    { type: 'admin', name: 'Jane Doe', age: 32, role: 'Administrator' },
    { type: 'user', name: 'Kate Müller', age: 23, occupation: 'Astronaut' },
    { type: 'admin', name: 'Bruce Willis', age: 64, role: 'World saver' }
];

export function isAdmin(person: Person) {
    return person.type === 'admin';
}

export function isUser(person: Person) {
    return person.type === 'user';
}

export function logPerson(person: Person) {
    let additionalInformation: string = '';
    if (isAdmin(person)) {
        additionalInformation = person.type;
    }
    if (isUser(person)) {
        additionalInformation = person.type;
    }
    console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
}

console.log('Admins:');
persons.filter(isAdmin).forEach(logPerson);

console.log();

console.log('Users:');
persons.filter(isUser).forEach(logPerson);
````

###### challenge => [exercise 5](https://typescript-exercises.github.io/#exercise=5 "Exercise 5")
###### 5 Solution
````

interface User {
    type: 'user';
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    type: 'admin';
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    { type: 'user', name: 'Max Mustermann', age: 25, occupation: 'Chimney sweep' },
    {
        type: 'admin',
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        type: 'user',
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        type: 'admin',
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    },
    {
        type: 'user',
        name: 'Wilson',
        age: 23,
        occupation: 'Ball'
    },
    {
        type: 'admin',
        name: 'Agent Smith',
        age: 23,
        role: 'Administrator'
    }
];

export const isAdmin = (person: Person): person is Admin => person.type === 'admin';
export const isUser = (person: Person): person is User => person.type === 'user';

export function logPerson(person: Person) {
    let additionalInformation = '';
    if (isAdmin(person)) {
        additionalInformation = person.role;
    }
    if (isUser(person)) {
        additionalInformation = person.occupation;
    }
    console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
}

export function filterUsers(persons: Person[], criteria: Partial<Omit<User, 'type'>>): User[] {
    return persons.filter(isUser).filter((user) => {
        const criteriaKeys = Object.keys(criteria) as (keyof Omit<User, 'type'>)[];
        return criteriaKeys.every((fieldName) => {
            return user[fieldName] === criteria[fieldName];
        });
    });
}

console.log('Users of age 23:');

filterUsers(
    persons,
    {
        age: 23
    }
).forEach(logPerson);
````


###### challenge => [exercise 6](https://typescript-exercises.github.io/#exercise=6 "Exercise 6")
###### 6 Solution
````

interface User {
    type: 'user';
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    type: 'admin';
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    { type: 'user', name: 'Max Mustermann', age: 25, occupation: 'Chimney sweep' },
    { type: 'admin', name: 'Jane Doe', age: 32, role: 'Administrator' },
    { type: 'user', name: 'Kate Müller', age: 23, occupation: 'Astronaut' },
    { type: 'admin', name: 'Bruce Willis', age: 64, role: 'World saver' },
    { type: 'user', name: 'Wilson', age: 23, occupation: 'Ball' },
    { type: 'admin', name: 'Agent Smith', age: 23, role: 'Anti-virus engineer' }
];

export function logPerson(person: Person) {
    console.log(
        ` - ${person.name}, ${person.age}, ${person.type === 'admin' ? person.role : person.occupation}`
    );
}

const getObjectKeys = <T>(obj: T) => Object.keys(obj) as (keyof T)[];

export function filterPersons(persons: Person[], personType: 'user', criteria: Partial<Omit<User, 'type'>>): User[];
export function filterPersons(persons: Person[], personType: 'admin', criteria: Partial<Omit<Admin, 'type'>>): Admin[];
export function filterPersons(persons: Person[], personType: string, criteria: Partial<Person>): Person[] {
    return persons
        .filter((person) => person.type === personType)
        .filter((person) => {
            let criteriaKeys = getObjectKeys(criteria);
            return criteriaKeys.every((fieldName) => {
                return person[fieldName] === criteria[fieldName];
            });
        });
}

export const usersOfAge23 = filterPersons(persons, 'user', { age: 23 });
export const adminsOfAge23 = filterPersons(persons, 'admin', { age: 23 });

console.log('Users of age 23:');
usersOfAge23.forEach(logPerson);

console.log();

console.log('Admins of age 23:');
adminsOfAge23.forEach(logPerson);
````

###### challenge => [exercise 7](https://typescript-exercises.github.io/#exercise=7 "Exercise 7")
###### 7 Solution
````
interface User {
    type: 'user';
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    type: 'admin';
    name: string;
    age: number;
    role: string;
}

function logUser(user: User) {
    const pos = users.indexOf(user) + 1;
    console.log(` - #${pos} User: ${user.name}, ${user.age}, ${user.occupation}`);
}

function logAdmin(admin: Admin) {
    const pos = admins.indexOf(admin) + 1;
    console.log(` - #${pos} Admin: ${admin.name}, ${admin.age}, ${admin.role}`);
}

const admins: Admin[] = [
    {
        type: 'admin',
        name: 'Will Bruces',
        age: 30,
        role: 'Overseer'
    },
    {
        type: 'admin',
        name: 'Steve',
        age: 40,
        role: 'Steve'
    }
];

const users: User[] = [
    {
        type: 'user',
        name: 'Moses',
        age: 70,
        occupation: 'Desert guide'
    },
    {
        type: 'user',
        name: 'Superman',
        age: 28,
        occupation: 'Ordinary person'
    }
];

export function swap<T1, T2>(v1: T1, v2: T2): [T2, T1] {
    return [v2, v1];
}

function test1() {
    console.log('test1:');
    const [secondUser, firstAdmin] = swap(admins[0], users[1]);
    logUser(secondUser);
    logAdmin(firstAdmin);
}

function test2() {
    console.log('test2:');
    const [secondAdmin, firstUser] = swap(users[0], admins[1]);
    logAdmin(secondAdmin);
    logUser(firstUser);
}

function test3() {
    console.log('test3:');
    const [secondUser, firstUser] = swap(users[0], users[1]);
    logUser(secondUser);
    logUser(firstUser);
}

function test4() {
    console.log('test4:');
    const [firstAdmin, secondAdmin] = swap(admins[1], admins[0]);
    logAdmin(firstAdmin);
    logAdmin(secondAdmin);
}

function test5() {
    console.log('test5:');
    const [stringValue, numericValue] = swap(123, 'Hello World');
    console.log(` - String: ${stringValue}`);
    console.log(` - Numeric: ${numericValue}`);
}

[test1, test2, test3, test4, test5].forEach((test) => test());
````

###### challenge => [kata](https://www.codewars.com/kata/54da5a58ea159efa38000836 "Kata")
###### Solution
````
function findOdd(A) {
  let count = 0;
   let last;  
   A.sort();  
   for (let i = 0; i < A.length; i++){
      if (A[i] === last) {
         count++;
         continue;
      };
    
      if(count % 2){
         return last;
      };
      last = A[i];
      count = 1;
   };
   return last;
}
````

###### challenge => [kata](https://www.codewars.com/kata/5264d2b162488dc400000001 "kata")
###### Solution
````
function spinWords(string){
  const sentenceArray = string.split(' ');
  let result = '';
  sentenceArray.map((str, i) => {
    if (str.length >= 5){
      sentenceArray[i] = str.split('').reverse().join('');
    } else {
      sentenceArray[i] = str;
    }
  result = sentenceArray.join(' ');
  });
return result;
}
````

## Week 4 challenges (Wednesday)
###### challenge 1 => [kata](https://www.codewars.com/kata/523f5d21c841566fde000009 "kata")
###### Solution
````
function arrayDiff(a, b) {
  return a.filter(e=> !b.includes(e));
}
````

###### challenge 2 => [kata](https://www.codewars.com/kata/525f50e3b73515a6db000b83 "Kata")
###### Solution
````
function createPhoneNumber(numbers){
  var format = "(xxx) xxx-xxxx";
  
  for(var i = 0; i < numbers.length; i++)
  {
    format = format.replace('x', numbers[i]);
  }
  
  return format;
}
````

## Week 4 challenges (Thursday)
###### challenge 1 => [kata](https://www.codewars.com/kata/545cedaa9943f7fe7b000048 "kata")
###### Solution
````
function isPangram(string){
  const alphabet = 'abcdefghijklmnopqrstuvwxyz';
  const str = string.toLowerCase();
  
  for (let i = 0, length=alphabet.length; i < length; i += 1) {
    if (str.indexOf(alphabet[i]) === -1) {
      return false;
    }
  }  
  return true;
}
````

###### challenge 2 => [kata](https://www.codewars.com/kata/5839edaa6754d6fec10000a2 "kata")
###### Solution
````
function findMissingLetter(array){  
  let first = array[0].charCodeAt(0);  
  for(let i=0, length=array.length; i<length; i++){
    if(first+i != array[i].charCodeAt(0)){
      return String.fromCharCode(first+i);
    }
  }  
}
````

###### challengue 3 =>  [kata](https://www.codewars.com/kata/585d7d5adb20cf33cb000235 "kata")
###### Solution
````
function findUniq(arr) {
  return +arr.filter( (value) => { return arr.indexOf(value) == arr.lastIndexOf(value) } );
}
````

## Week 5 challenges (Monday)
###### challenge 1 => [kata](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript "kata")
###### Solution
````
export function squareSum(numbers: number[]): number {
    let total = 0;
    let square = numbers.map(item => item * item);
  
    for(let i=0, length=square.length; i<length; i++) {
     total += square[i]; 
  }
  return total;
}
````

###### challenge 2 => [kata](https://www.codewars.com/kata/563b662a59afc2b5120000c6/ "kata")
###### Solution
````
export class G964 {
    public static nbYear = (p0, percent, aug, p) => {
    let population = p0;
    let years = 0;
    while(population < p)
    {
      population = population + (population * (percent/100)) + aug; 
      years++;
    }
    return years;
    }
}
````
