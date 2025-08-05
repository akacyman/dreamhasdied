<template>
  <div v-bind='{ class: "page "+menuitems[menuselect] }' id="root">

  <menubar>
    <menubox @menuselected="menuselect=2">Creator</menubox>
    <menubox @menuselected="menuselect=0"><img src="@/assets/morrisIcon.svg" width="58" height="50" border="0"></menubox> 
    <menubox @menuselected="menuselect=3">Contact</menubox>
  </menubar>

<pagetemplate :menuselect="menuselect" :thisselect="menuselect">
   <template v-if="menuselect === 2">
    <span class='headline'>I'm not an AI — Honest.</span>
  </template>

  <template v-else-if="menuselect === 3">
    <span class='headline'>Please don't contact me.</span>
  </template>

  <template v-else >
<div><span class='headline'>The dream has died.</span><br><span class='subheadline'>Bought domain 11 years ago...</span></div>
  </template>

</pagetemplate>

  <footer>&copy; Simon Mealings 2025</footer>

  </div>
</template>


<script>



</script>

<script type="text/javascript" src="./combine.js"></script>

<style lang="scss">
 @import "style.css"
</style>

