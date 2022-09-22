<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <q-layout class="bg-blue-grey-1" view="hHh Lpr lFf">
    <q-page-container>
      <q-page padding class="row items-center justify-center">
        <div class="row full-width">
          <div class="col-md-8 offset-md-2 col-xs-12 q-pl-md q-pr-md q-pt-sm">
            <q-card flat class="bg-white text-black">
              <div class="row">
                <div class="col-md-6 col-xs-12">
                  <div class="row q-pt-md q-pb-md ">
                    <div class="col-md-8 offset-2">
                      <q-img src="https://img.freepik.com/free-vector/secure-login-concept-illustration_114360-4582.jpg?w=740&t=st=1663775257~exp=1663775857~hmac=57244092af109ad84b199101190d707ea77a13ea07d475838a839fec62742c51"/>
                    </div>
                  </div>
                </div>
                <div class="q-pa-md">
                  <q-form
                    @submit="onSubmit"
                    class="q-gutter-md"
                  >
                    <q-input
                    class="q-pb-xs q-pt-md"
                      filled
                      v-model="name"
                      label="Username"
                      lazy-rules
                      :rules="[ val => val && val.length > 0 || 'Masukkan Username Anda']"
                    />

                    <q-input
                      filled
                      type="password"
                      v-model="password"
                      label="Password"
                      lazy-rules
                      :rules="[val => val !== null && val !== '' || 'Masukkan Password Anda']"
                    />

                      <div>
                      <q-btn class="full-width" label="Submit" type="submit" color="blue-7"/>
                      <q-btn class="full-width q-mt-md" label="Registrasi" unelevated/>
                    </div>
                  </q-form>
                </div>
              </div>
            </q-card>
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  setup () {
    return {
      name: null,
      password: null

      // onSubmit () {
      //   if (err) {
      //     $q.notify({
      //       color: 'red-5',
      //       textColor: 'white',
      //       icon: 'warning',
      //       message: 'You need to accept the license and terms first'
      //     })
      //   } else {
      //     $q.notify({
      //       color: 'green-4',
      //       textColor: 'white',
      //       icon: 'cloud_done',
      //       message: 'Submitted'
      //     })
      //   }
      // }
    }
  }
}
</script>
