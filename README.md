# RPN-Equation
Given an Infix equation, convert the equation into a Reverse Polish Notation(RPN) using Stacks and Queues.

## How it works:
  Loop through equation, if it is a variable, put it into the queue, otherwise put it into a stack. If there is a closing parenthesis, pop everything from the stack until the open parenthesis
  After looping, then pop from the top of the stack into the queue. 
  
## For example:  
      Stack = [] (last in, first out)  
      Queue = [] (first in, first out)    
    
      First iteration:  
      Stack = [+ * ( - ]  
      Queue = [a b c d]  
    
      Start popping from top of the stack  
      Result: Queue = [a b c d - * +]  
       
## Second example with numbers:  
        Infix equation: (1 + 2) + 3 / 3
        Stack = []  
        Queue = []  
        
        How stack and queu looks like before the closing parenthesis.
        Stack = [ (  + ] 
        Queue = [1 2 ]
        
        When we hit the ")", we pop everything from the stack and add it to the queue
        Stack = [ ]
        Queue = [1 2 +]
        
        Continue with the rest of the equation
        Stack = [ + / ]
        Queue = [ 1 2 + 3 4]
        
        Pop everything from Stack 
        Stack = [ ] 
        Queue = [ 1 2 + 3 4 / + ]
        
        Queue is now the RPN equation: 1 2 + 3 4 / + 
        
    
