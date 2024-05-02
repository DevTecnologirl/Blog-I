<template>
  <q-layout
    view="hHh Lpr lFf"
    container
    class="shadow-2 rounded-borders fullscreen"
  >
    <q-header elevated class="bg-purple">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="drawer = !drawer"
        />
        <q-space />
        <!--sing in com tabs-->
        <q-tabs v-model="tab" shrink stretch>
          <q-tab name="sing" label="Sing-In " />
        </q-tabs>
        <q-btn flat round dense icon="search" aria-label="Pesquisa" />
        <q-btn flat round dense icon="group_add" aria-label="Grupo" />
      </q-toolbar>
      <q-toolbar inset>
        <q-toolbar-title> BLOG COM QUASAR </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="drawer" show-if-above :width="50" :breakpoint="500">
      <q-scroll-area class="fit">
        <q-list padding class="menu-list">
          <!-- -----------conteudo da lista------------------------------>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon color="purple" name="person" />
              <q-tooltip> Pessoa </q-tooltip>
            </q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon color="purple" name="edit"
            /></q-item-section>
            <q-tooltip> Criar Blog </q-tooltip>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon color="purple" name="star" />
              <q-tooltip>Favoritos</q-tooltip>
            </q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon color="purple" name="send"
            /></q-item-section>
            <q-tooltip> Blogs Enviados </q-tooltip>
          </q-item>

          <!-- ----------------------------------------->
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view> </router-view>
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    return {
      drawer: ref(false),
    };
  },
};
</script>

<style lang="sass" scoped>
.menu-list .q-item
  border-radius: 0 32px 32px 0
</style>
