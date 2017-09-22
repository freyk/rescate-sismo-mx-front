<template>
   <v-layout>
      <div class="o-wrapper">
         <div class="o-layout u-margin-top">
            <div class="o-layout__item u-1/3@desktop">
               <div class="c-teaser-form">
                  <h3>Ingresar Persona</h3>

                  <div class="c-teaser-form__input-wrap">
                     <label class="c-teaser-form__label" for="nombres">Nombres</label>
                     <input type="text" name="" value="" id="nombres">
                  </div>

                  <div class="c-teaser-form__input-wrap">
                     <label class="c-teaser-form__label" for="apellido-paterno">Apellido Paterno</label>
                     <input type="text" name="" value="" id="apellido-paterno">
                  </div>

                  <div class="c-teaser-form__input-wrap">
                     <label class="c-teaser-form__label" for="apellido-materno">Apellido Materno</label>
                     <input type="text" name="" value="" id="apellido-materno">
                  </div>

                  <div class="c-teaser-form__input-wrap">
                     <input type="submit" value="Guardar" class="c-btn c-btn--secondary">
                  </div>
               </div>
            </div>
         </div>
      </div>
   </v-layout>
</template>

<script>
/* ============
 * Add new person page
 * ============
 *
 * Page where the user can add new people.
 */

import VLayout from '@/layouts/Default';

export default {
  /**
   * The name of the page.
   */
  name: 'people-add',

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
   * The methods the page can use.
   */
  methods: {

  },

  /**
   * The components the page can use.
   */
  components: {
    VLayout,
  },
};
</script>