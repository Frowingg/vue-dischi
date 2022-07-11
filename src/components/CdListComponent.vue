<template>
    <div class="container">
        <div class="row row-cols-5">
        
            <CdComponent :info="cd" v-for="(cd, index) in CdList" :key="index"/>

        </div>
    </div>
</template>

<script>
import axios from 'axios';
import CdComponent from './CdComponent.vue';

export default {
    name: 'CdListComponent',
    components: {
        CdComponent
    },
    data() {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            CdList: [],
        }
    },
    created() {
        this.getCd();
    },
    methods:{
        getCd() {
            axios.get(this.url).then((result) => {
                this.CdList = result.data.response
                console.log(this.CdList)
            })
            .catch((err) =>
                console.log('error', err)
            )}
        }
}


</script>

<style lang="scss" scoped>
.container{
    width: 60%;
}
</style>