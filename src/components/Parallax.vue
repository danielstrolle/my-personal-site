<template>
  <section>
    <v-flex xs12 text-xs-center>
      <mq-layout mq="desktop">
        <v-parallax src="../../static/img/San-Antonio-Skyline.jpg">
        </v-parallax>
      </mq-layout>
      <mq-layout mq="mobile">
        <v-parallax src="../../static/img/San-Antonio-Skyline-Mobile.jpg" height="300">
        </v-parallax>
      </mq-layout>
      <img src="../../static/img/TestImg.jpg" alt="ProfilePic"
           style="border-radius: 50%; position: relative; top: -77px; margin-bottom: -77px; border: 2px solid white; box-shadow: inset 0 1.5px 3px 0 rgba(0,0,0,.15), 0 1.5px 3px 0 rgba(0,0,0,.15);">
    </v-flex>
  </section>
</template>
