<template>
    <div class="col mt-2">
        <div class="card">
            <img :src="info.poster" :alt="info.title">
            <h6>{{info.title.toUpperCase()}}</h6>
            <div class="sub-title">{{info.author}}</div>
            <div class="year-of-production">{{info.year}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CdComponent',
    props: ['info'],
}

</script>

<style lang="scss" scoped>
.card{
    margin-bottom: 20px;
    background-color: #2e3a46;
    padding: 15px;
    text-align: center;
    color: white;
    height: 250px;

    .sub-title, .year-of-production{
        color: gray;
    }
    .sub-title{
        font-size:12px
    }
    .year-of-production{
        font-size: 10px
    }
}
</style>