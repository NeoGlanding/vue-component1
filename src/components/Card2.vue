<template>
    <div class="card">
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
    }    
}
</script>

<style scoped>

</style>