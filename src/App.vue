<script>
  import { ref } from 'vue'

  export default {
    // data() {
    //   return {
    //     color: 'red',
    //     font: {
    //       size: '2em',
    //     },
    //   }
    // },
    // 👇 how to use style-variables with setup render function?
    setup() {
      // eslint-disable-next-line
      const color = ref('red')
      // eslint-disable-next-line
      const font = ref({ size: '2em' })

      return () => <div class="text">hello</div>
    },
  }
</script>

<style>
  body {
    background: #000;
    text-align: center;
  }

  .text {
    color: v-bind(color);

    /* expressions (wrap in quotes) */
    font-size: v-bind('font.size');
  }
</style>
