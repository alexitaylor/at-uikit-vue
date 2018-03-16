<template>
  <at-table :columns="columns" :data="data" pagination></at-table>
</template>

<script>

export default {
  name: 'Table',
  data() {
    return {
      columns: [
        {
          title: 'Name',
          key: 'name',
        },
        {
          title: 'Age',
          key: 'age',
          sortType: 'normal',
        },
        {
          title: 'Address',
          key: 'address',
        },
      ],
      data: this.makePageData(),
    };
  },
  methods: {
    makePageData() {
      const data = [
        {
          name: 'Stephen Curry',
          age: 18,
          address: 'Shenzhen Shi, Baoan Qu',
        },
        {
          name: 'Lebron James',
          age: 25,
          address: 'Gangding, Tianhe, Guangzhou',
        },
        {
          name: 'Kobe Bryant',
          age: 24,
          address: 'Pudong, Shanghai',
        },
        {
          name: 'Kevin Durant',
          age: 22,
          address: 'Shen Nan Da Dao, Nanshan Qu, Shenzhen Shi',
        },
        {
          name: 'Russell Westbrook',
          age: 21,
          address: 'Chaoyang District, Beijing',
        },
        {
          name: 'Tim Duncan',
          age: 26,
          address: 'The Mixc of Shenzhen City ',
        },
        {
          name: 'Tony Parker',
          age: 25,
          address: 'Shenzhen Book City',
        },
        {
          name: 'Kyrie Irving',
          age: 20,
          address: 'Guangzhou Higher Education Mega Center',
        },
        {
          name: 'Isaiah Thomas',
          age: 19,
          address: 'Chaoyang District, Beijing',
        },
      ];
      let pageData = [];

      for (let i = 0; i < 5; i += 1) {
        pageData = pageData.concat(data);
      }

      return pageData;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
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
</style>
