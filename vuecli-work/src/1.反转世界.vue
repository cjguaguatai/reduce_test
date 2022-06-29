<template>
  <div>
    <h1>{{msg}}</h1>
    <button @click="reverse">点我反转</button>
  </div>
</template>

<script>
export default {
    data() {
        return {
            msg:'hello vue!'
        }
    },
    methods: {
        reverse() {
            this.msg = this.msg.split('').reverse().join('')
        }
    },
}
</script>

<style>

</style>