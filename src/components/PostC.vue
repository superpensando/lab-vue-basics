<template>
    <div class="post">     
            <h2>{{ title }} - {{ idPost }} </h2>
            <p>{{ description }} - {{ idPost }}</p>
            <div>
                {{ content }} - {{ idPost }}
            </div>
    </div>
</template>

<script>
export default {
    name: 'PostC',
    props: {
        idPost: Number,
        title: String,
        description: String,
        content: String,
    }
}
</script>

<style lang="scss">
.post {
    padding: 30px;
    border: 2px dashed green;
}
</style>