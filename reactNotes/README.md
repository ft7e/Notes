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

## conditional rendering

- if part of the code only will change we do this :

**put the edge case in a variable and then if statement to change it if the condition applies and render the variable itself**

`let expensesContent = <p>No items were found</p>;`
`if (filteredExpenses.length > 0) { expensesContent = filteredExpenses.map((expense) => ( <ExpenseItem key={expense.id} title={expense.title} amount={expense.amount} date={expense.date} />`

- if the whole component will change, we can use if statement and return the whole new thing we wanna render :

`if(filteredExpenses.length === 0){ return <h2>No items were found</h2> }`

- if we can only 2 components or a small number we can do this :
  ` js {hideForm && ( <button type='button' onClick={hideFormHandler}> Add New Expense </button> )}`
  `{!hideForm && <ExpenseForm onSaveExpenseData={saveExpenseDataHandler} />}`

  **the '&' will only continue if it's true so we coop it with the state**
