<script>
  export default {
    data() {
      return {
        items: [
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
          { content: 'ФИО' },
        ]
      }
    },
  }
</script>

<template>
  <div>
    <table class="minimalistBlack">
<thead>
<tr>
<th v-for="item in items" :key="item">{{ item.content }}</th>
</tr>
</thead>

<tbody>
<tr>
<td>cell1_1</td>
<td>cell2_1</td>
<td>cell3_1</td>
<td>cell4_1</td>
<td>cell5_1</td>
<td>cell6_1</td>
<td>cell7_1</td>
<td>cell8_1</td>
<td>cell9_1</td>
</tr>
</tbody>
</table>
  </div>
</template>



<style scoped>

</style>