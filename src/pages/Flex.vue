<template>
  <q-page class="flex column">
    <h1>Flex Vue</h1>
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
