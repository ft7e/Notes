# Almost everything I learned so far

## useState

it has 2 uses :

1- to change the element value

`const [enteredTitle, setEnteredTitle] = useState('Hello');`
`<p>{enteredTitle}</p>`

_You give the element the default value and then change it using the function_

- if the element depends on it's previous state the function must be changed :

`const setEnteredTitle = (prev)=>{ return enteredTitle + '!' }`

2- to store element value, usually used in forms :

` <form onSubmit={submitHandler}>`
`<input type='text' onChange={titleChangeHandler} />`
`const titleChangeHandler = (event) => { setEnteredTitle(event.target.value);}`

_We can also add value attribute to the input tag and give it the state variable so we can reset it after submiting_

## Pass from child to parent

_<Form> => <NewExpense> => <App>_

- You should make a function in the parent, pass it to the child, child use it and send data back to parent

NewExpense function (parent) =>

'const getFormData = (formData) => {
const data = {
...formData,
};
console.log(data)
};'

- pass this function to FORM : `<Form passFormData={getFormData} />`

- use it in FORM : `props.passFormData(formData)`
