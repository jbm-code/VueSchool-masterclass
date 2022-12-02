<template>
    <div>Hello from page home</div>
    <div 
        v-for="thread of threads" :key="thread.id"> 
        <h2>{{thread.title}}</h2>  
        <div v-for="postId of thread.posts" :key="postId">
            <p>{{posts.find(p => p.id === postId).text}}</p>
        </div>
    </div>
</template>

<script>
import sourceData from "@/data.json"

export default {
    data () {
        return {
            threads: sourceData.threads,
            posts: sourceData.posts,
            
        }
    }
}

</script>


<style scoped>


</style>