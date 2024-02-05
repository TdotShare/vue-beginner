<template>
  <v-table>
    <thead>
      <tr>
        <th>#</th>
        <th class="text-left">ชื่อโปเกมอน</th>
        <th>ข้อมูล</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(item, index) in dataPokemon || []" :key="item.name">
        <td>{{ index + 1 }}</td>
        <td>{{ item.name }}</td>
        <td>
          <a target="_blank" :href="item.url"><v-btn>ดูข้อมูล</v-btn></a>
        </td>
      </tr>
    </tbody>
  </v-table>
</template>

<script>
export default {
  props: {
    dataPokemon: Array
  },
}
</script>

<style></style>
