# Ex4 Evaluation of prefix expression
## DATE:
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm:
```
1.  Start 
2. Initialize an empty stack s with a variable top for tracking the stack index. 
3. Define a push() function to add an element to the stack. 
4. Define a pop() function to remove and return the top element from the stack. 
5. In evalprefix(), loop through the given prefix expression from right to left. 
6. For each character, if it’s an operator (+, *), pop two operands from the stack, perform the 
operation, and push the result. 
7. If it's a digit, convert it to an integer and push it onto the stack; finally, print the result after 
the loop ends. 
8. End the program.
```

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: SARANYA S
RegisterNumber:  212223110044
*/
```
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>

int stack[50];
int top=0;

void push(int ch)
{
    top=top+1;
    stack[top]=ch;
	
}

int pop()
{
	int ch;
	ch=stack[top];
	top=top-1;
	return(ch);
}

//void evalprefix(char p[50])
//{
    int a,b,c;
    int i=strlen(p)-1;
    while(i>=0)
    {
        
    if(isdigit(p[i]))
    {
        
    push(p[i]-48);
    }
    else
    {
        a=pop();
        b=pop();
        switch (p[i])
        {
            case '+':
            c=a+b;
            break;
            case '*':
            c=a*b;
            break;
        }
        push(c);
    }
    i--;
    }
    printf("%d",pop());
```
## Output:
![image](https://github.com/user-attachments/assets/1b19fb45-0e07-43cc-a221-b21b43db11aa)

## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
