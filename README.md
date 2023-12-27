Calculator Assignment

import inquirer from "inquirer";

let calculate = await inquirer.prompt
([

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


if (calculate.num1 === 'String') {
    console.log('Enter Valid Number!');
}


if (calculate.operator === 'Add') {
    console.log(`${calculate.num1} + ${calculate.num2} = ${calculate.num1 + calculate.num2}`);
}


else if(calculate.operator === 'Sub'){
    console.log(`${calculate.num1} - ${calculate.num2} = ${calculate.num1 - calculate.num2}`);
}

else if(calculate.operator === 'Mul'){
    console.log(`${calculate.num1} * ${calculate.num2} = ${calculate.num1 * calculate.num2}`);
}

else if(calculate.operator === 'Div'){
    console.log(`${calculate.num1} / ${calculate.num2} = ${calculate.num1 / calculate.num2}`);
}

else{
    console.log('Enter Valid Number');
}
