# LOOPS AND ITERATIONS IN JAVASCRIPT


Differences between For, While and Do-While loops in example code:
_(Built upon code from Codecademy)_

## _FOR_ loop
A for loop repeats until a specified condition evaluates to false. 

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


- In the code below, a for loop is used with an initialization (let cupsAdded = 1), condition (cupsAdded < cupsOfSugar), and increment (cupsAdded++).

- This loop will execute as long as **cupsAdded is less than cupsOfSugar**.
 
- This loop will execute a **specific number of times**, iterating **from 1 up to cupsOfSugar (its numeric value) - 1**


        let cupsOfSugar = 5

        for (let cupsAdded = 1; cupsAdded < cupsOfSugar; cupsAdded++){

         console.log (cupsAdded + ' cup was added [for loop]');

        };

- The for loop has a clear initialization, condition, and increment (aka afterthought) section. **It iterates from 1 to cupsOfSugar - 1 (i.e., 4 iterations when cupsOfSugar is 5)**.
- The loop executes exactly as many times as specified in the condition and doesn't go beyond that limit (aka doesn't go beyond the value of 5.)
- For example, if the value of variable _cupsOfSugar_ is 5, the loop **iterates 4 times**, adding 1 cup of sugar each time, resulting in a total of 4 cups added, because the **value of cupsAdded must be less than the value of cupsOfSugar** as it is stated in condition of the loop!


## _WHILE_ loop
- A while statement executes its statements as long as a specified condition evaluates to true.
- If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop (inside the loop).
- **The condition test occurs before statement in the loop is executed.** If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

- A while statement looks as follows:

            while (condition) {

            statement

            };
  
1. **Condition:** Inside the parentheses, you specify the condition that needs to be evaluated. As long as this condition evaluates to true, the loop will continue to execute. If the condition evaluates to false initially, the statement inside the loop will not be executed at all.
2. **Statement:** This is the statement that you want to execute repeatedly as long as the condition remains true. It can be a single statement or a block of statements enclosed in curly braces {}.


            let count = 0;

            while (count < 5)

            console.log(count++);

   

While loop are often used when **the number of iterations is not known** beforehand and depends on a specific condition.

Condition is evaluated before executing the loop. If the condition is true, the code inside the loop is executed. If the condition is false, the code block is skipped, and the program continues to execute the code after the loop. After executing the code block, the condition is evaluated again. If it's still true, the code block is executed again. This process repeats until the condition becomes false.
A while loop becomes infinite if the condition specified in the loop header never becomes false. It happens if the increments are not specified, unintended logic is implemented (i.e. using floating-point arithmetic) or inadequate exit condition is used (this will lead to the loop never meeting the specified conditions if they're not implemented enough)




let sugar = 5
let added = 0
while (++added < sugar)
{console.log(added + ' cup was added[while loop]');}



// D O   W H I L E   L O O P 

// defining both variables 
let cupsOfSugaR2 = 5;
let cupsAdded2 = 0;

do {
  cupsAdded4++
  console.log(cupsAdded4 + ' cup was added [do-while loop]');
} while (cupsAdded4 < cupsOfSugarNeeded4);



// increment inside the loop
let sugar2 = 5
let added2 = 0

while(added2 < sugar2) {
  added2++;
  console.log (added2 + ' cup was added [while loop with increment inside the loop]');
  //This way, added2 will be incremented only after the loop condition is checked!!!
}


//for loop
let sugar3 = 5

for (let added3 = 1; added3 < sugar3; added3++){
    console.log (added3 + ' cup was added [for loop]');
}
