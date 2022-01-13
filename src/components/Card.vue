<template>
    <div class="card">
        <b>{{ name }}</b>
        <p>{{ schoolClass }}</p>
        <p>{{ phoneNumber }}</p>
    </div>
</template>

<script>
export default {
    props: ['name', 'schoolClass', 'phoneNumber'],
    data() {
        return {
            
        }
    },
    methods: {

    }
}
</script>

<style scoped>
    .card {
        width: 10rem;
        border: 1px solid red;
    }

    .card p {
        margin: 0
    }
</style>