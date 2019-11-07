<template>
  <div class="hello">

    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <div class="row">
            <div class="card" style="width: 15rem;">
              <img src="https://www.w3schools.com/bootstrap4/img_avatar3.png" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
            <div class="card" style="width: 15rem;">
              <img src="https://www.w3schools.com/bootstrap4/img_avatar3.png" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
            <div class="card" style="width: 15rem;">
              <img src="https://www.w3schools.com/bootstrap4/img_avatar3.png" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
          </div>
        </div>
        <div class="col-sm-3">
          <div class="card">
            <div class="card-header">Price Table</div>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">Item 1</li>
              <li class="list-group-item">Item 2</li>
              <li class="list-group-item">Item 3</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      
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
