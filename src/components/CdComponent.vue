<template>
    <div class="col-3">
        <img :src="info.poster" :alt="info.title">
        <h2>{{info.title}}</h2>
        <div class="sub-titile">{{info.author}}</div>
        <div class="year-of-prodaction">{{info.year}}</div>
    </div>
</template>

<script>
export default {
    name: 'CdComponent',
    props: ['info'],
}

</script>

<style lang="scss" scoped>

</style>