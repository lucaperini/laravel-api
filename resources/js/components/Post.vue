<template>
<div class="col-4">
    <div class="card">
        <img :src="post.image_url" class="card-img-top" style="width:18rem;" :alt="'image of ' + post.title">
        <div class="card-body">
            <div class="card-title">
                {{post.title}}
            </div>
            <div class="subtitle">
                {{post.author}}
            </div>
            <div class="card-text">
                {{post.content}}
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {

    name: "Post",
    components: {
    },
    props:['post']
}
</script>

<style>

</style>


