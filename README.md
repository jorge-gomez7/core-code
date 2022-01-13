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
      		


