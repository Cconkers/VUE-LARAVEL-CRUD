<template>
  <div class="app app-signup p-0" cz-shortcut-listen="true">
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
            <h2 class="auth-heading text-center mb-4">Sign up to Portal</h2>

            <div class="auth-form-container text-left mx-auto">
              <form class="auth-form auth-signup-form">
                <div class="email mb-3">
                  <label class="sr-only" for="signup-email">Your Name</label>
                  <input
                    id="signup-name"
                    name="signup-name"
                    type="text"
                    class="form-control signup-name"
                    placeholder="Full name"
                    required="required"
                  />
                </div>
                <div class="email mb-3">
                  <label class="sr-only" for="signup-email">Your Email</label>
                  <input
                    id="signup-email"
                    name="signup-email"
                    type="email"
                    class="form-control signup-email"
                    placeholder="Email"
                    required="required"
                  />
                </div>
                <div class="password mb-3">
                  <label class="sr-only" for="signup-password">Password</label>
                  <input
                    id="signup-password"
                    name="signup-password"
                    type="password"
                    class="form-control signup-password"
                    placeholder="Create a password"
                    required="required"
                  />
                </div>
                <div class="extra mb-3">
                  <div class="form-check">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      value=""
                      id="RememberPassword"
                    />
                    <label class="form-check-label" for="RememberPassword">
                      I agree to Portal's
                      <a href="#" class="app-link">Terms of Service</a> and
                      <a href="#" class="app-link">Privacy Policy</a>.
                    </label>
                  </div>
                </div>
                <!--//extra-->

                <div class="text-center">
                  <button
                    type="submit"
                    class="btn app-btn-primary btn-block theme-btn mx-auto"
                  >
                    Sign Up
                  </button>
                </div>
              </form>
              <!--//auth-form-->

              <div class="auth-option text-center pt-5">
                Already have an account?
                <router-link :to='{path: "login"}' class="text-link">Log in
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
              <div>
                Portal is a free Bootstrap 5 admin dashboard template. You can
                download and view the template license
                <a
                  href="https://themes.3rdwavemedia.com/bootstrap-templates/admin-dashboard/portal-free-bootstrap-admin-dashboard-template-for-developers/"
                  >here</a
                >.
              </div>
            </div>
          </div>
        </div>
        <!--//auth-background-overlay-->
      </div>
      <!--//auth-background-col-->
    </div>
    <!--//row-->

    <iframe
      src="chrome-extension://kbbdabhdfibnancpjfhlkhafgdilcnji/./html/sources.html"
      allow="camera"
      style="display: none;"
    ></iframe
    ><iframe
      src="chrome-extension://kbbdabhdfibnancpjfhlkhafgdilcnji/./html/audiosources.html"
      allow="microphone"
      style="display: none;"
    ></iframe>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
