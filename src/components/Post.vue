<template>
    <div class="post">
        <div>article: {{this.$route.params.article}}</div>
        <div>content: {{this.$route.params.content}}</div>
    </div>
</template>

<script>
export default {
    name: 'Post',
}
</script>