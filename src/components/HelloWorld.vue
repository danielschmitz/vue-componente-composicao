<template>
  <div>
    <form-box title="Hello Form Box" message="A help message" v-on:save="onSave" @clear="onClear">
        <b-field label="Name">
            <b-input v-model="name"></b-input>
        </b-field>
        <b-field label="Email">
            <b-input v-model="email"></b-input>
        </b-field>
    </form-box>
  </div>
</template>

<script>
import FormBox from './FormBox.vue'

export default {
  name: 'HelloWorld',
  components: {
    FormBox
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      name: '',
      email: ''
    }
  },
  methods: {
    onSave: function () {
      console.log('Save', this.name, this.email)
    },
    onClear: function () {
      alert('clear')
    }
  }
}
</script>
