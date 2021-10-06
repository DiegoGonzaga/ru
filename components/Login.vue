<template>
  <div class="container alert alert-primary">
    <b-form @submit.prevent="userLogin">
      <b-form-group label-for="txt_login" label="Login">
        <b-form-input
          id="txt_login"
          type="email"
          placeholder="Enter your e-mail"
          v-model="email"
          required
        />
      </b-form-group>

      <b-form-group label-for="txt_pass" label="Password">
        <b-form-input
          id="txt_pass"
          type="password"
          placeholder="Enter your password"
          v-model="password"
          required
        />
      </b-form-group>
      <b-button type="submit" variant="btn btn-info btn-block">Login</b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  data() {
    return { email: "", password: "" };
  },
  methods: {
    async userLogin(event) {
      try {
        console.log(this.email);
        console.log(this.password);
        let response = await this.$auth.loginWith("local", {
          data: {
            email: this.email,
            password: this.password,
          },
        });
        console.log(response);
      } catch (err) {
        console.log("oi");
        console.log(err);
      }
    },
  },
};
</script>
