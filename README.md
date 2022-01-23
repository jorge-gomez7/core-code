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

###### 3 Solution
function getChar(c){
  return String.fromCharCode(c);
}

###### 4 Solution
function addBinary(a,b) {
 let c = a+b;
  let cBinary = c.toString(2);
  return cBinary;
}

##### 5 Solution
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

## Week2 challenges (Wednesday)
###### 1 Solution
function dutyFree(normPrice, discount, hol){
  let realDiscount = (normPrice/100)*discount;
return Math.floor(hol/realDiscount);
}

###### 2 Solution
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs((sonYearsOld*2)-dadYearsOld);
}

###### 3 Solution
function validSpacing(s) {
  if(s.length == 0) return true;
  if(s[0]== ' ' || s[s.length-1]== ' ') return false;
  
  let aSpaces0 = s.split(' ');
  
  for(let i =0, length = aSpaces0.length; i<length; i++){
      if(aSpaces0[i] == '') return false;
  }
  return true;
}

###### 4 Solution
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
