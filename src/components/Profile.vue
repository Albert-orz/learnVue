<template>
    <div id="profile">
        <div>name: {{this.$route.params.name}} </div>
        <div>gender: {{this.$route.params.gender}}</div>
        <div>age: {{this.$route.params.age}}</div>
    </div>
</template>

<script>
export default {
    name: 'Profile',
}
</script>