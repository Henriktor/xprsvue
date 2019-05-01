<template>
    <div class="home">
        <img alt="Vue logo" src="../assets/logo.png">
        <HelloWorld msg="Welcome to Your Vue.js App" />
        <GChart type="LineChart" :data="chartData" :options="chartOptions" />
        <div class="list">
            <ListLister />
            <ul>
                <p v-for="item in items" v-bind:key="item.id">{{item.msg}}</p>
            </ul>
        </div>
    </div>
</template>
<script>
// @ is an alias to /src
import { GChart } from 'vue-google-charts';
import HelloWorld from '../components/HelloWorld.vue';
import ListLister from '../components/ListLister.vue';

export default {
  name: 'home',
  data() {
    return {
      // Array will be automatically processed with visualization.arrayToDataTable function
      chartData: [
        ['Year', 'Happiness', 'Expenses', 'Porn'],
        ['2014', 1000, 400, 1000],
        ['2015', 1100, 700, 750],
        ['2016', 200, 344, 20],
        ['2017', 800, 540, 1000],
        ['2018', 1030, 540, 350],
        ['2019', 1030, 540, 350],
        ['2020', 1030, 540, 350],
      ],
      chartOptions: {
        chart: {
          title: 'Company Performance',
          subtitle: 'Sales, Expenses, and Profit: 2014-2017',
        },
      },
    };
  },

  components: {
    HelloWorld,
    ListLister,
    GChart,
  },
};
</script>
