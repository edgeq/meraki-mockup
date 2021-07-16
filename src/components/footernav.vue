<template>
    <v-footer color="white"
      v-bind="localAttrs"
      :padless="padless"
    >
    <div class="footer-content">
      <div class="contact">
        <span class="contact-title">Contact</span>
        <span class="contact-phone">773-687-8107</span>
        <span class="contact-address">2028 W. Division Street</span>
        <span class="contact-city">Chicago, IL 60622</span>
        <span class="contact-email">hello@merakiroomchicago.com</span>
      </div>

      <div class="social">
        <v-icon x-large>mdi-facebook</v-icon>
        <v-icon x-large>mdi-instagram</v-icon>
      </div>

      <div class="hours">
        <span class="hours-title">Hours</span>
        <span class="hours-days">Monday -  Thursday</span>
        <span class="hours-times">11 PM - 8 PM</span>
        <span class="hours-days">Friday</span>
        <span class="hours-times">8 AM - 5 PM</span>
        <span class="hours-days">Saturday</span>
        <span class="hours-times">8 AM - 4 PM</span>

      </div>
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
.contact, .hours {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hours {
  align-items: flex-start;
}

</style>