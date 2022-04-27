<template>
  <q-page class="flex flex-center bg-primary">
    <q-card class="my-card" style="width: 400px; height: auto">
      <q-img src="../assets/pass.png" style="width:100px flex-center"/>


      <q-card-section>
        <div class="text-h4 flex flex-center">Esqueci a senha</div>
        <div class="text-subtitle flex flex-center">Informe seu Email para redefinir sua senha</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <q-input standout v-model="email" type="email" prefix="Email:">
          <template v-slot:prepend>
            <q-icon name="mail" />
          </template>
        </q-input>
      </q-card-section>
      <q-card-actions vertical align="center">
        <q-btn outline color="primary" label="Redefinir Senha" @click="$router.push({name:'login'})" style="height: 50px; width: 90%" />
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
      email: ''
    };
  },
};
</script>
