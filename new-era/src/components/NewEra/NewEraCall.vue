<template>
  <div>
    <b-container fluid>
      <b-row class="mt-3 ml-5 mr-5" align-h="center">
        <b-col cols="4"><hr class="layui-bg-red"></b-col>
        <b-col cols="4" class="text-center">
          <h3 class="wow animated fadeInUp" data-wow-duration="1s" data-wow-delay="0.5s">{{ $t('NewEraCall.name') }}</h3> 
        </b-col>
        <b-col cols="4"><hr class="layui-bg-red"></b-col>
      </b-row>
      <b-row>
        <b-col class="text-center ow animated heartBeat" data-wow-duration="2s" data-wow-delay="1s">
          <b-img :src="require('../NewEra/img/newera-call.png')" @click="call"></b-img>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="text-center">
          <small>{{ $t('NewEraCall.already') }} {{ countCall }} {{ $t('NewEraCall.call') }}</small>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import { WOW } from 'wowjs'
export default {
    data () {
      return {
        countCall: 2019621
      }
    },
    methods: {
      call: function () {
        this.countCall ++;
      }
    },
    mounted () {
      var wow = new WOW({
        boxClass: 'wow',
        animateClass: 'animated',
        offset: 30,
        mobile: true,
        live: false
      })
      wow.init()
    }
}
</script>
<style scoped>
 
</style>

