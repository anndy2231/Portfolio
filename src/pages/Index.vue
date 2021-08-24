<template>
  <q-layout view="lHh lpr lFf">
    <div
      v-bind:class="{
        main: $q.platform.is.desktop,
        mobile_main: $q.platform.is.ipad || $q.platform.is.mobile,
      }"
      class="full-height"
      style="background-color:rgba(0, 0, 0, 0.68);"
    >
      <q-header class="q-py-sm" style="background-color:rgba(0, 0, 0, 0.68);">
        <q-toolbar class="text-h4">
          <q-space></q-space>
          <q-tabs v-model="selected_tab" shrink>
            <q-tab
              name="about_me"
              :style="[
                selected_tab == 'about_me'
                  ? { backgroundColor: 'darkslateblue' }
                  : {},
              ]"
              class="q-mr-sm q-py-xs custom_tab"
              @click="scrollToElement('id_about_me')"
              style="width:120px;min-height:auto !important;color: white"
              label="About Me"
            />
            <q-tab
              name="works"
              :style="[
                selected_tab == 'works'
                  ? { backgroundColor: 'darkslateblue' }
                  : {},
              ]"
              class="q-mr-sm q-py-xs custom_tab"
              @click="scrollToElement('id_projects')"
              style="width:120px;min-height:auto !important;color: white"
              label="Work1"
            />
            <q-tab
              name="pubs"
              :style="[
                selected_tab == 'pubs'
                  ? { backgroundColor: 'darkslateblue' }
                  : {},
              ]"
              class="q-mr-sm q-py-xs custom_tab"
              @click="scrollToElement('id_publications')"
              style="width:120px;min-height:auto !important;color: white"
              label="Work2"
            />
            <q-tab
              name="photo"
              :style="[
                selected_tab == 'photo'
                  ? { backgroundColor: 'darkslateblue' }
                  : {},
              ]"
              class="q-mr-sm q-py-xs custom_tab"
              @click="scrollToElement('id_photo')"
              style="width:120px;min-height:auto !important;color: white"
              label="Work3"
            />
            <q-tab
              name="contact"
              :style="[
                selected_tab == 'contact'
                  ? { backgroundColor: 'darkslateblue' }
                  : {},
              ]"
              class="q-mr-sm q-py-xs custom_tab"
              @click="scrollToElement('id_contact_me')"
              style="width:120px;min-height:auto !important;color: white"
              label="Contact Me"
            />
          </q-tabs>
        </q-toolbar>
      </q-header>
      <section>
        <div
          class="full-height full-width flex flex-center text-center"
          style="background-color: rgba(0, 0, 0, 0.68) !important;z-index:0;height: 100vh !important;"
        >
          <div class="">
            <!-- <div class="text-h6 text-grey-5">WELCOME TO MY PAGE</div> -->
            <div
              class="text-h2 text-white q-py-sm q-my-md"
              style="border-top:4px solid darkslateblue; border-bottom: 4px solid darkslateblue;"
            >
              PORTFOLIO
            </div>
            <div class="text-h6" style="color: darkgrey;">
              WEB DEVELOPER
            </div>
            <div class="text-h6" style="color: darkslateblue;">
              NAM DEOK KIM
            </div>
          </div>
        </div>
      </section>
    </div>

    <div style="background-color:rgba(0, 0, 0, 0.68)" id="id_about_me">
      <div class="row">
        <div class="col-md-4 col-lg-4 col-xs-12 col-sm-12">
          <div
            style="background-color: rgba(0, 0, 0, 0.68)"
            class="q-pa-md text-center text-white text-weight-bolder text-h5"
          >
            ABOUT ME
          </div>
          <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
            <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <q-img
                style="height:auto;"
                class="col-5"
                src="/statics/images/profile1.jpg"
              />
            </div>
          </div>
        </div>
        <div
          class="col-md-8 col-lg-8 col-xs-12 col-sm-12 q-px-md q-pt-sm"
          style="background-color:rgba(0, 0, 0, 0.68)"
        >
          <div
            class="text-h4 text-center text-white"
            style="border-top:3px solid darkslateblue; border-bottom: 3px solid darkslateblue;"
          >
            Profile
          </div>
          <h2 class="text-h6" style="color: white; margin-left:40px">
            <br />
            2021.03 ~ : 폴리텍대학교 스마트금융과<br />
            <br />
            2018.02 : 가톨릭대학교 영어영문학과 졸업<br />
            <br />
          </h2>
        </div>
      </div>
    </div>
    <div style="background-color:rgba(0, 0, 0, 0.68)" id="id_projects">
      <div class="row q-px-xl" style="background-color:rgba(0, 0, 0, 0.68)">
        <div
          class="text-h4 text-center text-white q-py-sm q-my-md full-width"
          style="border-top:3px solid darkslateblue; border-bottom: 3px solid darkslateblue; margin-bottom:60px"
        >
          Stock Price Forecast
        </div>
        <div
          class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center"
        >
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon
                class="github-text"
                position="top-right"
                type="corner"
                color="white"
                background-color="darkslateblue"
              >
                <a
                  href="https://github.com/anndy2231/python/tree/master/%EC%A3%BC%EA%B0%80%EC%98%88%EC%B8%A1"
                  target="_blank"
                  >FORK ME ON GITHUB!</a
                >
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-purple">
                      2021 GitHub Archive Program
                    </div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a
                        class="project_link"
                        style="text-decoration: none; color: purple;"
                        href="https://github.com/anndy2231/python/tree/master/%EC%A3%BC%EA%B0%80%EC%98%88%EC%B8%A1"
                        target="_blank"
                        >Stock Price Forecast</a
                      >
                    </div>
                    <div class="text-caption text-grey-9">
                      Python Program
                      <ul>
                        <li>
                          KOSPI 시총 상위 10개 종목의 데이터를 기반으로 '투자
                          심리선' 지표 제작
                        </li>
                        <li>
                          투자심리도가 75% 이상이면 과열상태로 판단하여 매도시점
                          표기, 반대로 25% 이하일 경우 매수시점 표기
                        </li>
                        <li>
                          직관적인 그래프로 주식 초보에게 도움을 주도록 설계함
                        </li>
                      </ul>
                    </div>
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/portfolio1.png"
                    />
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/portfolio2.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator />

            <q-card-actions class="block">
              <div class="float-right q-py-sm">
                <iframe
                  class="float-right"
                  src="https://ghbtns.com/github-btn.html?user=anndy2231&repo=python&type=fork&count=true&size=large"
                  frameborder="0"
                  scrolling="0"
                  width="136"
                  height="30"
                  title="GitHub"
                ></iframe>
              </div>
            </q-card-actions>
          </q-card>
        </div>
      </div>
    </div>

    <div style="background-color:rgba(0, 0, 0, 0.68)" id="id_publications">
      <div class="row q-px-xl" style="background-color:rgba(0, 0, 0, 0.68);">
        <div
          class="text-h4 text-center text-white q-py-sm q-my-md full-width"
          style="border-top:3px solid darkslateblue; border-bottom: 3px solid darkslateblue; margin-bottom:60px"
        >
          Send Mail
        </div>
        <div
          class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center"
        >
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon
                class="github-text"
                position="top-right"
                type="corner"
                color="white"
                background-color="darkslateblue"
              >
                <a
                  href="https://github.com/anndy2231/SendMail/tree/master/Sendmail_Final"
                  target="_blank"
                  >FORK ME ON GITHUB!</a
                >
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-purple">
                      2021 GitHub Archive Program
                    </div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a
                        class="project_link"
                        style="text-decoration: none; color: purple;"
                        href="https://github.com/anndy2231/SendMail/tree/master/Sendmail_Final"
                        target="_blank"
                        >Send Mail</a
                      >
                    </div>
                    <div class="text-caption text-grey-9">
                      Java + Linux(SendMail Server) Program
                      <ul>
                        <li>
                          리눅스에 SendMail 서버 구축 후 Java로 제작한 이메일
                          전송 프로그램
                        </li>
                        <li>서버에 대한 이해, 리눅스 명령어 학습</li>
                        <li>게시판 CRUD, 로그인 세션처리</li>
                      </ul>
                    </div>
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/sendmail1.png"
                    />
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey;"
                      src="/statics/images/sendmail2.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator />

            <q-card-actions class="block">
              <div class="float-right q-py-sm">
                <iframe
                  class="float-right"
                  src="https://ghbtns.com/github-btn.html?user=anndy2231&repo=java&type=fork&count=true&size=large"
                  frameborder="0"
                  scrolling="0"
                  width="136"
                  height="30"
                  title="GitHub"
                ></iframe>
              </div>
            </q-card-actions>
          </q-card>
        </div>
      </div>
    </div>

    <div style="background-color:rgba(0, 0, 0, 0.68)" id="id_photo">
      <div class="row q-px-xl" style="background-color:rgba(0, 0, 0, 0.68)">
        <div
          class="text-h4 text-center text-white q-py-sm q-my-md full-width"
          style="border-top:3px solid darkslateblue; border-bottom: 3px solid darkslateblue; margin-bottom:60px"
        >
          MongoDB Board
        </div>
        <div
          class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center"
        >
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon
                class="github-text"
                position="top-right"
                type="corner"
                color="white"
                background-color="darkslateblue"
              >
                <a
                  href="https://github.com/anndy2231/java/tree/master/boardMongo"
                  target="_blank"
                  >FORK ME ON GITHUB!</a
                >
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-purple">
                      2021 GitHub Archive Program
                    </div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a
                        class="project_link"
                        style="text-decoration: none; color: purple;"
                        href="https://github.com/anndy2231/java/tree/master/boardMongo"
                        target="_blank"
                        >MongoDB Board</a
                      >
                    </div>
                    <div
                      class="text-caption text-grey-9"
                      style="margin-bottom:33px"
                    >
                      MongoDB + Java Program
                      <ul>
                        <li>NoSQL MongoDB와 Spring으로 제작한 게시판</li>
                        <li>게시판 CRUD, 로그인 세션처리</li>
                        <li>MongoDB에 대한 이해</li>
                      </ul>
                    </div>
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/mongodb3.png"
                    />
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/mongodb2.png"
                    />
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/mongodb1.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator />

            <q-card-actions class="block">
              <div class="float-right q-py-sm">
                <iframe
                  class="float-right"
                  src="https://ghbtns.com/github-btn.html?user=anndy2231&repo=java&type=fork&count=true&size=large"
                  frameborder="0"
                  scrolling="0"
                  width="136"
                  height="30"
                  title="GitHub"
                ></iframe>
              </div>
            </q-card-actions>
          </q-card>
        </div>
      </div>
    </div>

    <div id="contact_us">
      <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
        <div
          style="text-align:center; padding-top:30px;"
          class="text-h4 text-white"
        >
          FEEL FREE TO CONTACT ME
        </div>
        <form action="https://formspree.io/f/mnqlowoe" method="POST">
          <div class="row text-center flex flex-center q-py-lg">
            <div
              class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none"
            >
              <q-input
                required
                v-model="name"
                name="name"
                bg-color="white"
                outlined
                label="Your Name *"
              >
                <template v-slot:append>
                  <q-icon name="list" style="color:darkslateblue" />
                </template>
              </q-input>
              <q-input
                type="email"
                required
                v-model="email"
                name="_replyto"
                bg-color="white"
                outlined
                label="Your Email *"
              >
                <template v-slot:append>
                  <q-icon name="email" style="color:darkslateblue" />
                </template>
              </q-input>
            </div>
            <div
              class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none"
            >
              <q-input
                required
                v-model="message"
                name="message"
                class=""
                type="textarea"
                bg-color="white"
                outlined
                label="Your Message *"
              >
                <template v-slot:append>
                  <q-icon name="comment" style="color:darkslateblue" />
                </template>
              </q-input>
            </div>
          </div>
          <div class="row flex flex-center text-center q-pb-xl q-mt-md">
            <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12">
              <q-btn
                type="submit"
                size="lg"
                style="background:darkslateblue; color: white"
                label="Send Message"
              />
            </div>
          </div>
        </form>
      </div>
    </div>
    <q-toolbar
      class="flex flex-center text-white"
      style="background-color: #1c1b21; border-top: 2px solid darkslateblue"
      id="id_contact_me"
    >
      <div class="q-pa-sm q-gutter-sm">
        <q-btn
          target="_blank"
          style="border: 2px solid darkslateblue"
          round
          type="a"
          href="https://github.com/anndy2231"
          glossy
          icon="fab fa-github"
        />
        <q-btn
          style="border: 2px solid darkslateblue"
          round
          type="a"
          href="mailto:anndy24h@gmail.com"
          glossy
          icon="email"
        />
      </div>
    </q-toolbar>
  </q-layout>
