<template>
  <v-app dark color="grey lighten-1">

    <v-app-bar color="grey lighten-1"  :clipped-left="clipped" fixed app>
      <v-btn icon  @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      <span class="fantez" style="font-size: 1.5rem">سجا</span>
      <v-spacer/>
      <v-btn color="grey darken-2" text link to="/logout">
        <v-icon>mdi-logout</v-icon>
        <span class="mr-2 ">خروج</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <div class="ma-7">
        <nuxt/>
      </div>
    </v-main>

    <v-navigation-drawer v-model="rightDrawer" color="cyan accent-4" right app dark>
      <v-row justify="center" class="mt-10">
        <v-col cols="12" class="justify-center d-flex">
          <v-img
            src="/miniLogo.png"
            alt="User picture"
            max-width="100"
          />
        </v-col>
        <v-col cols="12" class="justify-center d-flex flex-column">
          <p class="white--text text-center">محمد ابوطالبی</p>
          <p class="white--text text-center">کاربر</p>

        </v-col>
      </v-row>

      <v-list sub-grup nav dark class="sidebar-menu">
        <v-list-item exact to="" no-prefetch link>
          <v-list-item-action>
            <v-icon white>mdi-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>داشبورد</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-group no-action>
          <template v-slot:activator>
            <v-list-item-action>
              <v-icon>mdi-menu</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>منو</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item to="" link>
            <v-list-item-action>
              <i class="fal fa-fw ml-1 fa-chalkboard-teacher"></i>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>منو های اصلی</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="" link>
            <v-list-item-action>
              <i class="fal fa-fw ml-1 fa-layer-plus"></i>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>محصولات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>

        <v-list-item to="" link >
          <v-list-item-action>
            <v-icon>mdi-clipboard-list</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>سفارش ها</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item to="" link >
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>کاربران</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item to="" link >
          <v-list-item-action>
            <v-icon>mdi-comment</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>نظرات</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item to="" link >
          <v-list-item-action>
            <v-icon>mdi-cog</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>تنظیمات</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

      </v-list>
    </v-navigation-drawer>

    <alert/>
  </v-app>
</template>

<script>
// import {mapGetters} from "vuex";
// import Alert from "@/components/utilities/Alert";

export default {

  name: "dashboard",

  // components: {Alert},

  // middleware: 'coffe',

  // async created() {
  //   await this.$store.dispatch('coffe/getCoffe')
  //   this.checkAccess()
  // },

  data() {
    return {
  //     clipped: false,
  //     drawer: false,
  //     fixed: false,
  //     miniVariant: false,
  //     right: true,
      rightDrawer: true,
  //     title: 'dashboard'
    }
  },

  // computed: {
  //   ...mapGetters({
  //     hasPlan: 'coffe/hasPlan',
  //     hasPlanExpired: 'coffe/hasPlanExpired',
  //   })
  // },

  // methods: {
  //   checkAccess() {
  //     if (this.hasPlanExpired) {
  //       this.$router.push('/dashboard/expired')
  //     }
  //     let route = this.$route.path
  //     let guards = [
  //       {route: /\/dashboard\/comment*/i, plan: 'club'},
  //       {route: /\/dashboard\/order*/i, plan: 'order'},
  //       {route: /\/dashboard\/user*/i, plan: 'club'},
  //     ]
  //     let flag = false
  //     guards.forEach(guard => {
  //       if (!(route.match(guard.route) && this.hasPlan(guard.plan))) {
  //         flag = true
  //       }
  //     })
  //     !flag && this.$router.push('/dashboard')
  //   }
  // }

}

</script>


<style>
.db1 {
  background: #242833 !important;
}

.db2 {
  background-color: #343B4C;
}

.db3 {
  background: #616872 !important;
}

.db4 {
  background: #F34747 !important;
}

.dc1 {
  color: #242833 !important;
}

.dc2 {
  color: #343B4C !important;
}

.dc3 {
  color: #616872 !important;
}

.dc4 {
  color: #F34747 !important;
}

.dc5 {
  color: #fdfcfa !important;
}

.v-toolbar__content, .v-toolbar__extension {
  background: #EEEEEE;
  color: #616161;
}

body{
  font-family:iransans !important ;
}

.v-label {
  right: 0 !important;
  left: auto !important;
  font-family: iransans !important;
}

.sidebar-menu .v-list-item__title {
  font-size: 12px !important;
}

.sidebar-menu .v-list-item__action {
  margin-left: 4px !important;
  margin-right: 0px !important;
}

/* .nuxt-link-exact-active div,
.v-list-item--active {
  background: #00667a !important;
} */
.sidebar-menu a {
  color: #fff !important;
  text-decoration: none !important;
}

.sidebar-menu .v-list-item {
  margin-bottom: 0px !important;
}

.sidebar-menu .v-list-item__action i,
.sidebar-menu .v-list-item__icon i {
  font-size: 18px;
}

.sidebar-menu .v-list-item__icon {
  margin-left: 4px !important;
}

.v-navigation-drawer__content .primary--text {
  color: #fff !important;
  caret-color: #fff !important;
}

.v-application--is-rtl
.v-list-group--no-action
> .v-list-group__items
> .v-list-item {
  padding-right: 25px;
}

/* .v-navigation-drawer__content .primary--text i {
  color: #024e5e !important;
  text-shadow: 0px 0px 10px rgba(22, 199, 255, 0.5) !important;
} */
.v-text-field--filled:not(.v-text-field--single-line) input {
  margin-top: 4px !important;
}

.v-app-bar__nav-icon {
  margin-left: 5px !important;
}

.sid-icon-close {
  color: white;
  font-size: 24px;
  cursor: pointer;
}

.v-card__text, .v-application .headline {
  font-family: iransans !important;
}

button i:before {
  left: 0 !important;
}

td i:before {
  top: 1px !important;
}
</style>
