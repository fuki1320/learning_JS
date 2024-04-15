LOOP IN JAVASCRIPT






Differences between For, While and Do-While loops in example code:
_(Built upon code from Codecademy)_

// F O R  L O O P

let cupsOfSugar = 5

for (let cupsAdded = 1; cupsAdded < cupsOfSugar; cupsAdded++){
    console.log (cupsAdded + ' cup was added [for loop]');
};




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
