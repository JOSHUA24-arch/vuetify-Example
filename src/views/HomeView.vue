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
                        <h1
                          class="
                            text-center
                            display-2
                            teal--text
                            text--accent-3
                          "
                        >
                          Sign to my company RABOtz
                        </h1>

                        <div class="text-center" mt-4>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <Icon
                              icon="akar-icons:facebook-fill"
                              style="font-size: 40px"
                            />
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <Icon
                              icon="ant-design:google-plus-circle-filled"
                              style="font-size: 40px"
                            />
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <Icon
                              icon="entypo-social:linkedin-with-circle"
                              style="font-size: 40px"
                            />
                          </v-btn>
                        </div>

                        <h4 class="text-center mlt-4">
                          Ensure your email for registration
                        </h4>

                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
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
                          />
                        </v-form>
                        <h3 class="text-center mt-3">Forget your Password ?</h3>
                      </v-card-text>
                      <div class="text-center mt-3 mb-2">
                        <v-btn rounded color="teal accent-3" dark
                          >SIGN IN</v-btn
                        >
                      </div>
                    </v-col>

                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Hello, Friends !</h1>
                        <h5 class="text-center">
                          Enter Your Personal details and start journey with us
                        </h5>
                      </v-card-text>

                      <div class="text-center">
                        <v-btn rounded outlined="" dark @click="step++"
                          >SIGN UP</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>

                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Welcome Back !</h1>
                        <h5 class="text-center">
                          To keep connected with us please login with your
                          credentials
                        </h5>
                      </v-card-text>

                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step--"
                          >SIGN IN</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="
                            text-center
                            display-2
                            teal--text
                            text--accent-3
                          "
                        >
                          Create Account
                        </h1>

                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                          <Icon
                              icon="akar-icons:facebook-fill"
                              style="font-size: 40px"
                            />
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <Icon
                              icon="ant-design:google-plus-circle-filled"
                              style="font-size: 40px"
                            />
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <Icon
                              icon="entypo-social:linkedin-with-circle"
                              style="font-size: 40px"
                            />
                          </v-btn>
                        </div>

                        <h4 class="text-center mt-4">Ensure your email for registration</h4>
                        <v-form>
                          <v-text-field 
                          label="Name"
                          name="Name"
                          prepend-icon="person"
                          type="text"
                          color="teal accent-3"
                          />

                          <v-text-field
                          label="Email"
                          name="Email"
                          prepend-icon="email"
                          type="text"
                          color="teal accent-3" 
                          />

                          <v-text-field 
                          label="Password"
                          name="Password"
                          prepend-icon="lock"
                          type="password"
                          color="teal accent-3" />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mb-2">
                      <v-btn rounded color="teal accent-3" dark>SIGN IN</v-btn></div>
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
import { Icon } from "@iconify/vue2";

export default {
  data: () => ({
    step: 1,
  }),

  components: {
    Icon,
  },
  props: {
    source: String,
  },
};
</script>