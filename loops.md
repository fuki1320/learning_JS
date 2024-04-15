# LOOPS AND ITERATIONS IN JAVASCRIPT


Differences between For, While and Do-While loops in example code:
_(Built upon code from Codecademy)_

## _FOR_ loop
**A for loop repeats until a specified condition evaluates to false.**

- A for statement looks as follows:

      for (initialization; condition; afterthought) {
  
      statement
  
       };
  
1. **Initialization:** This is where you initialize your loop control variable(s). It typically sets the initial value of a counter variable. For example, int i = 0; initializes a variable named i with the value of 0.
2. **Condition:** This is the condition that is evaluated before each iteration of the loop. If the condition evaluates to true, the loop continues; if it evaluates to false, the loop terminates. For example, i < 10; checks if the variable i is less than 10.
3. **Afterthought:** This is an expression that is executed at the end of each iteration of the loop. It's commonly used to update the loop control variable(s). For example, i++ increments the value of i by 1 after each iteration.
4. **Statement(s):** This is the block of code that you want to execute repeatedly as long as the condition remains true. It can be a single statement or a block of statements enclosed in curly braces {}.

      
         for (int i = 0; i < 10; i++) {
   
         // Statement(s) to be executed repeatedly
   
         console.log("the value of i is ", i);
   
          };

A for loop is often used when you know **how many times you want to iterate**.

In most cases if the increment afterthought isn't specified, it will result in infinite loop. _This is because without an increment or decrement, the loop control variable will never change its value, potentially preventing the loop condition from ever becoming false._


### Specific example of For loop 
- In the code below, a for loop is used with an initialization (let cupsAdded = 1), condition (cupsAdded < cupsOfSugar), and increment (cupsAdded++).
- This loop will execute as long as **cupsAdded is less than cupsOfSugar**.
- This loop will execute a **specific number of times**, iterating **from 1 up to cupsOfSugar (its numeric value) - 1**

      let cupsOfSugar = 5
  
      for (let cupsAdded = 1; cupsAdded < cupsOfSugar; cupsAdded++){
  
      console.log (cupsAdded + ' cup was added [for loop]');
  
      };

- The for loop has a clear initialization, condition, and increment (in this case meaning afterthought) section. **It iterates from 1 to cupsOfSugar - 1 (i.e., 4 iterations when cupsOfSugar is 5)**.
- The loop executes exactly as many times as specified in the condition and doesn't go beyond that limit (doesn't go beyond the value of 5.)
- **The condition is tested first, if it's evaluated as a truthy statement, the loop's body is executed and only then the value of the variable is incremented.**
- For example, if the value of variable _cupsOfSugar_ is 5, the loop **iterates 4 times**, adding 1 cup of sugar each time, resulting in a total of 4 cups added, because the **value of cupsAdded must be less than the value of cupsOfSugar** as it is stated in condition of the loop!
  
| Iterations  | cupsAdded initial value | Iteration condition | Boolean value | Statement    | Incremented value of cupsAdded  (for the upcoming iteration) |
|-------------|-------------------------|---------------------|---------------|--------------|--------------------------------------------------------------|
| Iteration 1 | 1                       | 1<5                 | true          | executed     | 2                                                            |
| Iteration 2 | 2                       | 2<5                 | true          | executed     | 3                                                            |
| Iteration 3 | 3                       | 3<5                 | true          | executed     | 4                                                            |
| Iteration 4 | 4                       | 4<5                 | true          | executed     | 5                                                            |
| Iteration 5 | 5                       | 5<5                 | false         | not executed |                                                              |


## _WHILE_ loop
**A while statement executes its statements as long as a specified condition evaluates to true.**
- If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop (inside the loop).
- **The condition test occurs before statement in the loop is executed.** If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

- A while statement looks as follows:

      while (condition) {
  
      statement
  
      };
        
1. **Condition:** Inside the parentheses, you specify the condition that needs to be evaluated. As long as this condition evaluates to true, the loop will continue to execute. If the condition evaluates to false initially, the statement inside the loop will not be executed at all.
2. **Statement(s):** This is the statement that you want to execute repeatedly as long as the condition remains true. It can be a single statement or a block of statements enclosed in curly braces {}.

         let count = 0;
      
         while (count < 5)
            
         console.log(count++);
      
While loops are often used when **the number of iterations is not known** beforehand and depends on a specific condition.

Condition is evaluated before executing the loop. If the condition is true, the code inside the loop is executed. If the condition is false, the code block is skipped, and the program continues to execute the code after the loop. After executing the code block, the condition is evaluated again. If it's still true, the code block is executed again. This process repeats until the condition becomes false.

