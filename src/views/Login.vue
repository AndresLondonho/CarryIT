<template>
  <v-container id="signinup-form" class="fill-height">
    <v-row align="center" justify="center" no-gutters>
      <v-col cols="12" sm="8" md="8" class="">
        <v-card class="evelation-12 card">
          <v-window v-model="step">
            <!--Bloque inicio sesión-->
            <v-window-item :value="1">
              <v-row class="">
                <v-col cols="12" md="8" class="pt-6 pb-12">
                  <v-card-text>
                    <v-form class="signup-form-form">
                      <h1
                        class="text-center display-1 mb-10"
                        :class="`${bgColor}--text`"
                      >
                        Iniciar sesión
                      </h1>
                      <v-text-field
                        id="username"
                        label="Usuario"
                        name="Username"
                        append-icon="person"
                        type="text"
                        :color="bgColor"
                      />
                      <v-text-field
                        id="password"
                        label="Contraseña"
                        name="Password"
                        append-icon="lock"
                        type="password"
                        :color="bgColor"
                      />
                    </v-form>
                    <div class="text-center">
                      <a
                        href="#"
                        class="mt-3 overline no-text-decoration"
                        :class="`${bgColor}--text`"
                        @click="step = 3"
                      >
                        Olvidaste tu contraseña?
                      </a>
                    </div>
                  </v-card-text>
                  <div class="text-center mt-3">
                    <v-btn large :color="bgColor" dark>Iniciar</v-btn>
                  </div>
                </v-col>
                <v-col
                  cols="12"
                  md="4"
                  class="darken-2 vcenter"
                  :class="`${bgColor}`"
                >
                  <div>
                    <v-card-text :class="`${fgColor}--text`">
                      <h1 class="text-center headline mb-3">Aún no tienes un usuario?</h1>
                      <h5 class="text-center overline mb-3">
                        Por favor registrate para continuar
                      </h5>
                    </v-card-text>
                    <div class="text-center mb-6">
                      <v-btn dark outlined @click="step = 2">Registrarse</v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <!--Bloque registrarse-->
            <v-window-item :value="2">
              <v-row class="fill-height">
                <v-col
                  cols="12"
                  md="4"
                  class="darken-2 vcenter"
                  :class="`${bgColor}`"
                >
                  <div>
                    <v-card-text :class="`${fgColor}--text`">
                      <h1 class="text-center headline mb-3">Ya tienes un usuario?</h1>
                      <h5 class="text-center overline mb-3">Por favor inicia sesión</h5>
                    </v-card-text>
                    <div class="text-center mb-6">
                      <v-btn dark outlined @click="step = 1">Iniciar Sesión</v-btn>
                    </div>
                  </div>
                </v-col>
                <v-col cols="12" md="8" class=" pt-6 pb-12">
                  <v-card-text>
                    <h1
                      class="text-center display-1 mb-10"
                      :class="`${bgColor}--text`"
                    >
                      Registrate
                    </h1>
                    <v-form class="signup-form-form">
                      <v-text-field
                        id="username"
                        label="Usuario"
                        name="username"
                        append-icon="person"
                        type="text"
                      />
                      <v-text-field
                        id="email"
                        label="Correo electronico"
                        name="email"
                        append-icon="email"
                        type="email"
                      />
                      <v-text-field
                        id="password"
                        label="Contraseña"
                        name="password"
                        append-icon="lock"
                        type="password"
                      />
                    </v-form>
                  </v-card-text>
                  <div class="text-center">
                    <v-btn large :color="bgColor" dark>Registrarse</v-btn>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <!--Bloque restablecer contraseña-->
            <v-window-item :value="3">
              <v-row class="fill-height">
                <v-col
                  cols="12"
                  md="4"
                  class="darken-2 vcenter"
                  :class="`${bgColor}`"
                >
                  <div>
                    <v-card-text :class="`${fgColor}--text`">
                      <h1 class="text-center headline mb-3">Ya tienes un usuario?</h1>
                      <h5 class="text-center overline mb-3">Por favor inicia sesión</h5>
                    </v-card-text>
                    <div class="text-center mb-6">
                      <v-btn dark outlined @click="step = 1">Iniciar sesión</v-btn>
                    </div>
                  </div>
                </v-col>
                <v-col cols="12" md="8" class="pt-6 pb-12">
                  <v-card-text>
                    <v-form class="signup-form-form">
                      <h1
                        class="text-center display-1 mb-10"
                        :class="`${bgColor}--text`"
                      >
                        Restablecer la contraseña
                      </h1>
                      <v-text-field
                        id="username_email"
                        label="Usuario / Correo electronico"
                        name="Username_email"
                        append-icon="person / email"
                        type="text"
                        :color="bgColor"
                        class="v-input__icon--double"
                      />
                    </v-form>
                  </v-card-text>
                  <div class="text-center mt-3">
                    <v-btn large :color="bgColor" dark>Restablecer</v-btn>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Signupform',
  props: {
    source: {
      type: String,
      default: ''
    },
    bgColor: {
      type: String,
      default: 'red'
    },
    fgColor: {
      type: String,
      default: 'white'
    }
  },
  data: () => ({
    step: 1
  })
}
</script>

<style scoped lang="scss">
.v-input__icon--double .v-input__icon {
  margin-left: -4.25rem !important;
}
a.no-text-decoration {
  text-decoration: none;
}
#signinup-form {
  max-width: 75rem;
}
.signup-form-form {
  max-width: 23rem;
  margin: 0 auto;
}
.card {
  overflow: hidden;
}
.vcenter {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>