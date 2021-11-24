<template>
    <div class="card">
        <div class="card-img">
            <img :src="url" :alt="title">
        </div>
        <h3>{{ title }}</h3>
    </div>
</template>

<script>
export default {
    name: 'Cards',
    props: {
        url: String,
        title: String
    }
}
</script>

<style scoped lang="scss">

.card-img{
    width: 100%;
    height: 300px;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top left;
    }
}
h3{
     margin-top: 15px;
}
</style>