<template>
  <header>
    <h1>To-Do</h1>
  </header>
  
  {{novaTarefa}}
    <div class="container">
      
    <form>
      <input type="text" placeholder="Nova tarefa" v-model="novaTarefa" />
    </form>
    <ul>
      <li>
        <label>
          <input type="checkbox" >
        </label>
        <div class="text">
          <button>Super nova tarefa</button>       
        </div>
        <button class="remover">Remover</button>
      </li>
    </ul>
    </div>
    <footer>
      <p>
        Por Bruna © 2022
      </p>
    </footer>
 

  <main>
    <TheWelcome />
  </main>
</template>

<script>
  export default {
  setup(){
    const novaTarefa = 'Outra nova tarefa';
    return {novaTarefa};
  }
};
</script>


<style>
  header{
    padding: 3rem 0 1.5rem;
  }

  h1 {
    text-align: center;
    font-size: 4rem;
    color: #aaa;
    letter-spacing: 7px;
    font-weight: 100;
    margin: 0;
    line-height: 1;

  }
  .container{
    max-width: 30rem;
    background-color: white;
    margin: 0 auto;
    box-shadow: 0 5px 10px -7px rgba(0 0 0 /30%);
    border-radius: 5px;
  }

  form {
    border-bottom: 1px solid #ddd;
  }
  form input {
    border: none;
    padding: 1rem 1.5rem;
    width: 100%;
    font-size: 1.5rem;    
  }

  form input::placeholder {
    color: rgb(216, 213, 213);
  }

  ul{
    list-style: none;
    margin: 0;
    padding: 0;
  }

  li {
    border-bottom: 1px solid #eee;
    display: flex;
  }

  li:last-child {
    border: none;
  }
  label {
    padding: 0 1rem;
    line-height: 2.5rem;
  }

  .text{
    flex: 1;
  }

  .text button,
  .text span {
    font: inherit;
    color: inherit;
    padding: 0 1rem;
    width: 100%;
    text-align: left;
    line-height: 2.5rem;
  }

  .remover {
    color: red
  }

  footer{
    font-size: 0.75rem;
    color: #aaa;
    text-align: center;
  }
</style>

