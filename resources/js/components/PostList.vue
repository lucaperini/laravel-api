<template>
    <div>
        <Post v-for="(post, index) in posts" :key="index" :post="post"/>
    </div>
</template>

<script>
import Post from './Post.vue';
export default {
    name: "PostList",
    components: {
        Post
    },
    data: function() {
        return {
            posts: [],
        }
    },
    methods: {
        getPosts(){
            axios.get("http://localhost:8000/api/posts")
            .then((result) =>{

                this.posts = result.data.data;
            })
            .catch( (error) =>{
                console.warn(error);
            });
        }
    },
    created(){
        this.getPosts();
    }
}
</script>
