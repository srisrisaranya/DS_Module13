# Ex2 Conversion of the infix expression into postfix expression
## DATE:
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1.  Start the program. 
2. Initialize a stack and set the top index to -1. 
3. Define the push() and pop() functions to add and remove elements from the stack. 
4. Define the priority() function to assign priorities to operators. 
5. Traverse the expression in the IntoPost() function, handling operands, parentheses, and 
operators. 
6. After processing the expression, pop and print any remaining operators from the stack. 
7. End the program.

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: SARANYA S
RegisterNumber:  212223110044
*/
```
```
char IntoPost(char *exp)
{
   char *e,x;
   e=exp;
   while(*e!='\0')
   {
       if(isalnum(*e))
       printf("%c",*e);
       else if(*e=='(')
       push(*e);
       else if(*e==')')
       {
           while((x=pop())!='(')
           printf("%c",x);
       }
       else
       {
           while(priority(stack[top])>=priority(*e))
           printf("%c",pop());
           push(*e);
       }
       e++;
   }
   while(top!=-1)
   printf("%c",pop());
   
    
    
 return 1;   
}
```

## Output:
![image](https://github.com/user-attachments/assets/7e376e72-d609-4c39-942c-94f998ab4816)

## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
