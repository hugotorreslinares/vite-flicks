<template>
  <div class="resume">
    <h2>Resume</h2>
    <div v-for="work in history" :key="work.company" class="item">
      <img class="logo" src="https://placehold.jp/40x40.png" alt="logo" />
      <span class="date"> {{ work.date }} </span>
      <span class="description">{{ work.description }}</span>
    </div>
  </div>
</template>

<script>
import History from "../config/history.json";
export default {
  name: "Resume",
  components: {},
  created() {
    this.history = History;
  },
  data: () => ({
    history: [],
    messageWhenNoItems: "There are not items",
    timelineItems: [
      {
          title: "Zemoga - Monks",
          date: "february 2021 - currently",
          description: "Lead Frontend Developer",
        },
        {
          title: "Globant",
          date: "April 2018 - February 2021",
          description: "Web UI Semi Sr Advanced",
        },
        {
          title: "Quadi",
          date: "October 2016 - April 2018",
          description: "Definitio Architect/ Technical Leader",
        },
        {
          title: "SANCHO BBDO",
          date: "March 2015 - October 2016",
          description: "Inbound Technologist",
        },
        {
          title: "INP LTDA",
          date: "October 2012 - February 2015",
          description: "Development Engineer",
        },
    ],
  }),
};
</script>
<style lang="scss" scoped>
.resume {
  min-height: 40vh;
  background: #a7a7a7;
  .item {
    background: white;
    padding: 10px;
    display: flex;
    margin: 5px;
    .company {
      font-weight: bold;
      display: block;
      padding: 10px;
    }
    .date {
      color: slategrey;
      font-size: 8px;
    }
    .description {
      font-size: 12px;
    }
  }
}
</style>
