<template>
  <v-container>
    <v-card elevation="2" outlined shaped>
      <v-card-title>
        <h1>Ejemplo Titulo</h1>
      </v-card-title>
      <v-card-text>
        <v-row>
          <v-col cols="6">
            <v-card elevation="2" outlined>
              <v-card-title>
                <h3>Como solicitar Informacion</h3>
                <br />
              </v-card-title>
              <v-divider class="mx-4"></v-divider>
              <v-card-text>
                <ol>
                  <li>Descargar el formulario</li>
                  <li>Llenarlo con todos los datos.</li>
                  <li>
                    <v-btn
                      @click="revealEmail = !revealEmail"
                      text
                      color="success"
                    >
                      Enviar Correo
                    </v-btn>
                    ó
                    <v-btn
                      @click="revealAddress = !revealAddress"
                      text
                      color="success"
                    >
                      Entregar Solicitud
                    </v-btn>
                  </li>
                  <!-- <li>
                    Enviar junto con la solicitud copia del Documento de
                    Identidad (DUI).
                  </li> -->
                </ol>
              </v-card-text>
              <v-expand-transition>
                <v-card
                  v-if="revealEmail"
                  class="transition-fast-in-fast-out v-card--reveal"
                  style="height: 100%; width: 95%"
                >
                  <v-card-text class="pb-0">
                    <p class="text-h5 text--primary">Correo Institucional</p>
                    <ul>
                      <li>transparenciainstitucional@fgr.gob.sv</li>
                    </ul>
                  </v-card-text>
                  <v-card-actions class="pt-10">
                    <v-btn text color="red" @click="revealEmail = false">
                      Cerrar
                    </v-btn>
                  </v-card-actions>
                </v-card>
                <v-card
                  v-if="revealAddress"
                  class="transition-fast-in-fast-out v-card--reveal"
                  style="height: 100%; width: 95%"
                >
                  <v-card-text class="pb-0">
                    <p class="text-h5 text--primary">Dirección</p>
                    <ul>
                      <li>
                        Entregar la solicitud personalmente en la siguiente
                        dirección: Boulevard Orden de Malta, Avenida El Boquerón
                        # 4-A, Edificio Zafiro, Santa Elena, Antiguo Cuscatlán,
                        La Libertad
                      </li>
                    </ul>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn text color="red" @click="revealAddress = false">
                      Cerrar
                    </v-btn>

                    <a
                      href="http://portaldetransparencia.fgr.gob.sv/documentos/Formulario-de-Solicitud-de-Informacion.pdf"
                      target="_blank"
                      class="v-btn v-btn--text"
                    >
                      Descargar PDF</a
                    >
                  </v-card-actions>
                </v-card>
              </v-expand-transition>
            </v-card>
          </v-col>
          <v-col cols="6">
            <v-card elevation="2" outlined>
              <v-card-title>
                <h3>Como solicitar Informacion</h3>
                <br />
              </v-card-title>
              <v-divider class="mx-4"></v-divider>
              <v-card-text>
                <ol>
                  <li>Descargar el formulario</li>
                  <li>Llenarlo con todos los datos.</li>
                  <li>
                    <v-btn
                      @click="revealEmail = !revealEmail"
                      text
                      color="success"
                    >
                      Enviar Correo
                    </v-btn>
                    ó
                    <v-btn
                      @click="revealAddress = !revealAddress"
                      text
                      color="success"
                    >
                      Entregar Solicitud
                    </v-btn>
                  </li>
                  <!-- <li>
                    Enviar junto con la solicitud copia del Documento de
                    Identidad (DUI).
                  </li> -->
                </ol>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "HomeView",

  data: () => ({
    revealEmail: false,
    revealAddress: false,
  }),
};
</script>

<style scoped>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>
