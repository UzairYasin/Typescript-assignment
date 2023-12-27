Calculator Assignment

import inquirer from "inquirer";

let guess = await inquirer.prompt([
    {
        type: 'number',
        name: 'num1',
        message: 'num-1 :'
    },
    {
        type: 'number',
        name: 'num2',
        message: 'num-2 :'
    },
    {
        type: 'list',
        name: 'operator',
        message: 'what to do :',
        choices: ['Add','Sub','Mul','Div']
    }
]);

if (guess.num1 === 'String') {
    console.log('Enter Valid Number!');
}

if (guess.operator === 'Add') {
    console.log(`${guess.num1} + ${guess.num2} = ${guess.num1 + guess.num2}`);
}

else if(guess.operator === 'Sub'){
    console.log(`${guess.num1} - ${guess.num2} = ${guess.num1 - guess.num2}`);
}

else if(guess.operator === 'Mul'){
    console.log(`${guess.num1} * ${guess.num2} = ${guess.num1 * guess.num2}`);
}

else if(guess.operator === 'Div'){
    console.log(`${guess.num1} / ${guess.num2} = ${guess.num1 / guess.num2}`);
}

else{
    console.log('Enter Valid Number');
}
