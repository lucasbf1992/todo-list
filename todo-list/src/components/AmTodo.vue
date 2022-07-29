<template>
  <div class="">
    <div class="col-lg-12 border rounded mt-1 p-5 topo">
      <b-button @click="modalShow = !modalShow">Cadastar</b-button>

      <b-modal v-model="modalShow" hide-footer>
        <template #modal-title>Cadastrar</template>
        <div class="">
          <div class="input-group">
            <div class="input-group">
              <input
                id="title"
                type="text"
                class="form-control"
                placeholder="Título"
                aria-label="Titulo"
                v-model="title"
                @keypress.enter="pressEnter"
              />
            </div>
            <div class="input-group mt-3">
              <textarea focus="true"
                class="form-control"
                placeholder="Descrição"
                rows="5"
                ref="description"
                v-model="description"
                @keypress.enter="pressEnter"
              ></textarea>
            </div>
          </div>
          <div class="mt-3">
            <div class="row">
              <button class="btn btn-primary" @click="store">Cadastar</button>
            </div>
            <div class="row mt-2">
              <button class="btn btn-danger" @click="clear">Limpar</button>
            </div>
          </div>
        </div>
      </b-modal>
      <div class="row"></div>
      <div class="row">
        <b-table
          ref="table"
          striped
          hover
          :items="items"
          :fields="fields"
        ></b-table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AMNavbar",
  props: {
    titleNavbar: String,
  },
  data() {
    return {
      fields: [
        {
          key: "title",
          label: "Título",
          sortable: true,
        },
        {
          key: "description",
          label: "Descrição",
          sortable: true,
        },
      ],
      items: [],
      title: "",
      description: "",
      modalShow: false,      
    };
  },
  methods: {
    store: function() {
      this.items.push({ title: this.title, description: this.description });

      this.handleShowModal();
    },
    clear: function() {
      this.title = "";
      this.description = "";
    },
    handleShowModal() {
      this.modalShow = !this.modalShow;
    },
    pressEnter: function(e) {
      if (e.target.id == 'title') {        
        this.$refs.description.focus()
        return;
      }      
      
      this.store();
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.topo {
  background-color: #fcfcfc;
}
</style>



