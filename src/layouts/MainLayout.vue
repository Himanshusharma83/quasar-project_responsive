<template>
  <div class="q-pa-md">
    <q-layout view="hHh lpR fFf">
      <q-header elevated class="bg-white text-black">
        <q-toolbar>
          <img
            src="~assets/menu-2-fill.svg"
            @click="toggleLeftDrawer"
            style="margin-right: 15px; cursor: pointer"
          />

          <q-toolbar-title>
            <img
              class="himimg"
              src="~assets/Himanshu-designstyle-boots-m.png"
              style="width: 100px; height: 50px; margin-top: 7px"
            />
          </q-toolbar-title>
          <img
            src="~assets/user.svg"
            class="user"
            style="
              margin-right: 15px;
              background-color: lightslategray;
              border-radius: 50%;
              cursor: pointer;
            "
          />
          <small
            class="text"
            style="margin-right: 30%; font-size: 1.2rem; cursor: pointer"
            >One Day I will Find my Joy...</small
          >

          <img
            src="~assets/bell.svg"
            style="margin-right: 15px; cursor: pointer"
          />
          <img
            src="~assets/log-out.svg"
            style="margin-right: 20px; cursor: pointer"
          />
        </q-toolbar>
      </q-header>

      <q-drawer
        show-if-above
        v-model="leftDrawerOpen"
        side="left"
        bordered
        :breakpoint="500"
        :width="240"
      >
        <div class="q-pa-md" id="items">
          <div class="q-pa-md">
            <div class="q-gutter-md row items-start learn">
              <img src="~src/assets/book-open.svg" class="book" />
              <!---Nav-->
              <div class="menu-item" @click="isOpen = !isOpen">
                <a href="#" class="learner"> {{ options2[4] }}</a>
                <div class="down1">
                  <img src="~src/assets/chevron-down.svg" class="down" />
                </div>
                <transition name="fade" apear>
                  <div class="sub-menu" v-if="isOpen">
                    <div class="menu-item">
                      <router-link to="/services/web"></router-link>
                    </div>
                    <div class="menu-item">
                      <router-link to="/services/design">{{
                        options[0]
                      }}</router-link>
                    </div>
                    <div class="menu-item">
                      <router-link to="/services/videos">{{
                        options[1]
                      }}</router-link>
                    </div>
                  </div>
                </transition>
              </div>

              <!--Nav--->
            </div>
            <div class="mic-svg">
              <img src="~src/assets/mic-(1).svg" class="mic" />
              <a :label="options2[0]" class="expert">{{ options2[0] }}</a>
            </div>
            <div class="fre_Courses">
              <img src="~src/assets/eye-line-(1).svg" class="free-courses" />
              <a :label="options2[1]" class="courses">{{ options2[1] }}</a>
            </div>
            <div class="light">
              <img src="~src/assets/lightbulb-line.svg" class="bulb" />
              <a :label="options2[1]" class="light_bulb">{{ options2[2] }}</a>
            </div>
            <div class="file">
              <img src="~src/assets/file-text.svg" class="text-img" />
              <a :label="options2[1]" class="text">{{ options2[3] }}</a>
            </div>
          </div>
        </div>

        <hr width="150" class="line" />

        <div class="acc-setting">
          <img src="~src/assets/settings.svg" class="setting" />
          <a href="#" class="accounts">Account Settings</a>
        </div>
        <div class="user-profile">
          <img src="~src/assets/user.svg" class="user" />
          <a href="#" class="profile">View Profile</a>
        </div>
        <div class="user-profile">
          <img src="~src/assets/tool.svg" class="user" />
          <a href="#" class="profile">Preferences</a>
        </div>
        <div class="user-profile">
          <img src="~src/assets/link.svg" class="user" />
          <a href="#" class="profile">Link Accounts</a>
          <p class="total">1 of Total 2 Accounts</p>
        </div>
      </q-drawer>

      <q-page-container>
        <LayoutPage />
        <CardsPage />
        <Cards2Page />
      </q-page-container>
    </q-layout>
  </div>
  <FooterPage />
</template>

<script>
import { ref } from "vue";

import LayoutPage from "../components/LayoutPage.vue";
import CardsPage from "src/components/CardsPage.vue";
import FooterPage from "../components/FooterPage.vue";
import Cards2Page from "src/components/Cards2Page.vue";

export default {
  data() {
    return {
      isOpen: false,
    };
  },
  setup() {
    const leftDrawerOpen = ref(false);
    return {
      options: ["Free Courses", "Certification Courses"],
      options2: [
        "Expert Talks",
        "Free Course Preview",
        "Whitepapers",
        "Newsletters",
        "Learn",
      ],
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
  components: { LayoutPage, CardsPage, FooterPage, Cards2Page },
};
</script>
<style scoped>
/* #items {
  margin-top: 30%;
} */
.menu-item a {
  text-decoration: none;
  font-size: 0.9rem;

  color: black;
}
.menu-item a:hover {
  background-color: gray;
}
.book {
  font-weight: 500;
  width: 1.2rem;
  float: right;
  margin-left: 1rem;
  margin-bottom: 1rem;
}
.learn {
  display: flex;
  flex-wrap: nowrap;
}
.learner {
  float: left;
  font-size: 0.8rem;
  font-weight: 500;
}
.down1 {
  margin-left: 7rem;
  /* margin-bottom: -25rem; */
  cursor: pointer;
}
.down:active {
  transform: rotateX(120deg);
}
.expert {
  font-weight: 500;
  font-size: 0.8rem;
  margin-left: 1.25rem;
  cursor: pointer;
}
.mic-svg {
  font-weight: 500;
  font-size: 0.8rem;
}
.mic {
  width: 0.9rem;
}
.free-courses {
  width: 1rem;
  margin-top: 1rem;
}
.courses {
  margin-left: 1.25rem;
  margin-top: -0.5rem;
  cursor: pointer;
  font-size: 0.8rem;
  font-weight: 500;
}
.bulb {
  width: 1.2rem;
  margin-top: 1rem;
}
.light_bulb {
  font-weight: 500;
  font-size: 0.8rem;
  margin-left: 1rem;
  cursor: pointer;
}
.text-img {
  width: 1.2rem;
  margin-top: 1rem;
}
.text {
  font-weight: 500;
  font-size: 0.8rem;
  margin-left: 1rem;
  cursor: pointer;
}
.line {
  margin-top: 3rem;
  font-weight: 300;
}
.acc-setting {
  margin-top: 3rem;
  margin-bottom: 2.5rem;
}
.setting {
  margin-left: 2rem;
  float: left;
}
.accounts {
  text-decoration: none;
  color: gray;
  margin-left: 0.5rem;
}
.user {
  float: left;
}
.user-profile {
  margin-top: 1rem;
  margin-left: 2rem;
}
.profile {
  text-decoration: none;
  color: black;
  margin-left: 0.4rem;
}
.total {
  font-size: 0.7rem;
  margin-left: 2rem;
  color: gray;
}
.menu-btn {
  visibility: hidden;
}
.xbtn-div {
  visibility: hidden;
}
.file::after {
  background: gray;
}
@media (min-width: 300px) and (max-width: 700px) {
  .user {
    display: none;
  }
  .text {
    display: none;
  }
  .himimg {
    margin-left: 30%;
  }
}
</style>
