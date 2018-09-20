# shellcode-example
shellcode
```
	call shellcode(shellcode的地址替换本身要替换的函数地址)
	pushad
	//...shellcode代码，很多的shellcode会存在push使得esp值改变...
	add esp,xx(修复shellcode改变的ESP的值，xx为16进制的数字)
	popad
	add esp,4(修复call引起的esp的变化)
	call (原来的函数)
	jmp 回去
```
