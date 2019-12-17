<template>
  <div id="app">
    <v-app>
      <v-content>
        <div id="section-wrap">
          <v-layout column align-center justify-center>
            <header class="header">
              <nav class="header__nav">
                <ul class="header__navbar">
                  <li class="header__item">
                    <a href="#" class="header__link">
                      <transition name="slide-fade">
                        <!-- Header Navigation Menu Icons -->
                        <button
                          class="header--button"
                          v-if="show"
                          key="on"
                          @click="show = false"
                        >
                          <svg viewBox="0 0 24 24" class="header--icon">
                            <title>Close</title>
                            <path d="M0 0h24v24H0V0z" fill="none" />
                            <path
                              fill="currentColor"
                              d="M18.3 5.71c-.39-.39-1.02-.39-1.41 0L12 10.59 7.11 5.7c-.39-.39-1.02-.39-1.41 0-.39.39-.39 1.02 0 1.41L10.59 12 5.7 16.89c-.39.39-.39 1.02 0 1.41.39.39 1.02.39 1.41 0L12 13.41l4.89 4.89c.39.39 1.02.39 1.41 0 .39-.39.39-1.02 0-1.41L13.41 12l4.89-4.89c.38-.38.38-1.02 0-1.4z"
                            />
                          </svg>
                        </button>
                        <button
                          class="header--button"
                          v-else
                          key="off"
                          @click="show = true"
                        >
                          <svg
                            version="1.1"
                            class="header--icon"
                            xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink"
                            x="0px"
                            y="0px"
                            width="512px"
                            height="512px"
                            viewBox="0 0 512 512"
                            enable-background="new 0 0 512 512"
                            xml:space="preserve"
                          >
                            <title>Menu</title>
                            <g id="Icon_3_">
                              <g>
                                <path
                                  d="M64,384h384v-42.666H64V384z M64,277.334h384v-42.667H64V277.334z M64,128v42.665h384V128H64z"
                                />
                              </g>
                            </g>
                          </svg>
                        </button>
                      </transition>
                    </a>
                    <!-- Dropdown Menu -->
                    <transition name="dropdown">
                      <div
                        class="dropdown__menu"
                        v-bind:class="{ active: show }"
                        v-if="show"
                      >
                        <ul class="dropdown__menu-nav">
                          <li class="dropdown__menu-item">
                            <a
                              href="#"
                              class="dropdown__menu-link"
                              title="UX Design Portfolio"
                            >
                              <div class="dropdown__menu-svg">
                                <svg viewBox="0 0 640 512">
                                  <path
                                    fill="currentColor"
                                    d="M480 256c53 0 96-43 96-96s-43-96-96-96-96 43-96 96 43 96 96 96zm0-160c35.3 0 64 28.7 64 64s-28.7 64-64 64-64-28.7-64-64 28.7-64 64-64zM192 256c61.9 0 112-50.1 112-112S253.9 32 192 32 80 82.1 80 144s50.1 112 112 112zm0-192c44.1 0 80 35.9 80 80s-35.9 80-80 80-80-35.9-80-80 35.9-80 80-80zm80.1 212c-33.4 0-41.7 12-80.1 12-38.4 0-46.7-12-80.1-12-36.3 0-71.6 16.2-92.3 46.9C7.2 341.3 0 363.4 0 387.2V432c0 26.5 21.5 48 48 48h288c26.5 0 48-21.5 48-48v-44.8c0-23.8-7.2-45.9-19.6-64.3-20.7-30.7-56-46.9-92.3-46.9zM352 432c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16v-44.8c0-16.6 4.9-32.7 14.1-46.4 13.8-20.5 38.4-32.8 65.7-32.8 27.4 0 37.2 12 80.2 12s52.8-12 80.1-12c27.3 0 51.9 12.3 65.7 32.8 9.2 13.7 14.1 29.8 14.1 46.4V432zm271.7-114.9C606.4 291.5 577 278 546.8 278c-27.8 0-34.8 10-66.8 10s-39-10-66.8-10c-13.2 0-26.1 3-38.1 8.1 15.2 15.4 18.5 23.6 20.2 26.6 5.7-1.6 11.6-2.6 17.9-2.6 21.8 0 30 10 66.8 10s45-10 66.8-10c21 0 39.8 9.3 50.4 25 7.1 10.5 10.9 22.9 10.9 35.7V408c0 4.4-3.6 8-8 8H416c0 17.7.3 22.5-1.6 32H600c22.1 0 40-17.9 40-40v-37.3c0-19.9-6-38.3-16.3-53.6z"
                                  />
                                </svg>
                              </div>
                              <div class="dropdown__menu-text">
                                UX Design Portfolio
                              </div>
                            </a>
                          </li>
                          <li class="dropdown__menu-item">
                            <a
                              href="#"
                              class="dropdown__menu-link"
                              title="UI Development Portfolio"
                            >
                              <div class="dropdown__menu-svg">
                                <svg viewBox="0 0 576 512">
                                  <path
                                    fill="currentColor"
                                    d="M528 31H48C21.5 31 0 52.5 0 79v352c0 26.5 21.5 48 48 48h480c26.5 0 48-21.5 48-48V79c0-26.5-21.5-48-48-48zm16 400c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V79c0-8.8 7.2-16 16-16h480c8.8 0 16 7.2 16 16v352zm-352-68v8c0 6.6-5.4 12-12 12h-72c-6.6 0-12-5.4-12-12v-8c0-6.6 5.4-12 12-12h72c6.6 0 12 5.4 12 12zm192 0v8c0 6.6-5.4 12-12 12H236c-6.6 0-12-5.4-12-12v-8c0-6.6 5.4-12 12-12h136c6.6 0 12 5.4 12 12z"
                                  />
                                </svg>
                              </div>
                              <div class="dropdown__menu-text">
                                UI Development Portfolio
                              </div>
                            </a>
                          </li>
                          <!-- Dropdown Menu Separator -->
                          <hr />
                          <li class="dropdown__menu-item">
                            <a
                              href="#"
                              class="dropdown__menu-link"
                              title="Personal info"
                            >
                              <div class="dropdown__menu-svg">
                                <svg viewBox="0 0 576 512">
                                  <path
                                    fill="currentColor"
                                    d="M512 32H64C28.7 32 0 60.7 0 96v320c0 35.3 28.7 64 64 64h448c35.3 0 64-28.7 64-64V96c0-35.3-28.7-64-64-64zm32 384c0 17.6-14.4 32-32 32H64c-17.6 0-32-14.4-32-32V96c0-17.6 14.4-32 32-32h448c17.6 0 32 14.4 32 32v320zm-72-128H360c-4.4 0-8 3.6-8 8v16c0 4.4 3.6 8 8 8h112c4.4 0 8-3.6 8-8v-16c0-4.4-3.6-8-8-8zm0-64H360c-4.4 0-8 3.6-8 8v16c0 4.4 3.6 8 8 8h112c4.4 0 8-3.6 8-8v-16c0-4.4-3.6-8-8-8zm0-64H360c-4.4 0-8 3.6-8 8v16c0 4.4 3.6 8 8 8h112c4.4 0 8-3.6 8-8v-16c0-4.4-3.6-8-8-8zM208 288c44.2 0 80-35.8 80-80s-35.8-80-80-80-80 35.8-80 80 35.8 80 80 80zm0-128c26.5 0 48 21.5 48 48s-21.5 48-48 48-48-21.5-48-48 21.5-48 48-48zm46.8 144c-19.5 0-24.4 7-46.8 7s-27.3-7-46.8-7c-21.2 0-41.8 9.4-53.8 27.4C100.2 342.1 96 355 96 368.9V392c0 4.4 3.6 8 8 8h16c4.4 0 8-3.6 8-8v-23.1c0-7 2.1-13.8 6-19.6 5.6-8.3 15.8-13.2 27.3-13.2 12.4 0 20.8 7 46.8 7 25.9 0 34.3-7 46.8-7 11.5 0 21.7 5 27.3 13.2 3.9 5.8 6 12.6 6 19.6V392c0 4.4 3.6 8 8 8h16c4.4 0 8-3.6 8-8v-23.1c0-13.9-4.2-26.8-11.4-37.5-12.3-18-32.9-27.4-54-27.4z"
                                  />
                                </svg>
                              </div>
                              <div class="dropdown__menu-text">
                                Personal info
                              </div>
                            </a>
                          </li>
                          <li class="dropdown__menu-item">
                            <a
                              href="mailto:'tsmorro@gmail.com'"
                              class="dropdown__menu-link"
                              title="Send feedback"
                            >
                              <div class="dropdown__menu-svg">
                                <svg viewBox="0 0 512 512">
                                  <path
                                    fill="currentColor"
                                    d="M448 0H64C28.7 0 0 28.7 0 64v288c0 35.3 28.7 64 64 64h96v84c0 7.1 5.8 12 12 12 2.4 0 4.9-.7 7.1-2.4L304 416h144c35.3 0 64-28.7 64-64V64c0-35.3-28.7-64-64-64zm32 352c0 17.6-14.4 32-32 32H293.3l-8.5 6.4L192 460v-76H64c-17.6 0-32-14.4-32-32V64c0-17.6 14.4-32 32-32h384c17.6 0 32 14.4 32 32v288zm-224-88c-13.3 0-24 10.7-24 24s10.7 24 24 24 24-10.7 24-24-10.7-24-24-24zm-8.5-24h17c4.2 0 7.7-3.3 8-7.5l7-112c.3-4.6-3.4-8.5-8-8.5h-31c-4.6 0-8.3 3.9-8 8.5l7 112c.3 4.2 3.8 7.5 8 7.5z"
                                  />
                                </svg>
                              </div>
                              <div class="dropdown__menu-text">
                                Send me an email
                              </div>
                            </a>
                          </li>
                        </ul>
                      </div>
                    </transition>
                  </li>
                </ul>
              </nav>
            </header>
            <section id="header">
              <div id="header-back">
                <img id="head" src="./assets/header.png" />
              </div>
              <div id="logo">
                <img id="Vuelogo" src="./assets/cropped-Logo2.png" />
              </div>
            </section>
          </v-layout>
        </div>
      </v-content>
      <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
      <Recent project=""/>
    </v-app>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import Recent from "./components/Recent.vue";
