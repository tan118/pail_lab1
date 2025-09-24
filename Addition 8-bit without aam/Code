section .text
global _start ;must be declared for linker (ld)

_start:

mov eax,x 
mov ebx,0 
mov ecx, 5 

top: add ebx, [eax]

add eax,1 
loop top 

done:

add ebx, '0'
mov [sum], ebx 

display:

mov edx,1 
mov ecx, sum 
mov ebx, 1 
mov eax, 4 
int 0x80 

mov eax, 4
mov ebx, 1
mov ecx, newline    
mov edx,1
int 0x80

mov eax, 1 ;system call number (sys_exit)
int 0x80 ;call kernel

section .data
global x
x:
db 1
db 2
db 3
db 1
db 2

newline db 10

sum:
db 0 , 0xa
