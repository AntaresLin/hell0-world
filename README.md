# hell0-world
just an example

print('hello world!')

#include<stdio.h>
main{
    printf("hello world!\n")
}

data segment
    string db 'hello world!',13,10,'$'
data ends
code segment
    assume ds:data,cs:code
main:
    mov ax,data
    mov ds,ax
    mov dx,offset string
    mov ah,9
    int 21h
    mov ah,4ch
    int 21h
code ends
end main
