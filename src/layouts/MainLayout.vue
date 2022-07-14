<template>
  <q-layout view="lHh Lpr lFf" class="darkMode">
    <q-header reveal>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="toggleLeftDrawer"
          aria-label="Menu"
          icon="menu"
        />
        
        <q-toolbar-title>
           <q-avatar>
            <img src="https://vpdtnd.vnptioffice.vn/qlvbdh_ndh/login/img/logo-header.png">
          </q-avatar>
          Bộ Chỉ Số
        </q-toolbar-title>
         <q-space/>
          
         <div class="q-gutter-sm row items-center no-wrap">

          
          <dark-mode-t/>
          
          <q-btn round dense flat color="white" icon="notifications">
            <q-badge color="red" text-color="white" floating>
              5
            </q-badge>
            <q-menu
            >
              <q-list style="min-width: 100px">
                <messages></messages>
                <q-card class="text-center no-shadow no-border">
                  <q-btn label="Xem chi tiết" style="max-width: 120px !important;" flat dense
                         class=""></q-btn>
                </q-card>
              </q-list>
            </q-menu>
          </q-btn>
          <q-btn round flat>
            <q-avatar size="35px">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
              <q-menu>
                <q-list style="min-width: 100px">
                  <q-item clickable v-close-popup >
                    <q-item-section>Đăng nhập</q-item-section>
                  </q-item>
                  <q-separator />
                  <q-item clickable v-close-popup>
                    <q-item-section>Đăng xuất</q-item-section>
                  </q-item>
                </q-list>
              </q-menu>

            </q-avatar>
          </q-btn>
         </div>
      </q-toolbar>
    </q-header>
        

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      class="darkMode"
    >
      <q-list >
        <q-item-label header>Danh mục</q-item-label>
        <q-item to="/dashboard" active-class="q-item-no-link-highlighting">
          <q-item-section avatar>
            <q-icon name="dashboard"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Dashboard</q-item-label>
          </q-item-section>
        </q-item>
        <q-expansion-item
          icon="pages"
          label="Pages"
        >
          <q-list class="q-pl-lg">
            <q-item to="/login" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="email"/>
              </q-item-section>
              <q-item-section>
                <q-item-label class="login-button">Đăng nhập</q-item-label>
              </q-item-section>
            </q-item>
            <q-item to="src/pages/register" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="lock"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>Tạo tài khoản</q-item-label>
              </q-item-section>
            </q-item>
            <q-item to="/Lock-2" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="lock"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>Lock Screen - 2</q-item-label>
              </q-item-section>
            </q-item>
            <q-item to="/Profile" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="person"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>User Profile</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-expansion-item>
        <q-expansion-item
          icon="map"
          label="Maps"
        >
          <q-list class="q-pl-lg">
            <q-item to="/Map" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="map"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>Map</q-item-label>
              </q-item-section>
            </q-item>
            <q-item to="/MapMarker" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="location_on"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>Map Marker</q-item-label>
              </q-item-section>
            </q-item>
            <q-item to="/StreetView" active-class="q-item-no-link-highlighting">
              <q-item-section avatar>
                <q-icon name="streetview"/>
              </q-item-section>
              <q-item-section>
                <q-item-label>Street View</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-expansion-item>
        <q-item clickable target="_blank" rel="noopener" href="http://chat.quasar.dev">
          <q-item-section avatar>
            <q-icon name="chat" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Discord Chat Channel</q-item-label>
            <q-item-label caption>https://chat.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable target="_blank" rel="noopener" href="https://forum.quasar.dev">
          <q-item-section avatar>
            <q-icon name="record_voice_over" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Forum</q-item-label>
            <q-item-label caption>https://forum.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable target="_blank" rel="noopener" href="https://twitter.quasar.dev">
          <q-item-section avatar>
            <q-icon name="rss_feed" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Twitter</q-item-label>
            <q-item-label caption>@quasarframework</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable target="_blank" rel="noopener" href="https://facebook.quasar.dev">
          <q-item-section avatar>
            <q-icon name="public" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Facebook</q-item-label>
            <q-item-label caption>@QuasarFramework</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent ,ref } from 'vue'
import DarkModeT from 'src/components/DarkModeT.vue'

export default defineComponent({
    name: "MainLayout",

    components: {
        DarkModeT,
        
    },
    
    setup() {
        const leftDrawerOpen = ref(false);
        function toggleLeftDrawer() {
            leftDrawerOpen.value = !leftDrawerOpen.value;
        }
        return {
            leftDrawerOpen,
            toggleLeftDrawer
        };
    }

})



</script>

<style>

</style>