import Butter from 'buttercms';
  
const butter = Butter('841b7ea512187e4f4114d3f81573c665b9298f1f');

@Component({
  components: {
    HelloWorld,
    Recent
  }

})

export default class App extends Vue {
  show: boolean = false;
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
#app {
  position: absolute;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100%;
  overflow: hidden;

  ul {
    list-style-type: none !important;
  }
  .header__nav {
    position: absolute !important;
    left: 0px;
    top: 100px;
  }
  .header {
    z-index: 2000;
    padding: 2rem 5rem 2rem 5rem;
    &__nav {
      position: relative;
    }
    &__navbar {
      display: flex;
      align-items: center;
      justify-content: flex-end;
    }
    &__item {
      padding: 1rem;
    }
    &--icon {
      width: 1.65rem;
      height: 1.65rem;
    }
    &--button {
      top: 0;
      right: 0;
      position: absolute;
      margin: 0;
      padding: 0;
      color: gray;
      cursor: pointer;
      border: 1px solid transparent;
      background-color: transparent;
      &:focus {
        outline: 0;
      }
    }
  }

  // Dropdown Menu

  .dropdown__menu {
    top: 100%;
    left: 0;
    position: absolute;
    z-index: 10;
    height: -webkit-fit-content;
    height: -moz-fit-content;
    height: fit-content;
    min-width: 400px;
    margin-top: 1rem;
    overflow-y: auto;
    padding: 1rem 1rem 1rem 0rem;
    border-radius: 50px;
    background-color: white;
    -webkit-box-shadow: 2px 2px 3px #777;
    box-shadow: 2px 2px 6px #777;
    /* border: 1px solid #777; */
    background-clip: padding-box;

    &-link {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      text-decoration: none;
      color: rgba(0, 0, 0, 0.6);
      padding: 0.8rem 0 0.8rem 2rem;
      margin-top: 0.2rem;
      margin-bottom: 0.2rem;
      border-radius: 0 50px 50px 0;
      &:hover {
        color: #17bf63;
        background-color: rgba(79, 192, 141, 0.1);
      }
    }
    &-svg {
      width: 1.5rem;
      height: 1.5rem;
    }
    &-text {
      font-weight: 300;
      margin-left: 1rem;
      margin-right: 1rem;
    }
  }

