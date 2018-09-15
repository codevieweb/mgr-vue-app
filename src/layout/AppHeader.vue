<template>
    <header class="header-global">
        <base-nav class="navbar-main" transparent type="" effect="light" expand>
            <a slot="brand" class="navbar-brand mr-lg-5" href="https://demos.creative-tim.com/vue-argon-design-system/documentation">
                <img src="img/brand/logo.png">
            </a>

            <div class="row" slot="content-header" slot-scope="{closeMenu}">
                <div class="col-6 collapse-brand">
                    <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/">
                        <img src="img/brand/logo.png">
                    </a>
                </div>
                <div class="col-6 collapse-close">
                    <close-button @click="closeMenu"></close-button>
                </div>
            </div>

            <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
                <!-- <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-ui-04 d-lg-none"></i>
                        <span class="nav-link-inner--text">Components</span>
                    </a>
                    <div class="dropdown-menu-inner">
                        <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/"
                           class="media d-flex align-items-center">
                            <div class="icon icon-shape bg-gradient-primary rounded-circle text-white">
                                <i class="ni ni-spaceship"></i>
                            </div>
                            <div class="media-body ml-3">
                                <h6 class="heading text-primary mb-md-1">Getting started</h6>
                                <p class="description d-none d-md-inline-block mb-0">Get started with Bootstrap, the
                                    world's most popular framework for building responsive sites.</p>
                            </div>
                        </a>
                        <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/"
                           class="media d-flex align-items-center">
                            <div class="icon icon-shape bg-gradient-warning rounded-circle text-white">
                                <i class="ni ni-ui-04"></i>
                            </div>
                            <div class="media-body ml-3">
                                <h5 class="heading text-warning mb-md-1">Components</h5>
                                <p class="description d-none d-md-inline-block mb-0">Learn how to use Argon
                                    compiling Scss, change brand colors and more.</p>
                            </div>
                        </a>
                    </div>
                </base-dropdown> -->
                <!-- <base-dropdown tag="li" class="nav-item">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-collection d-lg-none"></i>
                        <span class="nav-link-inner--text">Examples</span>
                    </a>
                    <router-link to="/landing" class="dropdown-item">Landing</router-link>
                    <router-link to="/profile" class="dropdown-item">Profile</router-link>
                    <router-link to="/login" class="dropdown-item">Login</router-link>
                    <router-link to="/register" class="dropdown-item">Register</router-link>
                </base-dropdown> -->
            </ul>
            <ul class="navbar-nav align-items-lg-center ml-lg-auto">
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://www.facebook.com/creativetim" target="_blank"
                       data-toggle="tooltip" title="Like us on Facebook">
                        <i class="fa fa-facebook-square"></i>
                        <span class="nav-link-inner--text d-lg-none">Facebook</span>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://www.instagram.com/creativetimofficial"
                       target="_blank" data-toggle="tooltip" title="Follow us on Instagram">
                        <i class="fa fa-instagram"></i>
                        <span class="nav-link-inner--text d-lg-none">Instagram</span>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://twitter.com/creativetim" target="_blank"
                       data-toggle="tooltip" title="Follow us on Twitter">
                        <i class="fa fa-twitter-square"></i>
                        <span class="nav-link-inner--text d-lg-none">Twitter</span>
                    </a>
                </li>
                <!-- <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://github.com/creativetimofficial/vue-argon-design-system"
                       target="_blank" data-toggle="tooltip" title="Star us on Github">
                        <i class="fa fa-github"></i>
                        <span class="nav-link-inner--text d-lg-none">Github</span>
                    </a>
                </li> -->
                <li class="nav-item d-none d-lg-block ml-lg-4">
                    <a @click="modals.modal3 = true"
                       class="btn btn-neutral btn-icon">
                <span class="btn-inner--icon">
                  <i class="fa fa-sign-in mr-2"></i>
                </span>
                        <span class="nav-link-inner--text">Sign In</span>
                    </a>
                </li>
            </ul>
        </base-nav>
        <div class="col-md-4">
          <modal :show.sync="modals.modal3"
                 body-classes="p-0"
                 modal-classes="modal-dialog-centered modal-sm">
              <card type="secondary" shadow
                    header-classes="bg-white pb-5"
                    body-classes="px-lg-5 py-lg-5"
                    class="border-0">
                  <template>
                      <div class="text-muted text-center mb-3">
                          <small>Sign in with</small>
                      </div>
                      <div class="btn-wrapper text-center">
                          <base-button type="neutral">
                              <img slot="icon" src="img/icons/common/github.svg">
                              Github
                          </base-button>

                          <base-button type="neutral">
                              <img slot="icon" src="img/icons/common/google.svg">
                              Google
                          </base-button>
                      </div>
                  </template>
                  <template>
                      <div class="text-center text-muted mb-4">
                          <small>Or sign in with credentials</small>
                      </div>
                      <form role="form">
                          <base-input alternative
                                      class="mb-3"
                                      placeholder="Email"
                                      addon-left-icon="ni ni-email-83">
                          </base-input>
                          <base-input alternative
                                      type="password"
                                      placeholder="Password"
                                      addon-left-icon="ni ni-lock-circle-open">
                          </base-input>
                          <base-checkbox>
                              Remember me
                          </base-checkbox>
                          <div class="text-center">
                              <base-button type="primary" class="my-4">Sign In</base-button>
                          </div>
                      </form>
                  </template>
              </card>
          </modal>
        </div>
    </header>

</template>
<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";
import Modal from "@/components/Modal.vue";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown,
    Modal
  },
  data() {
    return {
      modals: {
        modal3: false
      }
    };
  }
};
</script>
<style>
</style>
