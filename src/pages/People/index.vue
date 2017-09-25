<template>
  <v-layout>
    <div class="o-wrapper">
      <v-people-search v-bind:teaser="teaser" v-on:do-search="doSearch()" v-on:get-term="setResultTerm($event)"></v-people-search>

      <div class="c-people-results">
        <h3 class="c-people-results__title">Resultados para la búsqueda "{{ searchTerm }}"</h3>

        <div class="c-people-results__content">
          <div v-for="person in persons" class="c-people-results__item">
            <h4 class="c-people-results__name">{{ person.fullName }}</h4>
            <span class="c-people-results__age">Edad {{ person.age }}</span>
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
import VPeopleSearch from '@/components/PeopleSearch';

export default {
  /**
  * The name of the page.
  */
  name: 'people-index',

  /**
  * The components the page can use.
  */
  components: {
    VLayout,
    VPeopleSearch,
  },

  /**
  * The data that can be used by the page.
  *
  * @returns {Object} The view-model data.
  */
  data() {
    return {
      searchTerm: '',
      teaser: {
        name: '',
        firstName: '',
        lastName: '',
      },
      persons: [
        {
          fullName: 'Marco Antonio Pedraza Acuña',
          status: 'Desaparecido',
          age: '28',
          CURP: 'PEAM881114HNLDCR09',
        },
        {
          fullName: 'Juan Jose Lopez Acuña',
          status: 'Desaparecido',
          age: '36',
        },
        {
          fullName: 'Sandra Melissa Pedraza Castillo',
          status: 'Desaparecido',
          age: '12',
        },
        {
          fullName: 'Jesus Alan Treviño Robledo',
          status: 'Desaparecido',
          age: '26',
        },
      ],
    };
  },

  /**
  * The methods the page can use.
  */
  methods: {

    doSearch() {
      // Do something
    },

    setResultTerm(value) {
      this.searchTerm = value;
    },
  },

  mounted() {
    this.teaser = this.$route.params.teaser;
  },
};
</script>