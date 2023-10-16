<template>
  <v-app id="inspire">

    <v-app-bar
      class="px-3"
      flat
      density="compact"
    >
      <v-avatar
        color="grey-darken-1"
        class="hidden-md-and-up"
        size="32"
      ></v-avatar>

      <!--原创-->
      <v-btn class="hidden-md-and-up" @click="redirectToLogin">
        登录
      </v-btn>
      <p class="hidden-md-and-up">|</p>
      <v-btn class="hidden-md-and-up">
        注册
      </v-btn>

      <v-spacer></v-spacer>

      <v-tabs
        centered
        color="grey-darken-2"
      >
        <v-tab
          v-for="link in links"
          :key="link"
          :text="link"
        ></v-tab>
      </v-tabs>
      <v-spacer></v-spacer>

      <v-btn class="hidden-sm-and-down">
        登录
      </v-btn>
      <p class="hidden-sm-and-down">|</p>
      <v-btn class="hidden-sm-and-down">
        注册
      </v-btn>

      <v-avatar
        class="hidden-sm-and-down"
        color="grey-darken-1"
        size="32"
      ></v-avatar>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="2"
          >
            <v-sheet
              rounded="lg"
              min-height="268"
            >
              <!--  -->
            </v-sheet>
          </v-col>

          <v-col
            cols="12"
            md="8"
          >
            <v-sheet
              min-height="70vh"
              rounded="lg"
            >
              <!--  -->
            </v-sheet>
          </v-col>

          <v-col
            cols="12"
            md="2"
          >
            <v-sheet
              rounded="lg"
              min-height="268"
            >
              <!--  -->
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>

  </v-app>
</template>

<script setup>
import {ref} from "vue";

const links = [
  'Dashboard',
  'Messages',
  'Profile',
  'Updates',
]
// 定义一个ref用于绑定登录组件
let loginRef = ref(null)
let login = () => {
  loginRef.value.showLogin = true
}
</script>

<script>
export default {
  data: () => ({
    links: [
      'Dashboard',
      'Messages',
      'Profile',
      'Updates',
    ],
  }),
}
</script>
<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    };
    },
  methods: {
    login() {
    },
    // 处理登录逻辑
    // 可以在这里发送登录请求，验证用户名和密码等
      console.log('Login:', this.username, this.password);
    },
  redirectToLogin() {
    // 点击登录按钮后跳转到登录页面
  this.$router.push('/login'); } } };
</script>
<style>
.home { text-align: center; margin-top: 100px; }
</style>
