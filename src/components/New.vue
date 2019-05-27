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
        <p class="alert alert-warning">
            if we use keep alive , we lose the destroy hook.
            what is the alternative to keep hook?
            there is two hook : that we can use instead:
            <br>
            <span>
                1- deactivated()
            </span>
            <br>
            <span>
                2-activated()
            </span>


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
    },
    deactivated() {
        console.log('deactivated!');
    },
    activated() {
        console.log('activated!');
    }
}
</script>

<style>

</style>
