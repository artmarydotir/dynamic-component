<template>
    <div>
        <h3>The New </h3>
        <p class="alert alert-danger">does the dynamic component create every time? lets test to see the real behavier</p>
        <button @click="counter++ " class="btn btn-success"> Increase me</button>
        <p>{{ counter }} </p>
        <p>As we see 
            the component destroy and create everytime.
            The component will DIE.
            we can check this by destroy hook too!
        </p>
    </div>
</template>

<script>

export default {
    data() {
        return {
            counter: 0,
        }
    },
    destroyed() {
        console.log('destroyed!');
    }
}
</script>

<style>

</style>
