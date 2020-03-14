<template>
  <div>
    <h3>Our Cats</h3>
    <p>
      Here is our current list of cats.
    </p>

    <q-table :data="cats" :columns="columns" row-key="name">
    </q-table>
  </div>
</template>

<script>

// https://stackoverflow.com/a/1527820/52160
function getRandomInt(min, max) {
    min = Math.ceil(min);
    max = Math.floor(max);
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

export default {
  data() {
    return {
      cats: [
        {name:"Fluffy Pants", gender:"male", age: getRandomInt(0,10)},
        {name:"Cracker", gender:"male", age: getRandomInt(0,10)},
        {name:"Luna", gender:"female", age: getRandomInt(0,10)},
        {name:"Pig", gender:"female", age: getRandomInt(0,10)},
        {name:"Elise", gender:"female", age: getRandomInt(0,10)},
        {name:"Sammy", gender:"male", age: getRandomInt(0,10)},
        {name:"King Fred", gender:"male", age: getRandomInt(0,10)},
        {name:"Queenie", gender:"female", age: getRandomInt(0,10)},
        {name:"Serendipity", gender:"fmale", age: getRandomInt(0,10)},
        {name:"Lilith", gender:"female", age: getRandomInt(0,10)},
      ],
      columns:[
        { align: "left", headerStyle: "font-weight: bold", sortable: true, name: "name", field: "name", label: "Name" },
        { headerStyle: "font-weight: bold", sortable: true, name: "gender", field: "gender", label: "Gender" },
        { headerStyle: "font-weight: bold", sortable: true, name: "age", field: "age", label: "Age" }
      ]
    }
  }
}
</script>