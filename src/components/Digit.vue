<template>
  <svg
class="digit" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
width="447px" height="834.1px" viewBox="0 0 447 834.1" enable-background="new 0 0 447 834.1" xml:space="preserve">
<path
:class="{ active: '02356789'.includes(data) }"
class="digit-a"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M409,16.5c0,9.113-7.388,16.5-16.5,16.5h-343
	C40.387,33,33,25.613,33,16.5l0,0C33,7.387,40.387,0,49.5,0h343C401.612,0,409,7.387,409,16.5L409,16.5z"/>
<path
:class="{ active: '2345689'.includes(data) }"
class="digit-b"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M409,417c0,9.113-7.388,16.5-16.5,16.5h-343
	c-9.113,0-16.5-7.387-16.5-16.5l0,0c0-9.113,7.387-16.5,16.5-16.5h343C401.612,400.5,409,407.887,409,417L409,417z"/>
<path
:class="{ active: '0268'.includes(data) }"
class="digit-c"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M16.5,801.5C7.387,801.5,0,794.112,0,785V442
	c0-9.113,7.387-16.5,16.5-16.5l0,0c9.113,0,16.5,7.387,16.5,16.5v343C33,794.112,25.613,801.5,16.5,801.5L16.5,801.5z"/>
<path
:class="{ active: '12347890'.includes(data) }"
class="digit-d"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M430.5,405c-9.113,0-16.5-7.388-16.5-16.5v-343
	c0-9.113,7.387-16.5,16.5-16.5l0,0c9.113,0,16.5,7.387,16.5,16.5v343C447,397.612,439.613,405,430.5,405L430.5,405z"/>
<path
:class="{ active: '134567890'.includes(data) }"
class="digit-e"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M430.5,801.5c-9.113,0-16.5-7.388-16.5-16.5V442
	c0-9.113,7.387-16.5,16.5-16.5l0,0c9.113,0,16.5,7.387,16.5,16.5v343C447,794.112,439.613,801.5,430.5,801.5L430.5,801.5z"/>
<path
:class="{ active: '456890'.includes(data) }"
class="digit-f"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M16.5,405C7.387,405,0,397.612,0,388.5v-343
	C0,36.387,7.387,29,16.5,29l0,0C25.613,29,33,36.387,33,45.5v343C33,397.612,25.613,405,16.5,405L16.5,405z"/>
<path
:class="{ active: '2356890'.includes(data) }"
class="digit-g"
fill="#E80006" stroke="#231815" stroke-miterlimit="10" d="M409,817.6c0,9.113-7.388,16.5-16.5,16.5h-343
	c-9.113,0-16.5-7.387-16.5-16.5l0,0c0-9.113,7.387-16.5,16.5-16.5h343C401.612,801.1,409,808.486,409,817.6L409,817.6z"/>
<circle :class="{ active: data === ':'}" fill="#E80006" stroke="#231815" stroke-miterlimit="10" cx="221" cy="217" r="36.5"/>
<circle :class="{ active: data === ':' }" fill="#E80006" stroke="#231815" stroke-miterlimit="10" cx="221" cy="613.5" r="36.5"/>
</svg>
</template>

<script setup>
defineProps({
  data: {
    type: String,
    default() {
      return ''
    },
  },
  color: {
    type: String,
    default() {
      return 'white'
    },
  },
})
</script>

<style scoped lang="sass">
.digit
  width: 100px
  height: 200px
  margin: 10px
path, circle
  fill: transparent
  &.active
    // v-bine 把 CSS 的值和 Vue 的變數綁定
    fill: v-bind(color)
</style>
