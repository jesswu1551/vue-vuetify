<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-icon>mdi-tooltip-account</v-icon>
        <span class="mx-2 font-weight-bold hidden-sm-and-down">Employee</span>
      </div>
    </v-app-bar>

    <v-main>
      <InputForm/>
      <DataTable/>
    </v-main>
  </v-app>
</template>

<script>
import DataTable from './components/DataTable';
import InputForm from './components/InputForm';

export default {
  name: 'App',

  components: {
    DataTable,
    InputForm
  },

  data: () => ({
    //
  }),
};
</script>
