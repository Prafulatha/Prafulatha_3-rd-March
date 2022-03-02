# Prafulatha_3-rd-March

React-js

App.js:----

import React from 'react';

import TodoForm from './components/ TodoForm'; import TodoList from './components/ TodoList';

function App() { return (
}; }

export default App;

TodoForm.js:-

import React,{useState, useEffect, useRef} from 'react'

function TodoForm(props){ const [input, setInput] = useState('props.edit ? props.edit.value:''); const inputRef = useRef(null);

useEffect{() => { inputRef.current.focus() });

const handlechange = e =>{ setInput(e.target.value); );

const handleSubmit = e =>{ e.preventDefault();

props.onSubmit({ id:Math.floor(math.random() * 10000), text: input }); setInput(''); };

return(
{props.edit ? ( <> Update); ); ( <> ); }

export default TodoForm;

TodoList.js:--

import React, {useState} from 'react' import TodoForm from './TodoForm' import Todo from './Todo';

function TodoList() { const [todos, setTodos] = useState([]);

const addTodo = todo => { if(!todo.text ||/^\s*$/.test(todo.text)){ return; } const newTodos = [todo,.....todos];

setTodos(newTodos); // console.log(....todos); };

const updateTodos = (todoId, newvalue) => { if(!newValue.text ||/^\s*$/.test(newValue.text)){ return; }

setTodos(prev => prev.map(item => (item.id ===todoId ? newValue : item)) ); };

const removeTodo = id => { const removeArr = [.....todos],filter[todo => todo.id !==id)

setTodos(removeArr); };

const completeTodo = id =>{ let updatedTodos = todos.map(todo =>{ if(todo.id ===id) { todo.isComplete = !todo.isComplete

} return todo; }); setTodos(updatedTodos); }; return (
Todo List

<TodoForm onSubmit={addTodo}/>
<Todo todos={todos} completeTodo={completeTodo} removeTodo= {removeTodo} updateTodo= {updateTodo}/>

); } export default TodoList;

Todo.js:--- import React, {useState} from 'react' import Todoform from './TodoForm' import { RiclosecircleLine } from 'react-icons/ri' import { TiEdit } from 'react-icons/ti'

function Todo({ todos, completeTodo, removeTodo , updateTodo}) { const [edit, setEdit] = useState({ id: null, value: '' });

const submitUpdate = value =>{ updateTodo(edit.id, value) setEdit({ id:null, value:'' }) } if(edit.id){ return <TodoForm edit=>{edit} onSubmit={submitUpdate}/>

return todos.map((todo,index)=>(
completeTodo(todo.id)}> {todo.text}
removeTodo(todo.id)} className='delete-icon' /> setEdit({ id: todo.id, value: todo.text })} className='edit-icon' /> 
