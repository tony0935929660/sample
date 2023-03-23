<template>
    <div class="page__body">
        <div v-for="color in colorList" :key="color">
            <div class="column">
                <colorComponent :color="color"/>
                <br>
                <br>
                <br>
                <searchComponent :color="color"/>
            </div>
        </div>
    </div>
</template>
<script>
import colorComponent from '@/components/color/ColorSample.vue'
import searchComponent from '@/components/color/SearchSample.vue'

export default {
  name: 'SampleView',
  components: {
    colorComponent,
    searchComponent
  },
  setup() {
    const colorList = [
        '#FFFF6F',
        '#81C0C0',
        '#B9B973',
        '#C07AB8',
        '#0066CC',
        '#804040',
    ]

    return {
        colorList
    }
  }
}
</script>

<style>
.page__body {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}
.column {
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>
