<template>
  <q-page class="flex column">
    <h1>Flex Vue</h1>

    <div class="row q-mb-md">
      <div class="col bg-primary">1</div>
      <div class="col bg-secondary">2</div>
      <div class="col bg-accent">3</div>
    </div>

    <div class="row q-mb-md">
      <div class="col bg-primary">1</div>
      <div class="col col-6 bg-secondary">2</div>
      <div class="col bg-accent">3</div>
    </div>

    <div class="row q-mb-md justify-center">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>
    <q-separator spaced />
    <div class="row q-mb-md justify-between">
      <div class="col-12 col-md-6 bg-primary">1</div>
      <div class="col-12 col-md-6 bg-secondary">2</div>
    </div>

    <div class="row q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-around">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column q-mb-md items-center bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column q-mb-md items-end bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div
      class="column custom-hight q-mb-md items-center justify-center bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>
    <div
      class="column custom-hight q-mb-md items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>
    <div
      class="column custom-hight q-mb-md items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box self-start bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>
    <q-separator />
    <q-btn
      color="primary"
      :label="sideMenuOpen ? 'Cerrar menú lateral' : 'Abrir menú lateral'"
      class="q-mt-md"
      @click="toggleSideMenu"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import useUI from "../composables/useUI";

export default defineComponent({
  name: "FlexPage",
  setup() {
    const { sideMenuOpen, toggleSideMenu } = useUI();
    return {
      sideMenuOpen,
      toggleSideMenu,
    };
  },
});
</script>

<style scoped>
.col,
.col-4,
.col-6,
.col-12 {
  height: 50px;
  text-align: center;
}
.square-box {
  height: 50px;
  width: 50px;
}
.custom-hight {
  height: 300px;
}
</style>
