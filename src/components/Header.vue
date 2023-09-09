<script setup>
import Logo from '@/components/system/Logo.vue'
import { RouterLink } from 'vue-router'

import useUsersStore from '@/stores/UserStore.js'

const userStore = useUsersStore()
</script>

<template>
  <header class="topnav" id="myTopnav">
    <a href="#home" class="active">Home</a>
    <a href="#news">News</a>
    <a href="#contact">Contact</a>
    <a href="#about">About</a>
    <a href="javascript:void(0);" class="icon" onclick="myFunction()">
      <i class="fa fa-bars"></i>
    </a>
  </header>
</template>

<style scoped>
header {
  margin-left: 200px;
  width: 100%-200px;
}

/* Add a black background color to the top navigation */
header {
  background-color: #333;
  overflow: hidden;
  position: fixed;
}

/* Style the links inside the navigation bar */
header a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

/* Change the color of links on hover */
header a:hover {
  background-color: #ddd;
  color: black;
}

/* Add an active class to highlight the current page */
header a.active {
  background-color: #04aa6d;
  color: white;
}

/* Hide the link that should open and close the topnav on small screens */
header .icon {
  display: none;
}

/* When the screen is less than 600 pixels wide, hide all links, except for the first one ("Home"). Show the link that contains should open and close the topnav (.icon) */
@media screen and (max-width: 600px) {
  .topnav a:not(:first-child) {display: none;}
  .topnav a.icon {
    float: right;
    display: block;
  }
}

/* The "responsive" class is added to the topnav with JavaScript when the user clicks on the icon. This class makes the topnav look good on small screens (display the links vertically instead of horizontally) */
@media screen and (max-width: 600px) {
  .topnav.responsive {position: relative;}
  .topnav.responsive a.icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
}
</style>
