<template>
    <div @click="clickEvent" class="card">
        <p>{{ name }}</p>
        <p>{{ active ? 'This user is Active' : 'This user is inactive'}}</p>
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
        },
        active: {
            type: Boolean,  
        }
    },
    methods: {
        clickEvent() {
            this.$emit('find-name', this.name)
        }
    }    
}
</script>

<style scoped>
    .card {
        padding: 1rem;
        border: 1px solid blue;
        width: 20rem;
    }
</style>