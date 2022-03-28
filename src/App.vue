<template>
  <div>
    <ChildHeader>
    </ChildHeader>
  </div>
  <div class="hero-container">
    <h3 class="hero-title">Lorem ipsum dolor sit.</h3>
    <p class="hero-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Non obcaecati sint deserunt necessitatibus totam quae inventore quos sunt ex esse.</p>
  </div>
  <div class="body-content">
    <div class="card-container">
    <Card 
    :title="products[0].title"
    :bgtext ="products[0].bgtext"
    :src ="products[0].src"
    :button ="products[0].button"
    :tag ="products[0].tag"
    />
    <Card 
    :title="products[1].title"
    :bgtext ="products[1].bgtext"
    :src ="products[1].src"
    :button ="products[1].button"

    />
    <Card 
    :title="products[2].title"
    :bgtext ="products[2].bgtext"
    :src ="products[2].src"
    :button ="products[2].button"
    
    />
  </div>
  </div>
  <div class="footer-content">
    <ChildFooter >
    </ChildFooter>
  </div>
</template>

<script setup>
// import {ref} from 'vue';
import Card from './components/Card.vue';
import ChildHeader from './components/ChildHeader.vue'
import ChildFooter from './components/ChildFooter.vue'

const products = ([
        {
          title: 'Forest One',
          button: 'More',
          bgtext: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Magnam pariatur.',
          src: require('./components/assets/forestOne.jpg'),
          tag: "#Forest, #Nature",
        },
        {
          title: 'Forest Two',
          button: 'More',
          bgtext: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Magnam pariatur.',
          src: require('./components/assets/forestTwo.jpg'),
          tag: "",
        },
        {
          title: 'Forest Three',
          button: 'More',
          bgtext: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Magnam pariatur.',
          src: require('./components/assets/forestThree.jpg'),
          tag: "",
        }
])
</script>

<style>
.hero-container {
  margin-bottom: 50px;
}
.hero-title {
  text-align: center;
  font-size: 2rem;
}
.hero-text {
  text-align: center;
  font-size: 1.5rem;
}

.card-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    
    gap: 1.5rem;
    border: 1rem;
}

body {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
html {
  height: 100%;
}
.body-content {
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  padding: 10px;
}

.footer-content {
  margin-top: auto;
}


</style>