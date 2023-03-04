<template>
    <div class="page__body">
        <div class="row">
            <div v-for="color in colorList" :key="color">
                <colorComponent :color="color"/>
            </div>
        </div>
    </div>
</template>
<script>
import colorComponent from '@/components/color/ColorSample.vue'

export default {
  name: 'SampleView',
  components: {
    colorComponent
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
}
.row {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}
</style>
