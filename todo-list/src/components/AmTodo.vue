<template>
  <div class="">
    <div class="col-lg-12 rounded mt-1 p-5 topo">
      <div class="row">
       <div class="col-lg-10">
          <div class="input-group">    
            <div class="input-group">
                  <input type="text" class="form-control" placeholder="Título" aria-label="Titulo">
              </div>
              <div class="input-group mt-3">
                <textarea class="form-control" placeholder="Descrição" rows="5"></textarea>
              </div>      
          </div>
        </div>

        <div class="col-lg-2 mt-3">
          <div class="row">    
            <button class="btn btn-primary">Cadastar</button>   
          </div>
          <div class="row mt-2">    
            <button class="btn btn-danger">Limpar</button>   
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AMNavbar',
  props: {
    titleNavbar: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.topo {
  background-color: #a1a1a1;
}
a {
  color: #42b983;
}
</style>



