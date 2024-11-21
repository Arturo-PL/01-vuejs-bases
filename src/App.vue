
<template>
  <Navbar></Navbar>
  <div class="container">
    <div class="row mt-2">
      <div class="col-3">
        <h4 :class="getStyle" > Contador: {{ counter }}</h4>
        <button class="btn btn-success" @click="handledIncrement">+1</button>
        <button class="btn btn-primary m-2" @click="handledReset">Reset</button>
        <button class="btn btn-danger" @click="handledDecrement">-1</button>
    </div>
    <div class="col"></div>
    </div>
  </div>
  <div class="container">
    <div class="row mt-2">
      <div class="col-3">
        <button :class="getDisabled" @click="handledAddValues">Agregar</button>
    </div>
    <div class="col"></div>
    </div>    
  </div>
  <div class="container">
    <div class="row mt-2">
      <div class="col-3">
        <h4>Números agregados a la lista: </h4>
        <div v-for="(value, index) in valoresLista" :key="index">
          <p>{{ value }}</p>
        </div>
    </div>
    <div class="col"></div>
    </div>    
  </div>
</template>

<script setup>

import { ref, computed } from 'vue'

import Navbar from './components/Navbar.vue';

const counter = ref( 0 ); // counter es una variable reactiva, y es de tipo number

const handledIncrement = ()=>{
  counter.value = counter.value + 1;

}

const handledDecrement = ()=>{
  counter.value = counter.value - 1;

}

const handledReset = ()=>{
  counter.value = 0;

}

const getStyle = computed( ()=> {
  if(counter.value === 0) return 'text-primary';
  if(counter.value > 0) return 'text-success';
  if(counter.value < 0) return 'text-danger';
})


const valoresLista = ref( [] );

const handledAddValues = () =>{
  if(!valoresLista.value.includes(counter.value)){
    valoresLista.value.push(counter.value);
  }
}

const getDisabled = computed(() => {
  if(valoresLista.value.includes(counter.value)) return 'btn btn-secondary btn-lg disabled';
  return 'btn btn-primary btn-lg';
})

</script>