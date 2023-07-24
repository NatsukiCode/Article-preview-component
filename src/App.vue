<script setup lang="ts"></script>

<template>
  <header>
    <!-- App.vue is the starting place for our vue app. In Index.html you can see a div with an id of app
    that div will display the contents of this App.vue file! -->
    <h2>Lets get started and look at App.vue!</h2>
    <div class="wrapper">
      <!-- Here we are calling the HelloWorld.Vue component and setting the msg attribute for it! -->
      <!-- setting the "msg" attribute here is setting the prop in HelloWorld.vue to be "You did it!" -->
      <HelloWorld msg="You did it! (This is passed through to the HelloWorld component from App.vue!)" />

      <!-- This is how we can create paging in our app
      See how these are setup in "src/router/index.ts"
      Using the RouterLink element will change the content in the RouterView to be whatever is in that view -->
      
    </div>
  </header>
  
  <!-- Anything contained in a RouterView will change depending on the current route (Url) that you are on! -->
  <!-- If you click on About, it will take you to /about.  -->
  <!-- See how the AboutView.vue html is displayed here -->
  <!-- It will basically replace this <RouterView /> line with   
  <div class="about">
    <h3>This is AboutView.vue !</h3>
  </div> -->
  
</template>

<style scoped>

a {
  padding-right: 2rem;;
}

</style>
