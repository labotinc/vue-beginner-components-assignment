<template>
  <div class="card-employee">
    <span>{{ employee.position }}</span>
    <h1>{{ employee.englishName }}</h1>
    <span>{{ employee.japaneseName }}</span>
  </div>
</template>

<script>
export default {
  name: "card-employee",
  props: ["employee"]
};
</script>

<style scoped lang="scss">
$border: #dcdcdc;

.card-employee {
  margin-bottom: 30px;
  span {
    &:first-of-type {
      font-weight: bold;
    }

    &:last-of-type {
      opacity: 0.7;
    }
  }

  h1 {
    margin: 5px 0;
  }
}
</style>
