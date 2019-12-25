<template>
  <div>
    <v-toolbar style="margin-bottom:20px">
      <v-toolbar-title>Movie Blog</v-toolbar-title>

      <v-spacer />

      <v-toolbar-items v-if="$vuetify.breakpoint.smAndUp">
        <v-btn text>
          HOME
        </v-btn>
        <v-btn text>
          CLASSICS
        </v-btn>
        <v-btn text>
          STARS
        </v-btn>
        <v-btn text>
          GENRES
        </v-btn>
        <v-btn text>
          EDITORS PICK
        </v-btn>
      </v-toolbar-items>
      <template v-if="$vuetify.breakpoint.mdAndDown">
        <!-- <form id="demo-2">
          <input type="search" placeholder="Search">
        </form> -->
        <!-- <v-list-item>
          <v-list-item-content>
            <v-list-item-title>Single-line item</v-list-item-title>
          </v-list-item-content>
        </v-list-item> -->
        <!-- <v-btn icon>
          <v-icon>mdi-export-variant</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-delete-circle</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-plus-circle</v-icon>
        </v-btn> -->
      </template>
      <!-- <v-form v-model="valid">
        <v-text-field
          :counter="10"
          label="First name"
          required
        />
      </v-form> -->
      <form id="demo-2">
        <input v-model="searchBar" type="search" placeholder="Search">
      </form>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      searchBar: 'stuff',
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style>
  input {
    outline: none;
  }
  input[type=search] {
    -webkit-appearance: textfield;
    -webkit-box-sizing: content-box;
    box-sizing: content-box;
    font-family: inherit;
    font-size: 100%;
  }
  input::-webkit-search-decoration,
  input::-webkit-search-cancel-button {
    display: none;
  }
  input[type=search] {
    background: #ededed url(https://static.tumblr.com/ftv85bp/MIXmud4tx/search-icon.png) no-repeat 9px center;
    border: solid 1px #ccc;
    padding: 9px 10px 9px 32px;
    width: 55px;
    -webkit-border-radius: 10em;
    -moz-border-radius: 10em;
    border-radius: 10em;
    -webkit-transition: all .5s;
    -moz-transition: all .5s;
    transition: all .5s;
  }
  input[type=search]:focus {
    width: 130px;
    background-color: #fff;
    border-color: rgb(214, 79, 17);
    -webkit-box-shadow: 0 0 5px rgba(109,207,246,.5);
    -moz-box-shadow: 0 0 5px rgba(109,207,246,.5);
    box-shadow: 0 0 5px rgba(109,207,246,.5);
  }
  input:-moz-placeholder {
    color: #999;
  }
  input::-webkit-input-placeholder {
    color: #999;
  }
  #demo-2 input[type=search] {
    width: 15px;
    padding-left: 10px;
    color: transparent;
    cursor: pointer;
  }
  #demo-2 input[type=search]:hover {
    background-color: #fff;
  }
  #demo-2 input[type=search]:focus {
    width: 130px;
    padding-left: 32px;
    color: #000;
    background-color: #fff;
    cursor: auto;
  }
  #demo-2 input:-moz-placeholder {
    color: transparent;
  }
  #demo-2 input::-webkit-input-placeholder {
    color: transparent;
  }
</style>
