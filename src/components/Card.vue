<template>
  <div class ="card-item-container">
    <img :src="props.src" class="card-item-image">

    <h3 class="card-item-title"> {{props.title}}</h3>
    <p class="card-item-text">{{props.bgtext}}</p>
    <button class="card-item-button"> {{props.button}} &rarr; </button>
    <p class="card-item-tag" v-if="props.tag"> {{props.tag}} </p>
  </div>
</template>

<script setup>
// import {ref} from 'vue';
import {defineProps} from 'vue';
  const props = defineProps({
  title: String,
  button: InputEvent,
  bgtext: String,
  src: Object,
  tag: String,
})


  

</script>

<style >
:root {
  --primary-color:  white;
  --secondary-color: #0b132b;
  --tertiary-color:  #598392;
}
  .card-item-container {
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   padding: 1rem;
   border-radius: 10px;
   background-color: var(--primary-color);
   box-shadow: 0 2rem 4rem rgba(0, 0, 0, 0.2);
   transition: all .5s ease-out;
}


.card-item-container:hover {
  transform: translateY(-.5%);
  box-shadow: 0 3rem 6rem rgba(0, 0, 0, 0.4);
}

.card-item-image {
  object-fit: contain;
  width: 100%;
  height: 100%;
  border-top-left-radius: 10px ;
  border-top-right-radius: 10px ;
}
.card-item-text {
  font-size: 1.5rem;
  line-height: 1.2;
  color: var(--secondary-color);
  text-align: center;
}

.card-item-title {
  font-size: 2rem;
  color: var(--secondary-color);
  margin: 0;
}

.card-item-button {
  display: block;
  width: 100%;
  padding: 0.5rem;
  font-size: 1.8rem;
  text-align: center;
  background-color: var(--tertiary-color);
  color: var(--primary-color);
  border-radius: .5rem;
  transition: all .5s ease-out;
}

.card-item-button:hover {
  
  background-color: var(--secondary-color);
  color: var(--primary-color);
  word-spacing: 0.5rem;

}

.card-item-tag {
  color: var(--tertiary-color);
  font-size: 1rem;
}
</style>