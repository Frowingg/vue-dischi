<template>
    <div>
        <div class="loader">
            <img src="../assets/lightning-svgrepo-com.svg" alt="load-img">
            <div class="text">
            Loading...            
            </div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'loaderComponent'
}
</script>

<style lang="scss" scoped>
    .loader{
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
    }
    svg{
        width: 75px;
        margin: 1rem auto;
        animation: pulse 1s infinite alternate;
    }

    @keyframes pulse{
        from{
            transform: scale(1);
        }
        to {
            transform: scale(1.3);
        }
    }
    .text{
        text-transform: uppercase;
        letter-spacing: 2px
    }
    img{
    width: 50px;
}
</style>