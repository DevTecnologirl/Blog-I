<template>
  <!--pagina-->
  <q-page class="page_post-list flex justify-center">
    <!--componente da pagina -->
    <div class="bg-grey-5 page_post-list__list text-h4 q-py-lg">Blog</div>
    <div class="q-my-lg">
      <!--listas de posts-->
      <q-list class="q-gutter-y-md">
        <!--Listar os cards-->
        <div v-for="(post, index) in postList" :key="index">
          <q-card flat>
            <!-- CARDS-->
            <q-card-section horizontal>
              <div class="q-mr-md">
                <q-img :src="post.img" style="width: 150px"></q-img>
              </div>
              <!--CONTEUDO CARD-->
              <div class="column">
                <!--titulo, categoria e descrição-->
                <div class="text-bold text-h6 q-mb-sm">
                  {{ post.title }}
                </div>
                <div>
                  {{ post.category }}
                </div>
                <div>
                  {{ post.description }}
                </div>
              </div>
            </q-card-section>
            <q-separator color="black" class="q-mt-md"></q-separator>
          </q-card>
        </div>
      </q-list>
    </div>
  </q-page>
</template>

<script>
const postList = [
  {
    title: 'Lorem, ipsum dolor.',
    img: 'https://picsum.photos/300/300?random=1',
    description:
      'Lorem amet consectetur adipisicing elit. Aliquid, voluptatum. Ratione facere dolores corporis perspiciatis! Nihil',
    category: 'Dashboard',
  },
  {
    title: 'Lorem, ipsum dolor.',
    img: 'https://picsum.photos/300/300?random=2',
    description:
      'Lorem amet consectetur adipisicing elit. Aliquid, voluptatum. Ratione facere dolores corporis perspiciatis! Nihil',
    category: 'Dashboard',
  },
  {
    title: 'Lorem, ipsum dolor.',
    img: 'https://picsum.photos/300/300?random=3',
    description:
      'Lorem amet consectetur adipisicing elit. Aliquid, voluptatum. Ratione facere dolores corporis perspiciatis! Nihil',
    category: 'Dashboard',
  },
  {
    title: 'Lorem, ipsum dolor.',
    img: 'https://picsum.photos/300/300?random=4',
    description:
      'Lorem amet consectetur adipisicing elit. Aliquid, voluptatum. Ratione facere dolores corporis perspiciatis! Nihil',
    category: 'Dashboard',
  },
];

export default {
  data() {
    return { postList, name: 'PostList' };
  },
};
</script>

<style lang="scss">
.page_post-list {
  &__list {
    width: 80%;
  }
}
</style>
