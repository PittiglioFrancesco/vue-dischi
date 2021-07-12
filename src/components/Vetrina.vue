<template>
  <div class="my-5 container">

    <div class="row">
        <h1 class="text-center text-uppercase">Vetrina</h1>
    </div>

    <div class="row">
        <h3 class="text-uppercase">Cerca</h3>
    </div>

    <div class="row riga3">
        <input type="text" placeholder="Cerca un disco" @keyup="submitSearch" v-model="searchText">
        <button>Reset</button>
        <button>Cerca</button>
    </div>

  </div>
</template>

<script>
import 'axios';
import axios from 'axios';

export default {

}

axios
    .get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(function (response){
        const result = response.data;
        console.log(result.response.poster);
    });
</script>

<style lang="scss" scoped>

// div generale

div{
  .riga3{
    input{
      display: inline;
    }
    button{
      display: inline;
    }
  }
}

</style>