<template>
  <div class="hello">
    <h1>Simple Test</h1>
    <p>This is a simple test Exercise</p>
    <h3>Follow the instructions</h3>
    <ul>
      <li>
        1. Add using reactive vue and state the number of stats that are in that
        request
      </li>
      <li>
        2. Create a simple table with the stats displaying only calories, and
        distance
      </li>
      <li>3. Add a simple filter for the stats that are with calories > 900</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Test Exercise",
  setup: () => {
    const retrieveStats = async () => {
      const response = await fetch("https://stats-tawny.vercel.app/api/stats");
      const data = await response.json();
      return data;
    };

    retrieveStats();

    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
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
