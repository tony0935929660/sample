<template>
    <div class="page__body">
        <div class="row">
            <div v-for="color in colorList" :key="color">
                <colorComponent :color="color"/>
            </div>
        </div>
        <div class="row">
            <div v-for="color in colorList" :key="color">
                <searchComponent :color="color"/>
            </div>
        </div>
        <tableComponent :columns="columns"/>
    </div>
</template>
<script>
import colorComponent from '@/components/sample/ColorSample'
import searchComponent from '@/components/sample/SearchSample'
import tableComponent from '@/components/sample/TableSample'

export default {
  name: 'SampleView',
  components: {
    colorComponent,
    searchComponent,
    tableComponent
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

    const columns = [
        {
            "value": "Stock Number",
            "key": "stock_number"
        },
        {
            "value": "Name",
            "key": "name"
        },
        {
            "value": "Price",
            "key": "price"
        },
        {
            "value": "Industry",
            "key": "industry"
        },
        {
            "value": "Dividend",
            "key": "dividend"
        },
        {
            "value": "Target Price",
            "key": "target_price"
        }
    ]

    return {
        colorList,
        columns
    }
  }
}
</script>

<style>
.page__body {
    width: 100%;
    display: flex;
    flex-direction: column;
}

.row {
    width: 100%;
    margin: 30px 0px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    justify-content: space-around;
}

</style>
