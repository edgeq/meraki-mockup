<template>
    <v-footer
      padless
    >
    <div class="footer-content pa-4">
      <div class="contact mx-1">
        <span class="contact-title">Contact</span>
        <span class="contact-phone">773-687-8107</span>
        <span class="contact-address">2028 W. Division Street</span>
        <span class="contact-city">Chicago, IL 60622</span>
        <span class="contact-email">Email Us</span>
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

    <div class="footer-social">
        <v-icon x-large>mdi-facebook</v-icon>
        <v-icon x-large>mdi-instagram</v-icon>
    </div>
    </v-footer>
</template>

<script>
export default {
    name: 'Footer',
    data(){
      return {}
    }
}
</script>

<style>
.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 100%;
}

.footer-social {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}
.contact, .hours {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.hours {
  align-items: flex-start;
}

.contact-title, .hours-title {
  font-weight: 600;
}

@media screen and (max-width: 600px) {
  .footer-content {}
}

</style>