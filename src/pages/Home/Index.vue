<template>
  <v-layout>
     <div class="o-wrapper">

        <div class="c-call-action">
           <h2 class="c-call-action__title">Si conoces alguna persona de los afectados o tienes acceso a una lista apoya ingresandolos</h2>
           <router-link :to="{ name: 'people.add' }" tag="a" class="c-btn c-btn--primary">
              Ingresar persona
           </router-link>
        </div>

        <v-people-search></v-people-search>
     </div>
  </v-layout>
</template>

<script>
  /* ============
   * Home Index Page
   * ============
   *
   * The home index page.
   */

  import VLayout from '@/layouts/Default';
  import VPeopleSearch from '@/components/PeopleSearch';

  export default {
    /**
     * The name of the page.
     */
    name: 'home-index',

    /**
     * The components that the page can use.
     */
    components: {
      VLayout,
      VPeopleSearch,
    },
  };
</script>