  // Animation Menu Icon

  .slide-fade-enter-active,
  .slide-fade-leave-active {
    transition: all 0.6s;
  }
  .slide-fade-enter,
  .slide-fade-leave-active {
    opacity: 0;
  }
  .slide-fade-enter {
    transform: translateX(31px);
  }
  .slide-fade-leave-active {
    transform: translateX(-31px);
  }

  // Dropdown Menu Animation

  .dropdown-enter-active,
  .dropdown-leave-active {
    transition: all 1s;
  }
  .dropdown-enter,
  .dropdown-leave-to {
    opacity: 0;
    transform: translateY(30px);
  }

  // Wrapper

  .main {
    margin: 6rem;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    &__subtitle {
      color: #4f5959;
      font-weight: 100;
      margin-bottom: 2rem;
    }
    &__link {
      margin-right: 1.5rem;
      display: inline-block;
      &:last-child {
        margin-right: 0;
      }
    }
    &__svg {
      width: 2rem;
      height: 2rem;
      opacity: 0.6;
      color: #94a2b0;
      &:hover {
        color: #ffad1f;
      }
    }
  }
  button.header__button {
    position: absolute;
    top: 30px;
    left: 30px;
  }
  section#header {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: block;

    -webkit-box-pack: center;
    -ms-flex-pack: center;
    z-index: 100;
    background: white;
    position: absolute;
    top: 0;
    left: 0;
    text-align: center;
    color: #2c3e50;
    width: 100%;
    div#header-back {
      width: 100%;
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      margin: 0;
      padding: 0;
      filter: drop-shadow(-1px 3px 4px rgba(50, 50, 0, 0.5));
      img#head {
        top: -100px;
        position: absolute;
        width: 100%;
        height: auto;
        max-height: 60vh;
        z-index: 100;
        display: block;
        /* box-shadow: 2px 2px 4px gray; */
      }
    }
    div#logo {
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      justify-content: flex-start;
      margin-top: 10px;
      width: 80%;
      margin-left: 50px;

      img#Vuelogo {
        width: 35%;
        margin-top: 0px;
        margin-left: 30px;
        z-index: 1000;
      }
    }
  }
}
</style>
