# LOOPS AND ITERATIONS IN JAVASCRIPT


Differences between For, While and Do-While loops in example code:
_(Built upon code from Codecademy)_

## _FOR_ loop
- A for loop repeats until a specified condition evaluates to false. (The JavaScript for loop is similar to the Java and C for loop.)

- A for statement looks as follows:

      for (initialization; condition; afterthought) {

      statement };

- A for loop is often used when you know **how many times you want to iterate**.

- In the code below, a for loop is used with an initialization (let cupsAdded = 1), condition (cupsAdded < cupsOfSugar), and increment (cupsAdded++).

> This loop will execute as long as **cupsAdded is less than cupsOfSuga**r.

> This loop will execute a **specific number of times**, iterating **from 1 up to cupsOfSugar (its numeric value) - 1**

        _// FOR loop example_

        let cupsOfSugar = 5

        for (let cupsAdded = 1; cupsAdded < cupsOfSugar; cupsAdded++){

         console.log (cupsAdded + ' cup was added [for loop]');

        };

- The for loop has a clear initialization, condition, and increment section. It iterates **from 1 to cupsOfSugar - 1 ****_(i.e., 4 iterations when cupsOfSugar is 5)**_.
- The loop executes exactly as many times as specified in the condition and doesn't go beyond that limit.
- For example, if the value of variable _cupsOfSugar_ is 5, the loop **iterates 4 times**, adding 1 cup of sugar each time, resulting in a total of 4 cups added, because** the value of cupsAdded must be less than the value of cupsOfSugar** as it is stated in condition of the loop!



// W H I L E   L O O P

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