A while loop becomes infinite if the condition specified in the loop header never becomes false. It happens if the increments are not specified, unintended logic is implemented (i.e., using floating-point arithmetic) or inadequate exit condition is used (this will lead to the loop never meeting the specified conditions if they're not implemented enough.)

### Specific example of While loop 
- Two variables are initialized (cupsOfSugar and cupsAdded.)
- The while loop starts with the condition ++cupsAdded < cupsOfSugar (aka incremented value of cupsAdded can't be greater than cupsOfSugar.)

      let cupsOfSugar = 5

      let cupsAdded = 0
      
      while (++cupsAdded < cupsOfSugar)
      
      {console.log(cupsAdded + ' cup was added[while loop]');}

- ++cupsAdded is a **pre-increment** operation, which means **cupsAdded is incremented by 1 before being compared** to cupsOfSugar.
- The loop continues executing as long as the incremented value of added is less than cupsOfSugar.
- In this case, **the loop iterates exactly 4 times, until the condition becomes falsy**. Meaning cupsAdded is pre-incremented 4 times in total (by 1 in each iteration) to be still less than the value of the variable cupsOfSugar.
  
| Iterations  | cupsAdded initial value | Incremented value of cupsAdded | Iteration condition | Boolean value           | Statement    |
|-------------|-------------------------|--------------------------------|---------------------|-------------------------|--------------|
| Iteration 1 | 0                       | 1                              | 1<5                 | true                    | executed     |
| Iteration 2 | 1                       | 2                              | 2<5                 | true                    | executed     |
| Iteration 3 | 2                       | 3                              | 3<5                 | true                    | executed     |
| Iteration 4 | 3                       | 4                              | 4<5                 | true                    | executed     |
| Iteration 5 | 4                       | 5                              | 5<5                 | false (end of the loop) | not executed |


## _Do-While_ loop
**The do-while statement repeats until a specified condition evaluates to false. **
- A do-while statement looks as follows:

      do {
  
        statement
  
      } while (condition);
  
1. **Initialization:** First, any variables needed in the loop are initialized (this usually happens outside the loop.)
2. **Statement(s):** Code of block that is always executed before the condition of the loop is checked.
3. **Condition:** If the condition evaluates to true, the loop continues, and the code block is executed again. If the condition evaluates to false, the loop terminates, and the program continues with the next statement after the loop.
4. **Increment or Update Variables:** If the loop involves any variables that are updated inside the code block, those updates are typically done before the condition is evaluated again.

            var i = 1;
   
            do {
   
            console.log(i);
   
            i++;
   
            } while (i <= 5);

Do-while loops are particularly used when you want to ensure that a **block of code (aka loop statement) runs at least once, regardless of whether the condition is initially true or false.** This can be useful in situations where you need to perform some action and then check a condition afterward to determine if the action should be repeated.

A do-while loop becomes infinite if the condition never becomes false. This can happen when dealing with user input or never changing conditions of specified statements. 

### Specific example of Do-while loop 
 - Two variables are initialized and their values specified outside the loop.
 - Two statements are created inside the do cycle. The variable cupsAdded is incremented by 1 each iteration, while console logs the current number (value) of cupsAdded.

            let cupsOfSugar = 5;
   
            let cupsAdded = 0;

            do {
  
              cupsAdded++
 
              console.log(cupsAdded + ' cup was added [do-while loop]');

            } while (cupsAdded < cupsOfSugar);

- The while keyword is followed by a condition that states cupsAdded < cupsOfSugar. This condition checks if the number of cupsAdded is less than the total of cupsOfSugar. If the condition is truthy, the loop continues. Otherwise, it terminates.
- The loop will execute at least once because it's a do-while loop. Meaning, even if cupsAdded is initially greater than or equal to cupsOfSugar, **the loop will still execute once, because it executes statements before checking the condition.**
- This loop will iterate 5 times, though the last iteration is executed its condition is falsy, which leads to the loop termination.
  
| Iterations  | cupsAdded initial value | Incremented value of cupsAdded  (for the upcoming iteration) | Iteration condition | Statement | Boolean value           |
|-------------|-------------------------|--------------------------------------------------------------|---------------------|-----------|-------------------------|
| Iteration 1 | 0                       | 1                                                            | 1<5                 | executed  | true                    |
| Iteration 2 | 1                       | 2                                                            | 2<5                 | executed  | true                    |
| Iteration 3 | 2                       | 3                                                            | 3<5                 | executed  | true                    |
| Iteration 4 | 3                       | 4                                                            | 4<5                 | executed  | true                    |
| Iteration 5 | 4                       | 5                                                            | 5<5                 | executed  | false (loop terminates) |





// increment inside the loop
let sugar2 = 5
let added2 = 0

while(added2 < sugar2) {
  added2++;
  console.log (added2 + ' cup was added [while loop with increment inside the loop]');
  //This way, added2 will be incremented only after the loop condition is checked!!!
}



