<template>
  <div id="app">
  <router-view class="view-router"  ></router-view>
  </div>
   
</template>

<style>
body {
  font-size: 16px;
  background-color: #f8f8f8;
  -webkit-font-smoothing: antialiased;
}

.view-router {
	height: 100%;
	overflow-y: auto;
	padding-bottom: 50px;
	box-sizing: border-box;
	overflow-x: hidden;
}
.autoImg{
  display: block; 
  margin-left: auto; 
  margin-right: auto;
  max-width: 100%;
  max-height: 100%;
}
</style>
