<template>
  <div>
    <nav class="navbar">
      <div class="brand-title">Logo</div>
      <a href="#" class="toggle-button">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </a>
      <div class="navbar-links">
        <ul>
          <li><a href="">Gallery</a></li>
          <li><a href="">Products</a></li>
          <li><a href="">About</a></li>
        </ul>
      </div>
    </nav>
  </div>
</template>
<script setup>
import {onMounted} from 'vue'

onMounted (() => {
  const toggleButton = document.getElementsByClassName('toggle-button')[0];
  const navbarLinks = document.getElementsByClassName('navbar-links')[0];

  toggleButton.addEventListener('click', () => {
  navbarLinks.classList.toggle('active')
})})

</script>

<style>
  /* Navbar styles  */
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: rgb(26, 24, 24);
    color: white;
  }

  .brand-title {
    font-size: 3rem;
    margin:0.5rem;
  }

  .navbar-links ul{
    margin: 0;
    padding: 0;
    display: flex;
  }

  .navbar-links li {
    list-style: none;
  }

  .navbar-links li a {
    text-decoration: none;
    color: white;
    padding: 1rem;
    display: block;
    font-size: 1.5rem;
  }

  /* Hamburger styles  */
  .toggle-button {
    position: absolute;
    top: 1.5rem;
    right: 1rem;
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 30px;
    height: 21px;
  }
  .toggle-button .bar {
    height: 3px;
    width:100%;
    background-color: white;
    border-radius: 10px;
  }
  @media (max-width: 800px) {
    .toggle-button {
      display: flex;
    }
    .navbar-links{
      display: none;
      width: 100%
    }
    .navbar {
      flex-direction: column;
      align-items: flex-start;
    }
    .navbar-links ul{
      width: 100%;
      flex-direction: column;
    }
    .navbar-links ul li {
      text-align: center;
    }
    .navbar-links li a {
      padding: 0.5rem 1rem;
    }
    .navbar-links.active {
      display: flex;
    }
  }

  /* Hover  */
  .navbar-links li:hover{
    background-color: #555;
  }

</style>
