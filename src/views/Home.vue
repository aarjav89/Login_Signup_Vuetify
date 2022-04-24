<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
          <v-row align="center" justify="center">
            <v-col cols="12" sm="8" md="8">
              <v-card class="elevation-12">
                  <v-window v-model="step">
                    <v-window-item :value="1">
                      <v-row>
                        <v-col cols="12" md="8">
                          <v-card-text class="mt-12">
                            <h1 class="text-center display-2 teal--text text-accent-3">Sign-in to CRM</h1>
                          <div class="text-center mt-4">
                            <v-btn class="mx-2" fab color='teal accent-3' outlined>
                              <v-icon>fab fa-facebook-f</v-icon>
                            </v-btn>
                            <v-btn class="mx-2" fab color='teal accent-3' outlined>
                              <v-icon>fab fa-google-plus-g</v-icon>
                            </v-btn>
                            <v-btn class="mx-2" fab color='teal accent-3' outlined>
                              <v-icon>fab fa-linkedin-in</v-icon>
                            </v-btn>
                          </div>
                            <h4 class="text-center mt-4">Ensure your email for registration</h4>
                            <v-form>
                              <v-text-field
                                  label="Email"
                                  name="email"
                                  prepend-icon="email"
                                  type="text"
                                  color="teal accent-3"
                              />
                              <v-text-field
                              id="password"
                              label="Password"
                              name="password"
                              prepend-icon="lock"
                              type="password"
                              color="teal accent-3" />

                            </v-form>
                            <h3 class="text-center mt-3">Forgot Password ?</h3>
                          </v-card-text>
                          <div class="text-center mb-3">
                            <v-btn rounded color="teal accent-3" dark>Sign In</v-btn>
                          </div>
                        </v-col>


                        <v-col cols="12" md="4" class="teal accent-3">
                            <v-card-text class="white--text mt-12">
                              <h1 class="text-center display-1">Don't have an account with us ? No problem !</h1>
                              <h5 class="text-center">Enter your personal credentials and start accesing your leads with us !</h5>
                            </v-card-text>
                          <div class="text-center mb-2">
                            <v-btn rounded outlined dark @click="step++">Sign Up</v-btn>
                          </div>
                        </v-col>
                      </v-row>
                    </v-window-item>

                    <v-window-item :value="2">
                        <v-row class="fill-height">
                          <v-col cols="12" md="4" class="teal accent-3">
                            <v-card-text class="white--text mt-12">
                              <h1 class="text-center display-1">Lets get you registered !</h1>
                              <h5 class="text-center">To stay connected with us please login with your personal info ! If you already have an account with us, simply sign-in below !</h5>
                            </v-card-text>

                            <div class="text-center mb-3">
                              <v-btn rounded outlined dark @click="step--">Sign In</v-btn>
                            </div>
                          </v-col>
                          <v-col cols="12" md="8">
                            <v-card-text class="mt-12">
                              <h1 class="text-center display-2 teal--text text--accent-3"> Create Account</h1>
                              <div class="text-center mt-4">
                                <v-btn class="mx-2" fab color="teal accent-3" outlined>
                                  <v-icon>fab fa-facebook-f</v-icon>
                                </v-btn>
                                <v-btn class="mx-2" fab color="teal accent-3" outlined>
                                  <v-icon>fab fa-google-plus-g</v-icon>
                                </v-btn>
                                <v-btn class="mx-2" fab color="teal accent-3" outlined>
                                  <v-icon>fab fa-linkedin-in</v-icon>
                                </v-btn>
                              </div>
                              <h4 class="text-center mt-4">Ensure your email for registration</h4>
                              <v-form>
                                <v-text-field
                                name="Name"
                                label="Name"
                                type="text"
                                prepend-icon="person"
                                color="teal accent-3" />

                                <v-text-field
                                    name="Email"
                                    label="Email"
                                    type="text"
                                    prepend-icon="email"
                                    color="teal accent-3" />

                                <v-text-field
                                    name="Password"
                                    label="Password"
                                    type="password"
                                    prepend-icon="lock"
                                    color="teal accent-3" />


                              </v-form>
                            </v-card-text>
                            <div class="text-center mb-5">
                              <v-btn rounded color="teal accent-3" dark>
                                Register
                              </v-btn>
                            </div>
                          </v-col>
                        </v-row>
                    </v-window-item>

                  </v-window>

              </v-card>
            </v-col>
          </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  data:() => ({
    step:1
  }),
  props:{
    source: String
  },
  components: {

  }
}
</script>
