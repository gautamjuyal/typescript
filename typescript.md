# INTERFACE 

Interfaces are similar to classes. Used in TS to define a schema(?)/ contract that an object must adhere to.

## Usage : 

1. In a typescript file, an interface is defined like this: 

interface Person {
    firstName : String,
    dob: Date
}

and used like this

let person : Person = {
    firstName : 'Dave',
    dob: new Date('2000-01-01')
}

2. In a tsx file, interface is defined similarly, but used with a different syntax 

interface ButtonProps{
    text: String,
    color: String
}

const Button :  React.FC<ButtonProps> = (props)=>{
    <button></button>
}

or

const Button :  React.FC = (props: { text: String})=>{
    <button></button>
}

3. Making a prop optional in an interface : Just add a question mark in front of optional prop

interface ButtonProps{
    text: String,
    color?: String
}