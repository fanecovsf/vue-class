<template>
  <div>
    <HeaderVue :headerList="headerList"/>
    <FormVue/>
    <FirstComponent/>
    <LifeCycle/>
    <Person/>
    <PictureVue/>
  </div>
</template>

<script>
  import FirstComponent from './components/FirstComponent.vue'
  import FormVue from './components/form/Form.vue'
  import HeaderVue from './components/Header.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Person from './components/Person.vue'
  import PictureVue from './components/Picture.vue'

  export default {
    name: 'App',
    components: {
      FirstComponent,
      LifeCycle,
      Person,
      FormVue,
      PictureVue,
      HeaderVue
    },

    data() {
      return {
        headerList: [
          'Home',
          'Projetos',
          'Contato',
          'Instagram'
        ]
      }
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff
  }

  a {
    color: red
  }
</style>
