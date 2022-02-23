<template>
    <main>
        <div class="container mt-5">
            <h1>Posts list</h1>


        </div>
    </main>
</template>

<script>
export default {
    name: 'Main',
    data() {
        return {
            posts: []
        }
    },
    created() {
        axios.get('api/posts')
            .then((response) => {
                this.posts = response.data;
            })
    }
}
</script>

<style lang='scss' scoped>

</style>