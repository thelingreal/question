<template>
  <v-app>
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="12" sm="8" md="4"> <v-card>
          <v-card-title class="text-center"> <h2>Login</h2>
          </v-card-title> <v-card-text> <v-form ref="form" @submit="login">
          <v-text-field v-model="username" label="Username" required ></v-text-field>
          <v-text-field v-model="password" label="Password" type="password" required >
          </v-text-field>
          <v-btn color="primary" block type="submit">
            Login
          </v-btn>
        </v-form>
        </v-card-text>
        </v-card> </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  data() {
    return { username: '', password: '' };
    },
  methods: {
    login() {
      // 处理登录逻辑
      // 可以在这里发送登录请求，验证用户名和密码等
      console.log('Login:', this.username, this.password);
    }
  }
};
</script>
<style> /* 可以在这里添加自定义样式 */
</style>
