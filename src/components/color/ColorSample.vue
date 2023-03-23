<template>
    <div class="colorBar">
    </div>
    <br>
    {{color}}
</template>

<script>
export default {
    props: {color: String},
}
</script>

<style>
.colorBar {
    width: 100px;
    height: 100px;
    background-color: v-bind(color);
    border-radius: 40px;
    border: 3px solid #E0E0E0;
}
</style>
