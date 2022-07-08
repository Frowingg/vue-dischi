<template>
    <div class="container">
        <div class="row" v-for="(cd, index) in CdList" :key="index">

            <CdComponent :info="cd" />

        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'CdListComponent',

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

</style>