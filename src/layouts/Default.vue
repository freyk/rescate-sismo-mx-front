<template>
   <div>
      <div class="c-page-head">
         <div class="o-wrapper">
            <h1 class="c-page-head__logo">
               <router-link :to="{ name: 'home.index' }" tag="a">
                  Rescatando México
               </router-link>
            </h1>

            <ul class="c-main-nav">
               <router-link :to="{ name: 'people.add' }" tag="li">
                  <a href="">Ingresar persona</a>
               </router-link>

               <li class=""><a href="">Buscar persona</a></li>
            </ul>
         </div>
      </div>

      <div class="c-page-content">
         <!-- Content will be placed here -->
         <slot></slot>
      </div>

      <div class="c-page-foot">
         <p class="c-page-foot__copy">Hecho con amor para México</p>
      </div>
   </div>
</template>

<script>
  /* ============
   * Default Layout
   * ============
   *
   * Used for the home.
   *
   * Layouts are used to store a lot of shared code.
   * This way the app stays clean.
   */

  export default {
    /**
     * The name of the layout.
     */
    name: 'default-layout',

    /**
     * The data that can be used by the page.
     *
     * @returns {Object} The view-model data.
     */
    data() {
      return {

      };
    },

    /**
     * The methods that the layout can use.
     */
    methods: {

    },
  };
</script>
