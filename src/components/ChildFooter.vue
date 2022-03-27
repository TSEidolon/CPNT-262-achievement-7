<template>
  <div class="footerContainer">
    <p class="footerText">&copy; Edgar Caballero 2022</p>
  </div>
</template>



<style>
  .footerContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgb(26, 24, 24);
    color: white;
    position: absolute;
    bottom: 0;
    width: 100%;
    margin-top: 1rem;
  }
  @media (max-width: 1800px) {
    .footerContainer {
      position: relative;
      bottom: 0;
    }
    
  }

</style>