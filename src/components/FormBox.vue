<template>
  <div>
      <b-message :title="title" :closable="false">
        <b-tag type="is-warning" v-show="message">{{message}}</b-tag>
        <slot></slot>
        <hr/>
        <button class="button is-primary is-pulled-right" @click="$emit('save')" >Save</button>
        <button class="button is-secondary " @click="onClearClick" >Clear</button>
      </b-message>
  </div>
</template>
<script>
export default {
  name: 'FormBox',
  props: ['title', 'message'],
  data () {
    return {

    }
  },
  methods: {
    onClearClick: function () {
      this.$emit('clear')
    }
  }
}
</script>
