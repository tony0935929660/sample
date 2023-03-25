<template>
    <div class="searchBar">
        <div class="searchBar__input"> 
            <input class="searchBar__input--input"/>
            <button class="searchBar__input--icon">
                <font-awesome-icon style="font-size:18px; color:white" icon="magnifying-glass"/>
            </button>
        </div>
    </div>
</template>

<script>
export default {
    props: {color: String},
}
</script>

<style>
.searchBar {
    border-radius: 40px;
    border: 3px solid v-bind(color);
    width: 200px;
    height: 35px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.searchBar__input {
    border-radius: 20px;
    background-color: white;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.searchBar__input--input {
    border-radius: 15px;
    outline: none;
    border: none;
    width: 70%;
    height: 30px;
    margin: 0px 10px;
}

.searchBar__input--icon {
    border-radius: 15px;
    background-color: v-bind(color);
    outline: none;
    border: none;
    width: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.searchBar__input--icon:hover {
    background-color: gray;
    cursor: pointer;
}

</style>
