<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-10">
        <!-- Card de busca -->
        <card-container-component>
          <template v-slot:header>
            <span>Pesquisar marca</span>
          </template>

          <template v-slot:content>
            <div class="form-group">
              <input-container-component
                title="ID"
                id="inputId"
                id-help="idHelp"
                text-help="Opcional - ID da marca"
              >
                <input
                  type="number"
                  class="form-control"
                  id="inputId"
                  aria-describedby="idHelp"
                  placeholder="ID da marca"
                />
              </input-container-component>
            </div>

            <div class="form-group">
              <input-container-component
                title="name"
                id="inputName"
                id-help="nameHelp"
                text-help="Opcional - Nome da marca"
              >
                <input
                  type="text"
                  class="form-control"
                  id="inputName"
                  aria-describedby="nameHelp"
                  placeholder="Nome da marca"
                />
              </input-container-component>
            </div>
          </template>

          <template v-slot:footer>
            <button type="submit" class="btn btn-primary float-right">
              Pesquisar
            </button>
          </template>
        </card-container-component>
      </div>

      <!-- Card de listagem -->
      <div class="col-md-10 mt-3">
        <card-container-component title="Marcas">
          <template v-slot:header>
            <span>Marcas</span>
            <button
              type="button"
              class="btn btn-primary float-right"
              data-toggle="modal"
              data-target="#createModalMarca"
            >
              Adicionar
            </button>
            <modal-component id="createModalMarca" title="Nova marca">
              <template v-slot:content>
                <div class="form-group">
                  <input-container-component
                    title="Nome da marca"
                    id="newMarcaName"
                  >
                    <input
                      type="text"
                      class="form-control"
                      id="newMarcaName"
                      placeholder="Nome da marca"
                    />
                  </input-container-component>
                </div>

                <div class="form-group">
                  <input-container-component
                    title="Imagem"
                    id="newImageMarca"
                  >
                    <input
                      type="file"
                      class="form-control-file"
                      id="newImageMarca"
                      placeholder="Selecionar uma imagem PNG"
                    />
                  </input-container-component>
                </div>

              </template>

              <template v-slot:footer>
                       <button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
                       <button type="button" class="btn btn-primary">Salvar</button>
              </template>
            </modal-component>
          </template>

          <template v-slot:content>
            <table-container-component></table-container-component>
          </template>

          <template v-slot:footer>
            <p>Paginação</p>
          </template>
        </card-container-component>
      </div>
    </div>
  </div>
</template>

<script>
</script>
