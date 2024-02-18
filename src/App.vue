<template>
  <div id="app">
    <CalculadoraAritmetica />
  </div>
</template>

<script>

import CalculadoraAritmetica from './components/CalculadoraAritmetica.vue';

export default {
  components: {
    CalculadoraAritmetica
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', 'Helvetica', 'Arial', sans-serif;
  text-align: center;
  color: #f1a7cb;
  margin-top: 60px;
  background: linear-gradient(135deg, #0f1010, #701332); 
  min-height: 100vh; 
}

input, select {
  font-size: 22px; 
  margin: 15px; 
  padding: 15px; 
  border-radius: 5px; 
  border: 1px solid #101010; 
  box-shadow: 0px 4px 4px rgba(91, 7, 7, 0.1); 
  background-color: rgba(241, 241, 242, 0.9); 
}

select {
  font-size: 30px; 
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #101010;
  cursor: pointer;
}

p {
  font-size: 30px; 
  color: #121212; 
  margin-top: 20px;
  padding: 10px;
  border-radius: 5px;
  background-color: rgba(0, 0, 0, 0.5); 
}

p:hover {
  transform: scale(1.3);
  transition: transform 0.3s ease-in-out;
  background-color: rgba(232, 159, 236, 0.7); 
}

button {
  font-size: 20px;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  background-color: #4cd137;
  color: white;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
  transition: background-color 0.3s, box-shadow 0.3s;
}


h1 {
  color: #34495e;
  font-size: 36px;
  margin-bottom: 10px;
}


</style>