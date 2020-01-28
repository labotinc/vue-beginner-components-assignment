<template>
  <footer class="card-company">
    <span>{{ company.fullName }}</span>
    <span>{{ company.zipCode }}</span>
    <span>{{ company.address }}</span>
    <span>{{ company.addressExtended }}</span>
    <span>
      MAIL
      <span>{{ company.employee.email }}</span>
    </span>
  </footer>
</template>

<script>
export default {
  name: "card",
  props: ["company"]
};
</script>

<style scoped lang="scss">
.card-company {
  font-weight: 500;
  display: flex;
  flex-direction: column;

  span {
    font-size: 14px;
    &:first-of-type {
      font-size: 15px;
    }

    &:nth-of-type(2) {
      font-size: 12px;
    }

    & > span {
      font-weight: bold;
    }
  }
}
</style>
