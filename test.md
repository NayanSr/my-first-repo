### Q1.  What is Typescript, and how is it different from JavaScript?
**Answer:**  *Typescript is a superset of JavaScript. Typescript use JavaScript, difference is in typescript we need to declare type explicitly where JS type is implicit.*

### Q2.  Can you explain the difference between "interface" and "type" in Typescript? 
**Answer:**  *Botha is use for declaring type. Type  alias is more suitable for primitive data type where interface is suitable for non-primitive data type. An old interface can be extend to create a new interface, but in type alias extend do not works.*

### Q3.  Can you give an example of how to use generics in Typescript?
**Answer:**  
interface ICountry<T, F> {     
    capital: T,
    districts: F
} <br>
const bangladesh: ICountry<string, number> = {
        capital: 'Dhaka',
        districts: F
    }

### Q4.  What is the difference between an 'unknown' and 'any' type in Typescript?
**Answer:**  *'unknown'  type use when we will know the type on runtime. 'any' type is use when we don’t know the type just when declaring. 'any' is not recommended.*

### Q5.  Can you give an example of how to use enums in Typescript?
**Answer:**  **

### Q6.  What is the "as" keyword used for in Typescript?
**Answer:**  *‘as’ use for type assertion. It use for overwrite type of a data by a coder from typescript intelligence *

### Q7.  Can you explain how to use "type guards" with "in" and "typeof" operators in                        
,      Typescript?

**Answer:**  
*typeof guard:  Use for checking type* <br>
function checkTypeof(param1:string |number,param2:string |number){<br>
    if(typeof param1==='string' && typeof param2==='string'){<br>
        console.log('Both are string');<br>
    }<br>
    else if(typeof param1==='number' && typeof param2==='number'){<br>
        console.log('Both are number');<br>
    }<br>
}<br>

*in guard: Use to checking key from typr/interface*<br>

type NormalUser = { name: string };<br>
type AdminUser = { name: string, roll: 'admin' };<br>
function getUser(user: AdminUser | NormalUser): string {<br>
    if ('roll' in user) {<br>
        return `I am ${user.name} & my roll is ${user.roll}`<br>
    }<br>
    else { return `I am ${user.name}, a normal user` }<br>
};


