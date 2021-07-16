<template>
    <v-footer color="white"
      v-bind="localAttrs"
      :padless="padless"
    >
    <div class="footer-content">
      <div class="contact">Contact</div>

      <div class="social">Social</div>

      <div class="hours">Hours</div>
    </div>
    </v-footer>
</template>

<script>
export default {
    name: 'footernav',
    data: () => ({
    icons: [
        'mdi-home',
        'mdi-email',
        'mdi-calendar',
        'mdi-delete',
      ],
      items: [
        'default',
        'absolute',
        'fixed',
      ],
      padless: false,
      variant: 'default',
  }),
  computed: {
      localAttrs() {
        const attrs = {}

        if (this.variant === 'default') {
          attrs.absolute = false
          attrs.fixed = false
        } else {
          attrs[this.variant] = true
        }
        return attrs
      },
    },
}
</script>

<style>
.footer-content {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

</style>