<template>
  <q-layout>
    <q-page-container class="login-container">
      <div >
        <q-img id="login-logo"
          src="https://itvnpt.vn/wp-content/uploads/2021/11/Logo-VNPT-TP-HCM-1.png"
          
          
        />
      
     
      </div>
      <div>
        <q-card v-bind:style="$q.screen.lt.sm?{'width': '70%'}:{'width':'25%'}" class="login-card">
          <q-card-section> 
            <q-avatar size="103px" class="absolute-center shadow-10">
              <img src="https://cdn.popsww.com/blog/sites/2/2022/02/zoro-sau-2-nam.jpg">
            </q-avatar>
          </q-card-section>
          <q-card-section>
            <div class="text-center q-pt-lg">
              <div class="col text-h6 ellipsis">
                Đăng nhập
              </div>
            </div>
          </q-card-section>
          <q-card-section>
            <q-form
              class="q-gutter-md"
            >
              <q-input
                filled
                v-model="username"
                label="Tài khoản"
                lazy-rules
              />

              <q-input
                type="password"
                filled
                v-model="password"
                label="Mật khẩu"
                lazy-rules

              />

              <div>
                <q-btn id="login-button" label="Đăng nhập" to="/" type="button" color="primary" />
              </div>
            </q-form>
          </q-card-section>
          
        </q-card>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>
import {defineComponent} from 'vue'
import {ref} from 'vue'

export default defineComponent({
  setup() {
    return {
      username: ref('admin'),
      password: ref('admin')
    }
  },
})
</script>
.
<style lang="scss" scoped>

.login-container{
  width: auto;  
  min-height: 90%;
  padding: 50 50 50 50;
}
#login-logo{
  height: 30%;
  width: 40%;
  margin-right: auto;
  margin-left: auto;
  display: block;
 
}
.login-card{
  margin-top: 70px;
  margin-left: auto;
  margin-right: auto;
  height: 100%;
 
}

#login-button {
  width: 100%;
  height: 50px;

}

</style>