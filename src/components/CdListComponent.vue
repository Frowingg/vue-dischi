<template>
    <div class="container">
        <div v-if="isLoaded" class="row row-cols-5">
        
            <CdComponent :info="cd" v-for="(cd, index) in CdList" :key="index" />

            
        </div>
        <loaderComponent v-else />
    </div>
</template>

<script>
import axios from 'axios';
import CdComponent from './CdComponent.vue';
import loaderComponent from './loaderComponent.vue';

export default {
    name: 'CdListComponent',
    components: {
        CdComponent,
        loaderComponent
    },
    data() {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            CdList: [],
            isLoaded: false,
        }
    },
    created() {
        this.getCd();
    },
    methods:{
        getCd() {
            axios.get(this.url).then((result) => {
                this.CdList = result.data.response;
                this.isLoaded = true;
                console.log(this.CdList);
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