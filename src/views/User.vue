<template>
    <div id="User">
        <h1>Hello!</h1>
        <h2>User: {{this.$route.params.id}}</h2>
        <div class="nav">
            <div @click='showProfile'>show porfile</div> |
            <div @click="showPost">show post</div>
        </div>

        <router-view  />

    </div>
</template>

<script>
export default {
    name: 'User',
    methods: {
        showProfile(){
            this.$router.push(
                {
                    name: 'Profile',
                    params:{
                        name: 'Albert',
                        gender: 'Male',
                        age: 20,
                    }
                }
            )
        },
        showPost(){
            this.$router.push(
                {
                    name: 'Post',
                    params:{
                        article: 'Hello Wordd',
                        content: 'Hello, world. I hope we can make good friends.',
                    }
                }
            )
        }
    },
    mounted(){
        
    }
}
</script>

<style scoped>
.nav{
    display: flex;
    justify-content:center;
}
</style>