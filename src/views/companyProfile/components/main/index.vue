<template>
  <div class="main">
    <div class="container">
      <div class="left">
        <h4 class="title">
          <router-link to="/guanyuwomen">
            关于我们
          </router-link>
        </h4>
        <ul>
          <li
            v-for="(item, index) in des"
            :key="index"
            :class="{ cur: isCur === index }"
          >
            <router-link :to="item.url">{{ item.title }}</router-link>
          </li>
        </ul>
        <RelatedInfo />
        <ContactUs />
      </div>
      <div class="right">
        <div class="header">
          <h5>
            <span>企业简介</span>
          </h5>
          <el-breadcrumb separator-class="el-icon-arrow-right">
            <el-breadcrumb-item>您的位置</el-breadcrumb-item>
            <el-breadcrumb-item :to="{ path: '/' }">主页</el-breadcrumb-item>
            <el-breadcrumb-item :to="{ path: '/guanyuwomen' }">
              关于我们
            </el-breadcrumb-item>
            <el-breadcrumb-item>企业简介</el-breadcrumb-item>
          </el-breadcrumb>
        </div>
        <div class="content">
          <img src="./img/company.jpg" alt="" />
          <div>
            <span class="text">
              &nbsp; &nbsp; &nbsp; &nbsp;
              三五九旅干部培训中心，隶属于三五九旅干部学院，在以“践行三五
              九旅精神、胡杨精神和兵团精神，传承红色基因，赓续红色血脉”为主
              题，深入推进党史专题教育培训课堂，充分发挥兵团解放新疆、建设新
              疆、屯垦戍边、维稳戍边丰富红色资源的独特优势的前提下，并合力与
              “全国党建联盟体”共同打造出暨韶山、井冈山、瑞金、古田、遵义、延
              安等全国红色教育、爱国主义教育基地线路，以专题教学、现场教学、体
              验教学、激情教学、案例式拓展教学、研讨式互动教学以及情感教学、场
              景教学等独特教学方式，让学员“扮演一名军垦战士、深入一处历史现
              场、参观一遍红色场馆、缅怀一次戍边先烈、尝试一回戍边壮举、学唱一
              首红色歌谣、体验一天屯垦生活、重走一趟生死征途、参与一堂红色课
              程”,使学员在历史现场中多维度地深刻体验先辈们在革命时期的历史壮
              举与革命精神，达到“真学、真懂、真信、真用”的培训效果。
            </span>
          </div>
        </div>
        <div class="clear"></div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" src="./style.scss" scoped></style>
<script src="./component.js"></script>
