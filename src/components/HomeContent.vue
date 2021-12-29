<template>
  <div class="content">
    <div class="filter-sort">
      <div class="search">
        <label for="search">Search</label>
        <input placeholder="name" type="text" v-model="filter" />
      </div>
      <div class="sort">
        <label for="type">Company Rank</label>
        <select v-model="sort">
          <option
            v-for="(item, i) in options"
            :key="i"
            :label="item.label"
            :value="item.value"
          ></option>
        </select>
      </div>
    </div>
    <div class="data-table">
      <table>
        <thead>
          <tr>
            <th>Name</th>
            <th>Company Rank</th>
            <th>Company Address</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(company, i) in getCompany" :key="i">
            <td>
              {{ company.name }}
            </td>
            <td>
              {{ company.rank }}
            </td>
            <td>
              {{ company.address }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      filter: "",
      sort: "",
      options: [
        { label: "All", value: "none" },
        { label: "Top Rank", value: "rank" },
      ],
      companies: [
        {
          name: "acc",
          rank: 55,
          address: "Abc kochi",
        },
        {
          name: "abc",
          rank: 13,
          address: "Abc kochi",
        },
        {
          name: "acd",
          rank: 83,
          address: "acd kochi",
        },
        {
          name: "xyz",
          rank: 43,
          address: "acd kochi",
        },
        {
          name: "xyy",
          rank: 51,
          address: "acd kochi",
        },
      ],
    };
  },
  computed: {
    getCompany() {
      let companies = this.companies.filter((company) => {
        return company.name.toLowerCase().includes(this.filter.toLowerCase());
      });

      if (this.sort == "rank") {
        return companies.sort(function (a, b) {
          return a.rank - b.rank;
        });
      } else {
        return companies;
      }
    },
  },
};
</script>
<style lang="scss" scoped>
.content {
  width: calc(100% - 25%);
  .filter-sort {
    padding: 20px;
    display: flex;
    justify-content: space-evenly;
    label {
      font-size: 18px;
      margin-right: 5px;
    }
    input,
    select {
      padding: 10px 15px;
      margin: 4px 0;
      border: 1px solid #555;
      border-radius: 5px;
    }
  }
  .data-table {
    padding: 20px;
    table {
      width: 100%;
      border: 2px solid #42b983;
      border-radius: 3px;
      background-color: #fff;
      th {
        background-color: #42b983;
        color: rgba(255, 255, 255, 0.66);
        cursor: pointer;
      }
      td {
        background-color: #f9f9f9;
      }
      th,
      td {
        min-width: 120px;
        padding: 10px 20px;
      }
    }
  }
}
</style>
