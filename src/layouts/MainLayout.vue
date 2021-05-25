<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">
        <q-btn
          flat
          round
          icon="eva-camera-outline"
          size="18px"
          dense
          to="/camera"
          class="large-screen-only"
        ></q-btn>
        <q-separator vertical spaced="10px"  class="large-screen-only"/>
        <q-toolbar-title class="text-grand-hotel text-bold"> FutureGram </q-toolbar-title>
        <q-btn
          flat
          round
          icon="eva-home"
          size="18px"
          dense
          to="/"
          class="large-screen-only"
        ></q-btn>
      </q-toolbar>
    </q-header>
    <q-footer class="bg-white small-screen-only" bordered>
      <q-tabs
        active-color="primary"
        class="text-grey-10"
        dense
        indicator-color="transparent"
      >
        <q-route-tab icon="eva-home" to="/" />
        <q-route-tab icon="eva-camera-outline" to="/camera" />
      </q-tabs>
    </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data() {
    return {}
  }
}
</script>

<style lang="sass">
.q-toolbar
  @media only screen and (min-width: $breakpoint-sm-min)
    height: 77px

.q-toolbar__title
  font-size: 34px
  @media only screen and (max-width: $breakpoint-xs-max)
    text-align: center

.q-footer
  .q-tab__icon
    font-size: 30px
</style>
