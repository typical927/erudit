<template>
  <link href="https://fonts.cdnfonts.com/css/inter" rel="stylesheet">
   <link href="https://fonts.cdnfonts.com/css/black-han-sans" rel="stylesheet">

<h2> Resources</h2>
  <div class="aaa">
    <div class="aaasect">
    <a href="general"><img class="miku" src="https://cdn.discordapp.com/attachments/1147480257029492746/1149278593592070206/image.png"></a>
    <h3 class="left">General</h3>
    </div>
    <div class="aaasect"></div>
    <a href="disorders"><img class="miku2" src="https://i.pinimg.com/564x/65/37/72/653772c1b8d690e5cce4273c922037bb.jpg"></a>
    <h3 class="left">Disorders</h3>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
/* general css */
h2 {
  font-family: 'Black Han Sans', sans-serif;
  font-size: 35px;
  text-align: center;
  color: #36c0b3;
  margin-top: 30px;
  margin-bottom: 20px;
}

h3 {
  font-family: 'Inter', sans-serif;  
  font-size: 32px;
  font-weight: bold;
  text-decoration: underline;
  color: #118E95;
  margin-bottom: 15px;
}

p, li {
  font-family: 'Inter', sans-serif;  
  font-size: 18px;
  text-align: left;
}

.rsc a {
    color: #47c8c0;
    text-decoration: underline;
}

ul {
  list-style-type: disc;
}

.aaa img {
  width: 300px;
  margin: 10px;
}

.aaa {
  display: flex;
  align-items: center;
  margin: auto;
}

.aaasect {
  width: 450px;
  align-items: center;
}

.left {
  text-align: left;
  margin-top: 0px;
}

</style>
