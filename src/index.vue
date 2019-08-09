<template>
  <div id="container" style="height: 100%;width: 100%"></div>
</template>
<script>
  import { TMap } from './TMap'
  export default {
    data(){
      return {
      }
    },
    methods: {
      initMap(){
        //腾讯地图申请的key
        TMap('GENBZ-G5S3J-7OLFW-FLBX4-WVEMK-SOBL4').then(qq => {
          var map = new qq.maps.Map(document.getElementById("container"), {
            center: new qq.maps.LatLng(39.916527, 116.397128),// 地图的中心地理坐标。
            zoom: 8 //设置地图的缩放级别
                //设置地图样式详情参见MapType
          });
        });
      },
    },
    activated() {
      this.initMap();
    },
  }
</script>