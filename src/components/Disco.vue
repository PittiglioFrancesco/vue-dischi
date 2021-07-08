<template>
  <div>
      <div class="row justify-content-center">

        <div class="col-2 text-center bgc-1" v-for="disco in discoList" :key="disco.id">
            <img :src="disco.poster" :alt="disco.poster">
            <h3 class="text-uppercase bgc-1"> {{disco.title}} </h3>
            <p class="gray bgc-1">{{disco.author}}</p>
            <span class="gray bgc-1">{{disco.year}}</span>
        </div>

    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
    name: "dischi",
    data(){
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            discoList: []
        }
    },
    created(){
        this.getDisco()
    },
    methods:{
        getDisco(){
            axios
            .get(this.apiUrl)
            .then(response => {
            this.discoList = response.data.response;
            console.log(this.discoList);
        });
        }
    }

}
</script>

<style lang="scss" scoped>

div{
    div{
    margin: 30px 0;
    // div col dischi
    div{
        width: 240px;
        img{
            margin-top: 20px;
            margin-bottom: 10px;
            width: 200px;
            height: 200px;
        }
    }
}
}

</style>