<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <md-layout :md-gutter="8">
      <md-layout :md-flex="100">
        <md-card>
         <div class="md-header-container">
          <div class="tim-logo"></div>
          <img class="roma-logo" src="../assets/logo.png">
          <md-card-header>
            <div class="md-title">
              As Roma Players &amp; Staff
            </div>
            <div class="md-subhead">
              Current Team Roster
            </div>
          </md-card-header>
          <md-card-content>
            <md-button class="md-raised md-primary">Primary Button</md-button>
            <md-button class="md-raised md-secondary">Secondary Button</md-button>
          </md-card-content>
        </div>
        <md-table v-once>
          <md-table-header>
            <md-table-row>
              <md-table-head>Full Name</md-table-head>
              <md-table-head md-numeric>Position</md-table-head>
              <md-table-head md-numeric>Number</md-table-head>
              <md-table-head md-numeric>Nationality</md-table-head>
              <md-table-head md-numeric>Contract End Date</md-table-head>
              <md-table-head md-numeric>Player Market Value</md-table-head>
            </md-table-row>
          </md-table-header>

          <md-table-body>
            <md-table-row v-for="(row, index) in 5" :key="index">
              <md-table-cell>Data</md-table-cell>
              <md-table-cell v-for="(col, index) in 5" :key="index" md-numeric>10</md-table-cell>
            </md-table-row>
          </md-table-body>
        </md-table>
      </md-card>
    </md-layout>
  </md-layout>
</div>
</template>

<script>
  export default {
    name: 'hello',
    data () {
      return {
        msg: 'As Roma Roster Card'
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-family: 'Roboto', Helvetica, Arial, sans-serif;
    font-weight: 100;
    letter-spacing: -0.5px;
    font-size: 30px;
    line-height: 36px;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
  .roma-logo {
    margin: 25px 0 0 25px;
  }

  .md-theme-default.md-card {
  }
  .md-title {
    font-weight: 900;
    color: white;
  }
  .md-subhead {
    color: white;
  }
  .md-header-container {
    background-image: url("../assets/btn-bg.png")!important;
    background-size: cover;
  }
  .tim-logo {
    background-image: url(../assets/serie-a-logo.png);
    min-height: 72px;
    width: 60px;
    float: right;
    margin: 10px;
  }
  .md-card-header {
    padding: 20px 25px 0px!important;
  }
  thead {
    border-bottom: 1px solid #ccc;
    background: #9f9f9f!important;
  }
  .md-table-head-text {
    color: #2b2b2b;
  }
  .md-table-row {
    color: rgba(0,0,0,.70)!important;
  }
  .md-table .md-table-cell {
    cursor: pointer;
  }
  .md-primary {
    background-color: #f89728!important;
    color: white!important;
    opacity: 1;
  }
  .first-column {
    background: red;
  }
</style>
