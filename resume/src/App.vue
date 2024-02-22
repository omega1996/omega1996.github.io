
<template>
  <div>
    <Header></Header>
    <div class="app">
      <p>Frontend Developer</p>
      <p>
        {{ age }} years, male
      </p>
      <p>
        Developer with <span>{{ experience }}+ years</span> of experience in developing and maintaining web applications.
      </p>
      <p>
        Reasonable, solution oriented team-player with developed soft skills and willingness to learn and share.
      </p>
      <div>
        <ul>
          <li>
            web applications of any complexity <span class="comment">//social networks, online stores</span>
          </li>
          <li>
            made a lot of <span>MVP</span>s <span class="comment">//pet projects, demo applications, hackathon
              apps</span>
          </li>
          <li>
            won several hackathons with <span>LateDev</span> team
          </li>
          <li>
            telegram <span>chat bots</span>
          </li>
          <li>
            have Masters degree in <span>Information Technology</span><span class="comment"> //specialization in machine
              learning</span>
          </li>
        </ul>
      </div>
      <p>
        Tech stack:
      </p>
      <div>
        <ul>
          <li>
            languages: <span>TypeScript, JavaScript, Python</span>
          </li>
          <li>
            frameworks: <span>Vue.js, Quasar, FastAPI</span>
          </li>
          <li>
            storages: <span>Pinia, Vuex</span>
          </li>
          <li>
            databases: <span>PostgreSQL, SQLite</span>
          </li>
          <li>
            markup: <span>HTML, CSS, SCSS, SASS, Less</span>
          </li>
          <li>
            testing: <span>Jest</span>
          </li>
          <li>
            bundlers: <span>Webpack, Gulp, Vite </span>
          </li>
          <li>
            runtime_builders: <span>Bun, Node.js</span>
          </li>
          <li>
            team_work: <span>Git, Jira, Confluence</span>
          </li>
          <li>
            IDE: <span>VSCode</span>
          </li>
        </ul>
      </div>
      <p>
        Work experience:
      </p>
      <div>
        <Accordion title="Heyscribe" comment="02.2023 - 11.2023. #1 Productivity app at ProductHunt">
          <ul>
            <li>&nbsp;<a target="_blank" href="https://my.heyscribe.com">my.heyscribe.com
              </a>
            </li>
            <li>
              Created web application and frontend infrastructure from scratch
            </li>
            <li>
              Made pixel perfect markup
            </li>
            <li>
              Created a lot of components
            </li>
            <li>
              Managed GitLab repository, including CI/CD setup using AWS
            </li>
            <li>
              Rewrote pure Vue 3 (vite + pinia + ts) app to quasar SSR
            </li>
            <li>
              Successfully launched MPV
            </li>
          </ul>

        </Accordion>
        <Accordion title="EBAC online" comment="10.2021 -  11.2022. #2 Ed-tech in LATAM">
          <ul>

            <li>&nbsp;<a target="_blank" href="https://ebaconline.com.br/">ebaconline.com.br
              </a>
            </li>
            <li>
              Made a lot of UI-kit components (storybook)
            </li>
            <li>
              Feature development (notes component, visual sign editor etc.)
            </li>
            <li>
              Redesign, refactoring, code-review
            </li>
            <li>
              Pixel perfect markup
            </li>
            <li>
              Holding daily meetings, teamlead and PM support
            </li>
            <li>
              Assistance in establishing management processes
            </li>
          </ul>


        </Accordion>
        <Accordion title="Napoleon IT" comment="01.2019 - 10.2021">
          <ul>
            <li>
              Machine-learning based platform development
            </li>
            <li>
              Full-Stack (Backend and frontend) development
            </li>
            <li>
              Management optimization </li>
            <li>
              Data analytics
            </li>
            <li>
              Creation of several machine learning based MVPs
            </li>
            <li>
              Creation of educational program for newbies in frontend
            </li>
            <li>
              Leading 2 developers
            </li>
            <li>
              Cust-dev, code-review, repository management
            </li>
          </ul>
        </Accordion>
      </div>


    </div>
    <div class="app__background">
      <Background />
    </div>






  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue';
import Accordion from './components/Accordion.vue'
import Background from './components/Background.vue';
import Header from './components/Header.vue';



const age = computed(() => {
  const dateNow = new Date()
  const myAge = new Date('1996-03-31')
  dateNow.getMonth() < myAge.getMonth()
  // @ts-ignore
  const age = dateNow.getFullYear() - myAge.getFullYear() - (dateNow.getMonth() < myAge.getMonth() || (dateNow.getMonth() === myAge.getMonth() && dateNow.getDate() < myAge.getDate()));
  return age;
})


const experience = computed(() => {
  const dateNow = new Date()
  const myAge = new Date('2018-09-15')
  dateNow.getMonth() < myAge.getMonth()
  // @ts-ignore
  const age = dateNow.getFullYear() - myAge.getFullYear() - (dateNow.getMonth() < myAge.getMonth() || (dateNow.getMonth() === myAge.getMonth() && dateNow.getDate() < myAge.getDate()));
  return age;
})

</script>
<style scoped lang="scss">
@keyframes gradient {
  0% {
    background-position: 0% 0%;
  }



  100% {
    background-position: 0 100%;
  }

}

.app {




  z-index: 2;
  position: relative;
  font-family: 'Roboto Mono';
  font-weight: 600;
  padding: 2rem;
  padding-bottom: 0;
  width: calc(100% - 4em);

  color: #98d6f7;

  span {
    color: #bd9178;
  }

  span.comment {
    color: #6A9955;
  }

  p {
    background-color: #010215;
    width: fit-content;
  }

  li {

    list-style-type: none;

    span {
      background-color: #010215;
    }
  }

  li:before {
    content: "-";
    text-indent: -5px;
  }

  h1 {
    margin: 0;
    padding: 0;
  }

  &__background {
    width: 100%;
    font-family: 'Roboto Mono';
    position: fixed;
    top: 0;
    z-index: 0;
  }


}
</style>
