<template>
  <q-layout
    view="lHh Lpr lFf"
    container
    style="height: 1000px"
    class="shadow-2 rounded-borders"
  >
    <q-page-container>
      <q-page padding>
        <!-- <q-menu transition-show="fade" transition-hide="scale" /> -->
        <div class="q-pa-md q-gutter-md">
          <div class="row justify-between">
            <q-img
              src="https://images.pexels.com/photos/5052875/pexels-photo-5052875.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
            >
              <div class="absolute-bottom text-subtitle1 text-center">
                Caption
              </div>
            </q-img>
            <q-img
              src="https://img.freepik.com/fotos-gratis/tijolos-de-brinquedo-na-mesa-com-blog-de-palavras_144627-47465.jpg?t=st=1714679011~exp=1714682611~hmac=d1028ab7f434374e9e34caab8f5213a44e36401ca6034bfcd5a0603e865ab4a0&w=826"
            >
              <div class="absolute-bottom text-subtitle1 text-center">
                Caption
              </div>
            </q-img>
          </div>
        </div>

        <!-- SCROOLER OF PAGE -->
        <q-page-scroller
          position="bottom-right"
          :scroll-offset="150"
          :offset="[18, 18]"
        >
          <q-btn fab icon="keyboard_arrow_up" color="accent" />
        </q-page-scroller>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<!-- <template>
  PAGINA INICIAL DO BLOG
  <q-page class="row items-center justify-evenly">
    <q-btn color="pink" icon="public" flat rounded outline> Meu botão </q-btn>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  components: {},
  setup() {
    return {};
  },
});
</script> -->
