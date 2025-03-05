<script>
    export default {
        props:({
            item: {
                type: Object,
                default: () => ({})
            },
            headers: {
                type: Array,
                default: []
            },
        })
    }
</script>

<template>
    <tr>
        <td v-for="head in headers" :key="head.value">
            <div v-if="head.value === 'actions'">
                <div class="dropdown" >
                    <button class="dropbtn">Действия</button>
                    <div class="dropdown-content" style="left:0;">
                        <button>Редактировать</button>
                        <button>Уволить</button>
                    </div>
                </div>
            </div>
            <div v-else>
                {{ item[head.value] }}
            </div>
        </td>
    </tr>
</template>

<style>
.employeeRecords {
  border: 3px solid #000000;
  width: 100%;
  text-align: left;
  border-collapse: collapse;
  margin-top: 20px;
}

.employeeRecords td, th {
  border: 1px solid #000000;
  padding: 5px 4px;
}

.employeeRecords thead th {
  font-size: 15px;
  font-weight: bold;
  color: #000000;
  text-align: left;
}

.dropbtn {
    background-color: #7a7a7a;
    color: white;
    padding: 5px;
    font-size: 16px;
    border: none;
    cursor: pointer;
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 100px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
    padding: 5px;
}

.dropdown-content button {
    color: black;
    padding: 5px 5px;
    text-decoration: none;
    display: flex;
    cursor: pointer;
    width: 100%;
}

.dropdown-content button:hover {
    background-color: #929292;
}

.dropdown:hover .dropdown-content {
    display: block;
}

.dropdown:hover .dropbtn {
    background-color: #444444;
}
</style>