<template>
  <div class="card">
    <h2>{{ company.name }}</h2>

    <div class="card-content">
      <app-card-employee :employee="company.employee"></app-card-employee>

      <app-card-company :company="company"></app-card-company>
    </div>
  </div>
</template>

<script>
import CardEmployee from "./CardEmployee";
import CardCompany from "./CardCompany";

export default {
  name: "card",
  props: ["company"],
  components: {
    "app-card-employee": CardEmployee,
    "app-card-company": CardCompany
  }
};
</script>

<style scoped lang="scss">
$border: #dcdcdc;

.card {
  background-color: #ffffff;
  border: 1px solid $border;
  min-width: 500px;
  max-width: 500px;
  min-height: 270px;
  padding: 30px;
  display: flex;
  justify-content: flex-end;
  flex-wrap: wrap;
  margin: 15px 0;

  h2 {
    margin: 0;
    width: 100%;
  }
}
</style>
