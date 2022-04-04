<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="12">
        <v-text-field
          v-model="search"
          append-icon="mdi-magnify"
          label="Search"
          single-line
          hide-details
        ></v-text-field>
      </v-col>
      <v-col cols="12" sm="12">
        <v-data-table
          :headers="headers"
          :items="employee"
          :search="search"
          :items-per-page="-1"
        ></v-data-table>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      search: '',
      headers: [
        { text: 'ID', align: 'start', sortable: 'true', value: 'id' },
        { text: 'Name', align: 'start', sortable: 'true', value: 'name' },
        { text: 'Phone', align: 'start', sortable: 'true', value: 'phone' },
        { text: 'Profession', align: 'start', sortable: 'true', value: 'profession' },
      ],
      employee: [
        { id: 1, name: "Chandler Bing", phone: '305-917-1301', profession: 'IT Manager' },
        { id: 2, name: "Ross Geller", phone: '210-684-8953', profession: 'Paleontologist' },
        { id: 3, name: "Rachel Green", phone: '765-338-0312', profession: 'Waitress'},
        { id: 4, name: "Monica Geller", phone: '714-541-3336', profession: 'Head Chef' },
        { id: 5, name: "Joey Tribbiani", phone: '972-297-6037', profession: 'Actor' },
        { id: 6, name: "Phoebe Buffay", phone: '760-318-8376', profession: 'Masseuse' }
      ]
    }
  },
}
</script>
