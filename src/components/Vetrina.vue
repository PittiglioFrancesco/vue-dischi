<template>
  <div class="my-5 container">

    <div class="row">
        <h1 class="text-center text-uppercase">Vetrina</h1>
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

</style>