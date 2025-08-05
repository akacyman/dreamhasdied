<template>
  <div v-bind='{ class: "page "+menuitems[menuselect] }' id="root">

  <menubar>
    <menubox @menuselected="menuselect=2">Creator</menubox>
    <menubox @menuselected="menuselect=0"><img src="@/assets/morrisIcon.svg" width="58" height="50" border="0"></menubox> 
    <menubox @menuselected="menuselect=3">Contact</menubox>
  </menubar>

<pagetemplate :menuselect="menuselect" :thisselect="menuselect">
   <template v-if="menuselect === 2">
    Creator<br><br>I'm just a guy<br>
  </template>

  <template v-else-if="menuselect === 3">
    Please don't contact me.
  </template>

  <template v-else >
The dream has died.
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

