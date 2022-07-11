<template>
    <div>
        <div class="cont">
            <label for="genre">Genre</label>
            <input v-model="genreToSearch" type="text-area" id="genre" placeholder="Search...">
            <button @click="genreFilter" type="button" class="my-btn btn btn-primary">Search</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'selectGenre',
    data() {
        return{
            genreToSearch: '',
        }
    },
    methods: {
        genreFilter() {
            
        }
    }
}
</script>

<style lang="scss" scooped>
.cont{
    display: flex;
    align-items: center;
}
label{
    color: white;
    margin: 0 20px;
}
input{
    margin: 0 20px;
    height: 20px;
}
.cont .my-btn{
    border-radius: 0;
    height: 20px;
    font-size: 11px;
    margin-right: 20px;
}

</style>