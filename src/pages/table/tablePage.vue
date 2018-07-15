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
        <div @click="tables2">
          2<f7-icon f7="chevron_down" size="15" ></f7-icon>
        </div>
      </f7-col>
      <f7-col width="25" tablet-width="25" class="col_nav">
        3<f7-icon f7="chevron_down" size="15" ></f7-icon>
      </f7-col>
      <f7-col width="25" tablet-width="25" class="col_nav">
        4<f7-icon f7="chevron_down" size="15" ></f7-icon>
      </f7-col>
    </f7-grid>
    <f7-grid v-show="this.table2">
      <f7-col width="100" tablet-width="100"  class="col_tble">
        <div @click= "table2_1_f('a')">最新
          <f7-icon f7="check" v-show="this.table2_1.a"></f7-icon>
        </div>
      </f7-col>
      <f7-col width="100" tablet-width="100"  class="col_tble">
        <div @click= "table2_1_f('b')">推荐
          <f7-icon f7="check" v-show="this.table2_1.b"></f7-icon>
        </div>
      </f7-col>
    </f7-grid>
    <f7-grid>
      <f7-toolbar>
        <f7-link @click="table3_1_f('a')">附近</f7-link>
        <f7-link @click="table3_1_f('b')">商圈</f7-link>
        <f7-link @click="table3_1_f('c')">地铁</f7-link>
      </f7-toolbar>
      <f7-list>
        <f7-list-item swipeout title="Item 1" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 2" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 1" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 2" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 1" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 2" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 1" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
        <f7-list-item swipeout title="Item 2" @swipeout:deleted="onSwipeoutDeleted">
          <f7-swipeout-actions>
            <f7-swipeout-button delete>Delete</f7-swipeout-button>
          </f7-swipeout-actions>
        </f7-list-item>
      </f7-list>
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
// import tablePage2 from './tablePage2.vue'
export default {
  // components: { tablePage2 },
  data () {
    return {
      table2: false,
      table2_1: {
        a: true,
        b: false,
      },
      table3_1: {
        a: true,
        b: false,
        c: false
      }
    }
  },
  mounted () {
  },
  methods: {
    tables2: function () {
      console.log('ssss')
      if (this.table2 === false) {
        this.table2 = true
      } else {
        this.table2 =false
      }
      console.log(this.table2)
    },
    adds: function () {
      console.log(this)
      // mainView.router.back('/about/')
      // this.$f7Router.routes('/about/')
      this.$f7.alert('Hello')
    },
    table2_1_f: function (a) {
      if (a === 'a') {
        this.table2_1.a = true
        this.table2_1.b = false
      } else {
        this.table2_1.b = true
        this.table2_1.a = false
      }
    },
    table3_1_f: function (a) {
      console.log(a)
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
.col_tble {
  background:#fff;
  height: 30px;
  font-size: 1rem;
}
.table3 {
  display: flex;
  justify-content: center;
  align-items: center;
  background:#fff;
  height: 100px;
  font-size: 1rem;
}
</style>
