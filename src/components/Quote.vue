<template>
    <div>
        <slot name="first-slot"></slot>
        <slot name="second-slot"></slot>
        <slot>
        </slot>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
    div {
        border: 1px solid #ccc;
        box-shadow: 1px 1px 2px black;
        padding : 30px;
        margin: 30px auto;
        text-align: center;
    }
    h2 {
        /* style slot in child component apply
         */
         color: rebeccapurple;
    }
</style>

