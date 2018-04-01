<template>
   <svg :height="height" :width="width">
    <circle :cx="x(width)" :cy="y(height)" :r="calcR(width)" stroke="black" stroke-width="1" fill="#ddd" />
    <text x="50%" y="50%" text-anchor="middle" dy=".3em">{{text}}</text>
  </svg> 
</template>

<script>
export default {
  props: ['text', 'width', 'height'],

  data () {
    return {
      child_msg: 'Hello From the Child!',
      cx: 50,
      cy: 50,
      r: 40
    }
  },
  
  methods: {
    x(width) {
      return width/2;
    },

    y(height) {
      return height/2;
    },

    calcR(width) {
      return width/2 - 10;
    }
  }
}
</script>