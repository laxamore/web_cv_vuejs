<template>
  <div class="home">
    <div class="sidebar" v-bind:class="{show: show}" >
      <div class="photo">
        <img src="../../assets/img/me.png" alt="Me">
      </div>
      <div class="line"></div>
      <ul>
        <li class="about-me" v-bind:class="{active: aboutMeShow}">
          <a v-on:click="aboutMe">About Me</a>
        </li>
        <li class="my-skills" v-bind:class="{active: mySkillsShow}">
          <a v-on:click="mySkills">My Skills</a>
        </li>
        <li class="my-projects" v-bind:class="{active: myProjectsShow}">
          <a v-on:click="myProjects">My Projects</a>
        </li>
        <li class="achievements" v-bind:class="{active: achievementsShow}">
          <a v-on:click="achiev">Achievements</a>
        </li>
      </ul>
    </div>
    <div class="content" v-bind:class="{show: show}" >
      <div v-bind:class="{show: aboutMeShow}">
        <AboutMe/>
        <button v-on:click="closeContent">
          <div></div>
          <div></div>
        </button>
      </div>
      <div v-bind:class="{show: mySkillsShow}">
        <MySkills/>
        <button v-on:click="closeContent">
          <div></div>
          <div></div>
        </button>
      </div>
      <div v-bind:class="{show: myProjectsShow}">
        <MyProjects/>
        <button v-on:click="closeContent">
          <div></div>
          <div></div>
        </button>
      </div>
      <div v-bind:class="{show: achievementsShow}">
        <Achievements/>
        <button v-on:click="closeContent">
          <div></div>
          <div></div>
        </button>
      </div>
    </div>
    <div class="front">
      <h1 class="firstWord">
        I'm
        <span class="secondWord">Muchlis Kurnia</span>
      </h1>
      <h2>
        Embedded System, Machine Learning, Web Development.
      </h2>
      <div class="icon">
        <a href="https://www.facebook.com/akaryu.laxa" class="fa fa-facebook fa-2x"></a>
        <a href="#" class="fa fa-twitter fa-2x"></a>
        <a href="https://www.linkedin.com/in/muchlis-kurnia-644853178/" class="fa fa-linkedin fa-2x"></a>
        <a href="https://github.com/laxamore" class="fa fa-github fa-2x"></a>
      </div>
    </div>
    <div class="nav-button">
      <button v-bind:class="{show: show}" v-on:click="btnClick">
        <div></div>
        <div></div>
        <div></div>
      </button>
    </div>
  </div>
</template>

<script>
import AboutMe from '../contents/AboutMe'
import MySkills from '../contents/MySkills'
import MyProjects from '../contents/MyProjects'
import Achievements from '../contents/Achievements'
export default {
  name: 'Home',
  components: {
    AboutMe,
    MySkills,
    MyProjects,
    Achievements
  },
  data: function() {
    var vw = window.innerWidth;
    var aboutMeShow = true;

    if (vw <= 940) {
      aboutMeShow = false;
    }

    return {
      show: false,
      aboutMeShow: aboutMeShow,
      mySkillsShow: false,
      myProjectsShow: false,
      achievementsShow: false,
      windowWidth: vw
    }
  },
  methods: {
    btnClick: function() {
      this.show = !this.show;
    },
    aboutMe: function() {
      this.aboutMeShow = true;
      this.mySkillsShow = false;
      this.myProjectsShow = false;
      this.achievementsShow = false;
    },
    mySkills: function() {
      this.aboutMeShow = false;
      this.mySkillsShow = true;
      this.myProjectsShow = false;
      this.achievementsShow = false;
    },
    myProjects: function() {
      this.aboutMeShow = false;
      this.mySkillsShow = false;
      this.myProjectsShow = true;
      this.achievementsShow = false;
    },
    achiev: function() {
      this.aboutMeShow = false;
      this.mySkillsShow = false;
      this.myProjectsShow = false;
      this.achievementsShow = true;
    },
    closeContent: function() {
      this.aboutMeShow = false;
      this.mySkillsShow = false;
      this.myProjectsShow = false;
      this.achievementsShow = false;
    }
  },
  mounted() {
      this.$nextTick(() => {
        window.addEventListener('resize', () => {
          if (window.innerWidth <= 940) {
            this.aboutMeShow = false;
            this.mySkillsShow = false;
            this.myProjectsShow = false;
            this.achievementsShow = false;
          }
          else {
            this.aboutMeShow = true;
            this.mySkillsShow = false;
            this.myProjectsShow = false;
            this.achievementsShow = false;
          }
        });
      })
  }
}
</script>

<style scoped>
@import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css";
</style>

<style lang="scss" scoped>
@import "../../assets/scss/home.scss";
</style>

