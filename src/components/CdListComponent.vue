<template>
    <div class="container">
        <div class="row">
            <div class="col-3 col-md-6 col-lg-8" v-for="cd in CdList" :key="cd.id">

            </div>
            <div class="col-3 col-md-6 col-lg-8">

            </div>
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
            })
            .catch((err) =>
                console.log('error', err)
            )}
        }
}


</script>

<style lang="scss" scoped>

</style>