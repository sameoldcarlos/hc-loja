<template>
  <form class="form-inline">
    <input
      class="form-control mr-sm-0"
      type="search"
      placeholder="O que precisa?"
      aria-label="Search"
    />
    <button class="btn btn-outline-primary ml-md-auto" type="submit">
      <i class="fas fa-search"></i>
    </button>
  </form>
</template>

<script>
export default {};
</script>

<style scoped>
.btn-outline-primary, .form-control{
    border-style: none;
}
.form-control{
    width: 85%;
    padding-left: 10px;
}
.form-inline {
    border: solid 2px lightgrey;
    border-radius: 10px;
    width: 70%;
    margin: 30px;
    margin-top: 0;
    margin-bottom: 15px;
    background: #fff;
}
</style>