</template>

<script>
import { scroll } from "quasar";

const { getScrollTarget, setScrollPosition } = scroll;
export default {
  name: "PageIndex",
  data() {
    return {
      name: "",
      email: "",
      message: "",
      selected_tab: "about_me",
      modalWindow: false,
    };
  },
  methods: {
    scrollToElement(id) {
      let el = document.getElementById(id);
      const target = getScrollTarget(el);
      const offset = el.offsetTop - 65;
      const duration = 800;
      setScrollPosition(target, offset, duration);
    },
    imgDetails() {
      this.modalWindow = true;
    },
  },
  mounted: function() {
    // let canvas2Settings = {
    //     "target": "canvas2",
    //     "max": "120",
    //     "animate": true,
    //     "props": ["circle", "square", "triangle", "line"],
    //     "colors": [[165, 104, 246], [230, 61, 135], [0, 199, 228], [253, 214, 126]],
    //     "clock": "20"
    // };
    // let canvas2 = new ConfettiGenerator(canvas2Settings);
    // canvas2.render();
  },
};
</script>

<style>
.main {
  background: black;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh !important;
}

.mobile_main {
  background: url(/statics/images/my_1_2.jpg) no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh !important;
}

.my-card {
  width: 100%;
  max-width: 800px;
  border: none;
  border-radius: 0px;
}

.sponsor-card {
  width: 100%;
  max-width: 240px;
  border: none;
  border-radius: 6px;
}

.project_link:hover {
  text-decoration: underline !important;
}

.sketch_desktop {
  width: 100%;
  height: 100%;
  display: block;
  margin: auto;
  border: 5px solid #30313b;
}

.sketch_mobile {
  width: 100%;
  height: 100% !important;
  border: 20px solid #30313b;
}

#contact_us {
  background: url(/statics/images/contact_us.jpg);
  background-size: cover;
  background-position: 50%;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

.custom_tab {
  width: 130px;
}

body {
  overflow-x: hidden;
}

section {
  position: relative;
}

section > * {
  z-index: 9;
  position: relative;
  top: 0;
}

section > canvas {
  z-index: 1;
  position: absolute;
  left: 0;
}
</style>
