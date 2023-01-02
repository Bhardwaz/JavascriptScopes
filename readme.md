# Javascript has 3 Kinds of Scopes 
## 1. Global Scope ( i.e. Top Level Code)
## 2. Function Scope
## 3. Block Scope ( i.e. if-else statements and loops etc. )

# Let's Start
## 1. Global Scope :- The code that is outside of any function,statements or loops etc. that is called Global Scope. This is the Scope that remains on the top in hierarchy.

         ` // Global Scope 
            const name = 'sumit'
            const age = 25 ; 
            function fullName(){
             console.log(`My name is
             {name} and my age is ${age} `)
            }
            fullName(); 
            The name and age in this code is belongs to global scope  `

## 2. Function Scope :- Let's take same example for Function scope. Any declaration that happens in function that is called function scope and it is below than global scope in hierarchy and because of this hierarchy only it allows to access declarations from global scope but global scope is not allowed to do look down for declarations. it simply throws error of undefined

         ` // Global Scope 
            const name = 'sumit'
            const age = 25 ; 
            function fullName(){
             const jobRole = 'Developer'
             console.log(`My name is
             {name} and my age is ${age} and my job role is ${jobRole}`)
            }
            fullName(); 
            The name and age in this code is belongs to global scope  `

## 3. Block Scope :- This scope is interesting. This comes in ES6 with let and const ( let and const also comes in ES6 ) before that we used to declare variable with var keyword that is function scoped but with ES6 let and const comes as block scope 

       ` if(statement){
          var age = 25;
       }
       console.log(age) :- this does not throw any error because var is not block scoped       `
## but doing same with let and const also throws error because these are block scoped and does not allowed to access out of the block

     `   if(statements){
         let age = 25;
         const name = 'sumit'
     } 
     console.log(my age is ${age} and my name is ${name}); // This will throw error        `