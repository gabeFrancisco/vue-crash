<template>
  <div class="app">
    Hello world! God bless you!
    <p>{{ jobs[3].title}}</p>
    <button>Change!</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { Job } from './types/Job';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    // const state = reactive({
    //   name: "Some data...",
    //   age: 25
    // })

    // return {
    //   ...toRefs(state)
    // }

    const jobs = ref<Job[]>([
      {
        title: "farm_worker", location: "some fancy ranch", salary: 3000, id: 1
      },
      {
        title: "electrician", location: "some fancy electrical facility", salary: 4000, id: 7
      },
      {
        title: "truck_driver", location: "some fancy truck", salary: 3500, id: 15
      },
      {
        title: "programmer", location: "some fancy place with a computer", salary: 5000, id: 3
      },
    ])

    return { jobs }
  },
});
</script>

<style>
.app {
  width: 100vw;
  text-align: center;
}
</style>
