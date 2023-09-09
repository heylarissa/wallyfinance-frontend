<script setup></script>

<template>
  <nav>
    <ul>
      <li><a>Home</a></li>
      <li><a>Analytics</a></li>
      <li><a>Accounts</a></li>
      <li><a>Groups</a></li>
      <li><a>Invoices</a></li>
      <li><a>Documents</a></li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  margin: 0;
  padding: 0;
  width: 200px;
  background-color: #f1f1f1;
  position: fixed;
  height: 100%;
  overflow: auto;
  top: 0;
  z-index: 100;
}

/* Sidebar links */
nav li {
  display: block;
  color: black;
  padding: 16px;
  text-decoration: none;
}

/* Active/current link */
nav li.active {
  background-color: #04aa6d;
  color: white;
}

/* Links on mouse-over */
nav li:hover:not(.active) {
  background-color: #555;
  color: white;
}
</style>
