<template>
        <div class="c-people-search">
           <h3 class="c-people-search__title">Buscar Persona</h3>

           <div class="c-people-search__form">
              <div class="c-people-search__inputs-container">
                 <div class="c-people-search__input-wrap">
                    <input type="text" name="" value="" class="c-people-search__input" placeholder="Nombres">
                 </div><!--
               --><div class="c-people-search__input-wrap">
                    <input type="text" name="" value="" class="c-people-search__input" placeholder="Apellido Paterno">
                 </div><!--
              --><div class="c-people-search__input-wrap">
                    <input type="text" name="" value="" class="c-people-search__input" placeholder="Apellido Materno">
                 </div>
              </div><!--

           --><div class="c-people-search__btn-container">
                 <button class="c-people-search__btn c-btn c-btn--secondary"><i class="fa fa-search" aria-hidden="true"></i> Buscar</button>
              </div>
           </div>
        </div>
</template>

<script>
  /* ============
   * Card Component
   * ============
   *
   * A basic card component.
   *
   * Gives an idea how components work.
   */

  import SlotMixin from '@/mixins/slot';

  export default {
    /**
     * The name of the component.
     */
    name: 'people-search',

    /**
     * The mixins that the component can use.
     */
    mixins: [
      SlotMixin,
    ],

    /**
     * The computed properties that the component can use.
     */
    computed: {

    },
  };
</script>
