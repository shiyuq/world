<template>
  <div class="innovation">
    <div class="title">
      <p>MOSHI</p>
      <h3>独创“五位一体”红色文化培训模式体系</h3>
    </div>
    <ul class="menu">
      <li
        v-for="(item, index) in mList"
        :key="index"
        :class="{ cur: iscur === index }"
        @mouseover="setIscur(index)"
        @mouseenter="setAutoplay()"
        @mouseleave="changeAutoplay()"
      >
        <img src="./img/pro_s.png" alt="" />
        {{ item.title }}
      </li>
    </ul>
    <div class="content">
      <el-carousel
        indicator-position="outside"
        ref="remarkCarusel"
        height="396px"
        @change="change"
        :autoplay="autoplay"
      >
        <el-carousel-item v-for="(item, index) in eList" :key="index">
          <div class="wen">
            <b>{{ item.number }}</b>
            <h4>{{ item.title }}</h4>
            <span>{{ item.english }}</span>
            <p>{{ item.content }}</p>
          </div>
          <img
            class="carousel"
            :src="item.imgUrl"
            :alt="item.alt"
            width="540"
            height="396"
          />
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<style lang="scss" src="./style.scss" scoped></style>

<script src="./component.js"></script>
