<template>
  <div class="app app-login p-0" cz-shortcut-listen="true">
    <div class="row g-0 app-auth-wrapper">
      <div class="col-12 col-md-7 col-lg-6 auth-main-col text-center p-5">
        <div class="d-flex flex-column align-content-end">
          <div class="app-auth-body mx-auto">
            <div class="app-auth-branding mb-4">
              <a class="app-logo" href="index.html"
                ><img
                  class="logo-icon mr-2"
                  src="@/assets/images/app-logo.svg"
                  alt="logo"
              /></a>
            </div>
            <h2 class="auth-heading text-center mb-5">Log in to Portal</h2>
            <div class="auth-form-container text-left">
              <form @submit.prevent="login()" class="auth-form login-form">
                <div class="email mb-3">
                  <label class="sr-only" for="email">Email</label>
                  <input
                    v-model="email"
                    id="email"
                    name="email"
                    type="email"
                    class="form-control email"
                    placeholder="Email address"
                    required="required"
                  />
                </div>
                <!--//form-group-->
                <div class="password mb-3">
                  <label class="sr-only" for="password">Password</label>
                  <input
                    v-model="password"
                    id="password"
                    name="password"
                    type="password"
                    class="form-control password"
                    placeholder="Password"
                    required="required"
                  />
                  <div class="extra mt-3 row justify-content-between">
                    <div class="col-6">
                      <div class="form-check">
                        <input
                          class="form-check-input"
                          type="checkbox"
                          value=""
                          id="RememberPassword"
                        />
                        <label class="form-check-label" for="RememberPassword">
                          Remember me
                        </label>
                      </div>
                    </div>
                    <!--//col-6-->
                    <div class="col-6">
                      <div class="forgot-password text-right">
                        <a href="reset-password.html">Forgot password?</a>
                      </div>
                    </div>
                    <!--//col-6-->
                  </div>
                  <!--//extra-->
                </div>
                <!--//form-group-->
                <div class="text-center">
                  <button
                    type="submit"
                    class="btn app-btn-primary btn-block theme-btn mx-auto"
                  >
                    Log In
                  </button>
                </div>
              </form>

              <div class="auth-option text-center pt-5">
                No Account? Sign up
                <router-link :to="{ path: 'register' }" class="text-link"
                  >here
                </router-link>
              </div>
            </div>
            <!--//auth-form-container-->
          </div>
          <!--//auth-body-->

          <footer class="app-auth-footer">
            <div class="container text-center py-3">
              <!--/* This template is free as long as you keep the footer attribution link. If you'd like to use the template without the attribution link, you can buy the commercial license via our website: themes.3rdwavemedia.com Thank you for your support. :) */-->
            </div>
          </footer>
          <!--//app-auth-footer-->
        </div>
        <!--//flex-column-->
      </div>
      <!--//auth-main-col-->
      <div class="col-12 col-md-5 col-lg-6 h-100 auth-background-col">
        <div class="auth-background-holder"></div>
        <div class="auth-background-mask"></div>
        <div class="auth-background-overlay p-3 p-lg-5">
          <div class="d-flex flex-column align-content-end h-100">
            <div class="h-100"></div>
            <div class="overlay-content p-3 p-lg-4 rounded">
              <h5 class="mb-3 overlay-title">Explore Portal Admin Template</h5>
            </div>
          </div>
        </div>
        <!--//auth-background-overlay-->
      </div>
      <!--//auth-background-col-->
    </div>
    <!--//row-->
  </div>
</template>

<script>
import AuthService from "@/services/AuthService.js";
export default {
  data() {
    return {
      email: null,
      password: null,
    }
  },
  methods: {
    login(){
      let data = {
        email: this.email,
        password: this.password
      }

      AuthService.login(data)
      .then(res =>{
        console.log(res)
        localStorage.setItem('TokenFIRE',res.data.token)
        localStorage.setItem('Usuario',res.data.Usuario.name)
        })
        .catch((errors) => {
          console.log(errors);
        })
    }
  }
}
</script>
