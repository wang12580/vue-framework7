<template>
  <f7-page name="table">
    <f7-swiper pagination :params="{speed:500, slidesPerView: 1, spaceBetween: 20}">
      <f7-swiper-slide>Slide 1</f7-swiper-slide>
      <f7-swiper-slide>Slide 2</f7-swiper-slide>
      <f7-swiper-slide>Slide 3</f7-swiper-slide>
    </f7-swiper>
    <f7-grid>
      <f7-col width="50" tablet-width="25" class="col_table">
        <f7-link href="/about/">
          <f7-icon f7="add_round_fill" link="/cards/"></f7-icon>
        </f7-link>
      </f7-col>
      <f7-col width="50" tablet-width="25" class="col_table">
        <f7-icon f7="briefcase_fill"></f7-icon>
      </f7-col>
      <f7-col width="50" tablet-width="25" class="col_table">
        <f7-icon f7="bell_fill"></f7-icon>
      </f7-col>
      <f7-col width="50" tablet-width="25" class="col_table">
        <f7-icon f7="alarm"></f7-icon>
      </f7-col>
    </f7-grid>
    <f7-grid>
      <f7-col width="25" tablet-width="25" class="col_nav">
       <f7-link open-picker>
          1
          <f7-icon f7="chevron_down" size="15"></f7-icon>
        </f7-link>
      </f7-col>
      <f7-col width="25" tablet-width="25" class="col_nav">
        2<f7-icon f7="chevron_down" size="15" ></f7-icon>
      </f7-col>
      <f7-col width="25" tablet-width="25" class="col_nav">
        3<f7-icon f7="chevron_down" size="15" ></f7-icon>
      </f7-col>
      <f7-col width="25" tablet-width="25" class="col_nav">
        4<f7-icon f7="chevron_down" size="15" ></f7-icon>
      </f7-col>
    </f7-grid>
    <f7-picker-modal>
      <f7-toolbar>
        <div class="left"></div>
        <div class="right">
          <f7-link close-picker>Done</f7-link>
        </div>
      </f7-toolbar>
      <f7-block>
        Integer mollis nulla id nibh elementum finibus. Maecenas eget fermentum ipsum. Sed sagittis condimentum nisl at tempus. Duis lacus libero, laoreet vitae ligula a, aliquet eleifend sapien. Nullam sodales viverra sodales. Nulla hendrerit condimentum dolor facilisis tempor. Donec at est malesuada, sagittis nisi et, accumsan enim.
      </f7-block>
    </f7-picker-modal>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  mounted () {
  },
  methods: {
    adds: function () {
      console.log(this)
      // mainView.router.back('/about/')
      // this.$f7Router.routes('/about/')
      this.$f7.alert('Hello')
    }
  }
}
</script>

<style lang="less" scoped>
.swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
  background:#fff;
  font-size: 25px;
  height: 150px;
}
.col_table{
  display: flex;
  justify-content: center;
  align-items: center;
  background:#f0f;
  height: 100px;
  font-size: 25px;
}
.col_nav{
  display: flex;
  justify-content: center;
  align-items: center;
  background:#fff;
  height: 30px;
  font-size: 25px;
}
</style>
