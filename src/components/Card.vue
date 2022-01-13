<template>
    <div @click="changeIsMan()" class="card">
        <b>{{ name }}</b>
        <p>{{ schoolClass }}</p>
        <p>{{ phoneNumber }}</p>
        <p>{{ propsIsMan ? 'You\'re a man' : 'You are still a man'}}</p>
    </div>
</template>

<script>
function trueOrFalse(data) {
    if (data == 1) return true;
    return false;
}

export default {
    props: ['name', 'schoolClass', 'phoneNumber', 'getData', "isMan"],
    data() {
        return {
            compData: 'Hello',
            propsIsMan: trueOrFalse(this.isMan),
        }
    },
    methods: {
        changeIsMan() {
            console.log(this.propsIsMan) 
        }
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