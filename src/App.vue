<template>
  <mdb-container>
    <mdb-row>
      <mdb-col>
        <h4 class="text-center h4-responsive font-weight-bold align-middle">Welcome to your dashboard</h4>
      </mdb-col>
      <mdb-col>
        <settings/>
      </mdb-col>
    </mdb-row>
    <mdb-row>
      <mdb-col xs="12" md="7" class="order-md-1">
        <p>todo-list</p>
      </mdb-col>
      <mdb-col xs="12" md="5" class="order-md-12">
        <p>all other stuff</p>
      </mdb-col>
    </mdb-row>
  </mdb-container>
</template>

<script>
import {
  mdbContainer,
  mdbRow,
  mdbCol,
} from "mdbvue";
import settings from "@/components/settings";
export default {
  name: 'app',
  components: {
    settings,
    mdbContainer,
    mdbRow,
    mdbCol,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
