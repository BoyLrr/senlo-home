<template>
  <div class="common-layout">
    <el-container>
      <el-header height="100px" style="width: 100%" >
        <el-row>
          <el-col :span="20">
            <el-image style="margin-left:200px;margin-top:20px;width: 100px; height: 40px"
                      :src="require('./assets/logo_senlo.png')" :fit="scale-down"/>
          </el-col>
          <el-col :span="4">
            <el-image style="margin-left:200px;margin-top:20px;width: 35px; height: 35px"
                      :src="require('./assets/github_logo.png')" :fit="scale-down"
                      @click="toAddress('https://github.com/BoyLrr')"
            />
          </el-col>
        </el-row>
        <el-divider/>
      </el-header>
      <el-main >
        <div style="width: 1000px;margin: 0 auto;display: flex; justify-content: center; flex-direction: column; align-items: center">
          <el-image style="width: 300px;height: 300px" :src="require('./assets/logo-blue.png')" fit="scale-down"/>
          <div>
            <h1>蜃楼-多功能学习平台</h1>
          </div>
          <div><h3 style="color: gray">各式各样的功能网站，让一切的困难都成为海市蜃楼</h3></div>
          <el-divider/>

        </div>
        <div style="width: 1000px;margin: 0 auto;display: flex;justify-content: space-around;">
          <el-card class="box-card" @click="toAddress('http://user.senlou.top')">
            <template #header>
              <div class="card-header">
                <span style="font-weight: bold">Senlo-API开放平台</span>
              </div>
            </template>
            <el-image style="width: 200px;height: 200px" :src="require('./assets/logo-blue.png')" fit="scale-down"/>
          </el-card>
          <el-card class="box-card" @click="toAddress('https://www.baidu.com')">
            <template #header>
              <div class="card-header">
                <span style="font-weight: bold">Senlo-OJ判题系统</span>
              </div>
            </template>
            <el-image style="width: 200px;height: 200px" :src="require('./assets/logo-blue.png')" fit="scale-down"/>
          </el-card>
          <el-card class="box-card">
            <template #header>
              <div class="card-header" @click="toAddress('https://www.baidu.com')">
                <span style="font-weight: bold">Senlo-BI智能</span>
              </div>
            </template>
            <el-image style="width: 200px;height: 200px" :src="require('./assets/logo-blue.png')" fit="scale-down"/>
          </el-card>
        </div>

      </el-main>
      <div style="height: 300px;width: 100%"></div>
      <el-footer height="200px" style="background-color: #d9d9d9" class="footer">
        <div>该网站只做学习使用，如有侵权请联系：17623267424@163.com</div>
        <div>膜拜鱼皮大佬，欢迎加入
          <el-link type="primary" href="https://yupi.icu" target="_blank" >编程导航知识星球</el-link>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>
<script  setup>
const toAddress = (url)=>{
  window.open(url);
}

</script>
<style>
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.footer{
  display: flex;
  flex-direction: column;
  justify-content: center; /* 水平居中 */
  align-items: center; /* 垂直居中 */
}
.footer > div {
  margin-top: 20px; /* 为了让div距离footer底部有一定间距，可以根据需要调整具体数值 */
}
</style>
