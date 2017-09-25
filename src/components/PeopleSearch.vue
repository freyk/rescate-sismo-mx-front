<template>
        <div class="c-people-search">
           <h3 class="c-people-search__title">Buscar Persona</h3>

           <div class="c-people-search__form">
              <div class="c-people-search__inputs-container">
                 <div class="c-people-search__input-wrap">
                    <input type="text" class="c-people-search__input" placeholder="Nombres" v-model="teaser.name">
                 </div><!--
               --><div class="c-people-search__input-wrap">
                    <input type="text" class="c-people-search__input" placeholder="Apellido Paterno" v-model="teaser.firstName">
                 </div><!--
              --><div class="c-people-search__input-wrap">
                    <input type="text" class="c-people-search__input" placeholder="Apellido Materno" v-model="teaser.lastName">
                 </div>
              </div><!--

           --><div class="c-people-search__btn-container">
                 <button class="c-people-search__btn c-btn c-btn--secondary" v-on:click="doSearch()"><i class="fa fa-search" aria-hidden="true"></i> Buscar</button>
              </div>
           </div>
        </div>
</template>

<script>
  export default {
    /**
     * The name of the component.
     */
    name: 'people-search',

    /**
     * The custom props of the component.
     */
    props: {
      teaser: {
        type: Object,
        default() {
          return {
            name: null,
            firstName: null,
            lastName: null,
          };
        },
      },
    },

    methods: {

      doSearch() {
        this.$emit('do-search');
        this.setTerm();
      },

      setTerm() {
        const term = this.formatFullName([
          this.teaser.name,
          this.teaser.firstName,
          this.teaser.lastName,
        ]);

        this.$emit('get-term', term);
      },

      formatFullName(items) {
        let result = '';
        let newItems = [];

        if (typeof items !== 'object') {
          throw new Error('Expected items variable needs to be array');
        }

        newItems = items.filter((item) => {
          if (item === null || item === '') {
            return false;
          }

          return true;
        });

        newItems.forEach((item, index) => {
          result += ((index + 1) === newItems.length) ? `${item}` : `${item} `;
        });

        return result;
      },
    },

    mounted() {
      this.$nextTick(() => this.setTerm());
    },
  };
</script>
