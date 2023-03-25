<template>
    <div class="table__body">
        <div class="table__body--field">
            <div v-for="column in columns" :key="column">
                {{ column }}
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: {columns: Array},
    setup() {
        
        return {

        }
    }
}
</script>
<style>
.table__body {
    width: 100%;
    background-color: white;
    border-radius: 30px;
    padding: 30px 0px;
    font-size: 20px;
}
.table__body--field {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

</style>
