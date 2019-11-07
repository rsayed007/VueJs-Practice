<template>
    <nav class="navbar navbar-dark bg-dark navbar-expand-lg ">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
        </ul>
        <form @submit="searchItem" class="form-inline my-2 my-lg-0">
          <input  class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search" 
          v-model="keyword">
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
        </form>
      </div>
    </nav>
</template>

<script>
export default {
  data(){
    return{
      keyword: ''
    }
  },
  methods: {
    searchItem () {
      this.$emit('search', this.keyword)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container{
    padding-top: 20px;
  }
</style>
