<template>
  <q-page class="flex flex-center bg-primary">
    <q-card class="my-card" style="width: 500px; ">
      <q-img src="../assets/login.png" width="100px flex flex-center" />

      <q-card-section>
        <div class="text-h5 flex flex-center">Faça seu Login</div>
        <div class="text-subtitle2 flex flex-center">App alpha</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <q-input standout v-model="login.email" type="email" prefix="Email:">
          <template v-slot:prepend>
            <q-icon name="mail" />
          </template>
        </q-input>
        <q-input
          label="Senha"
          class="q-mt-md"
          v-model="password"
          filled
          :type="login.isPwd ? 'password' : 'text'"
        >
          <template v-slot:append>
            <q-icon
              :name="login.isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="login.isPwd = !login.isPwd"
            />
          </template>
        </q-input>
      </q-card-section>
      <q-card-actions vertical align="center">
        <q-btn color="primary" label="Login"  @click="$router.push({name:'principal'})" style="height: 50px; width: 90%" />

        <q-btn
          flat
          color="primary"
          label="Esqueci minha senha"

          style="font-size: 17px; width: 90%"
          @click="$router.push({name:'esqueciSenha'})"
        />
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="absolute-bottom text-subtitle2 text-center">Title</div>
      </q-img>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: "PageLogin",
  data() {
    return {
      login: {
        email: "",
        senha: "",
        isPwd: true,
      },
    };
  },
};
</script>
