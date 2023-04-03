<template>
    <table class="table__body" cellspacing="0">
        <tr class="table__body--header">
            <th v-for="item in columns" :key="item.key"> 
                {{ item.value }} 
            </th>
        </tr>
        <tr v-for="datum in data" :key="datum">
            <td v-for="item in columns" :key="item.key"> 
                {{ datum[item.key] }}
            </td>
        </tr>
    </table>
</template>
<script>
export default {
    props: {
        columns: {
            required: true,
            type: Object
        }
    },
    setup() {
        const data = [
            {"stock_number": 2330,
            "name": "台積電",
            "price": 530,
            "industry": "半導體",
            "dividend": 2.2,
            "target_price": 700},
            {"stock_number": 2382,
            "name": "廣達",
            "price": 89,
            "industry": "電子",
            "dividend": 6,
            "target_price": 100}
        ]
        
        return {
            data
        }
    }
}
</script>
<style>
.table__body {
    width: 100%;
    background-color: white;
    border: none;
    font-size: 20px;
}

tr:first-child th:first-child { border-top-left-radius: 10px; }
tr:first-child th:last-child { border-top-right-radius: 10px; }

tr:last-child td:first-child { border-bottom-left-radius: 10px; }
tr:last-child td:last-child { border-bottom-right-radius: 10px; }

th {
    border: none;
    padding: 20px 0px;
    background-color: aquamarine;
}

td {
    padding: 10px 0px;
}
</style>
