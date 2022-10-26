# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers. Although on line 4 x is given a value of two we are not calling the function. Therefore when called x will have a value of 1 because it is defined at the top globally. If we called f1 it would be 2

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less. the first console log will be 10 as we are calling for x to be console logged in the function. The second console log will say undefined because y is locally scoped.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}


f1(x);
console.log(x);
// x will stay 9 because it is a const
const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);

```

What will be the output of this code. Explain your answer in 50 words or less.
