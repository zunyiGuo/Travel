<template>
    <div>
      <div :class="$style.title">周末去哪儿</div>
      <ul>
        <li v-for="item of list" :key="item.id">
          <div :class="$style.item_img_warpper">
            <img :src="item.imgUrl" :class="$style.item_img">
          </div>
          <div :class="$style.item_info">
            <p :class="$style.item_title">{{item.title}}</p>
            <p :class="$style.item_dsc">{{item.dsc}}</p>
          </div>
        </li>
      </ul>
    </div>
</template>

<script>

export default {
  name: 'HomeWeekend',
  props: {
    list: {
      type: Array
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style module>

  .title {
    line-height: .8rem;
    background-color: #eee;
    text-indent: .2rem;
  }

.item_img_warpper {
    overflow: hidden;
    height: 0;
    padding-bottom: 37.09%;
  }

  .item_img {
    width: 100%;
  }

  .item_info {
    padding: .1rem;
  }

  .item_title {
    line-height: .54rem;
    font-size: .32rem;
  }

  .item_dsc {
    line-height: .4rem;
    color: #aaa;
    composes: u_text_overflow_ellipsis from 'styles/utilities.css';
  }

</style>
