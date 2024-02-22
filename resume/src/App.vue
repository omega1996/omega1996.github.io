
<template>
  <div>
    <Header></Header>
    <div class="app">
      <div>
        <a target="_blank" href="/Resume.pdf">Download resume</a>
      </div>
      <div>

        <a href="https://github.com/omega1996" target="_blank">My GitHub</a>
      </div>
      <p>Frontend Developer</p>
      <p>
        {{ age }} years, male
      </p>
      <p>
        Developer with <Hint :text="'Since ' + new Date('2018-09-15').toLocaleDateString()">{{ experience }}+ years</Hint>
        of
        experience in
        developing and
        maintaining web
        applications.
      </p>
      <p>
        Reasonable, solution oriented team-player with developed soft skills and willingness to learn and share.
      </p>
      <div>
        <ul>
          <li>
            web applications of any complexity <span class="comment">//social networks, online stores, any-management
              systems</span>
          </li>
          <li>
            made a lot of <Hint text="Minimal Viable Product">MVP</Hint>s <span class="comment">//pet projects, demo
              applications, hackathon
              apps</span>
          </li>
          <li>
            won several hackathons with <Hint>LateDev
              <template #hint>
                <a href="https://github.com/Late-Dev" target="_blank">github.com/Late-Dev</a>
              </template>
            </Hint> team
          </li>
          <li>
            telegram <Hint text="Chat interface and mini-apps">chat bots</Hint>
          </li>
          <li>
            have Masters degree in <Hint text="Bachelors degree in electronics (a.k.a. engineer)">Information
              Technology</Hint><span class="comment"> //specialization in machine
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
            languages: <Hint
              text="I apply OOP, SOLID, KISS, DRY, and YAGNI principles. I'll help you to design and develop your project.">
              TypeScript, JavaScript, Python</Hint>
          </li>
          <li>
            frameworks: <Hint
              text="I'm good in vanilla JS and Python, but I thrive in frameworks like Vue, Quasar, and FastAPI, have experience in Django, Flask, React, Electron, and more.">
              Vue.js, Quasar, FastAPI</Hint>
          </li>
          <li>
            storages: <Hint text="Or any storage you prefer">Pinia, Vuex, Redux Toolkit</Hint>
          </li>
          <li>
            databases: <Hint text="I know SQL, but mostly use ORM">PostgreSQL, SQLite</Hint>
          </li>
          <li>
            markup: <Hint text="Any pre- and post- processor, YAML and markdown. Pixel perfect markup">HTML, CSS, SCSS,
              SASS, Less</Hint>
          </li>
          <li>
            testing: <Hint text="Unit tests, End-to-End tests">Jest, Selenium</Hint>
          </li>
          <li>
            bundlers: <Hint text="npm packaging and deployind to npmjs">Webpack, Gulp, Vite, Rollup</Hint>
          </li>
          <li>
            runtime_builders: <Hint text="Create projects from scratch with useful package.json">Bun, Node.js</Hint>
          </li>
          <li>
            team_work: <Hint
              text="I'll integrate Agile best practices seamlessly into your team's workflow, ensuring efficiency and adaptability.">
              Git, Jira, Confluence</Hint>
          </li>
          <li>
            IDE: <Hint text="I use open-source and free IDE">VSCode</Hint>
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
      <p>
        Pet projects:
      </p>
      <div>
        <Accordion title="Smart Go Board" comment="open-source hardware startup">
          <ul>
            <li>&nbsp;<a href="https://www.instagram.com/smart.go.board/">Instagram</a></li>
            <li> I created the schematics, PCB and code by myself.</li>
          </ul>
        </Accordion>
        <Accordion title="TotalBattle" comment="open-source selenium game automation">
          <ul>
            <li>&nbsp;<a target="_blank" href="https://github.com/orgs/TBCounter/repositories">Source</a>
            </li>
            <li>&nbsp;<a target="_blank" href="https://totalbattle.omegasoft.keenetic.name/">Application</a></li>
            <li>
              Created whole project from scratch
            </li>
            <li>
              Several active users every day for about 1 year
            </li>
            <li>
              Backend, frontend, Chrome extension
            </li>
            <li>
              Technologies: FastAPI, Vue, PostgreSQL, docker, pinia
            </li>
          </ul>
        </Accordion>
        <Accordion title="Cashflow" comment="Telegram mini-app for financial management">
          <ul>
            <li>&nbsp;<a href="https://github.com/Late-Dev/Cashflow">Source</a></li>
            <li>&nbsp;<a href="https://t.me/keepcashflowbot">Try bot</a></li>
            <li>
              Created bot and mini-app from scratch
            </li>
            <li>
              Participate in telegram hackathon
            </li>
            <li>
              Project management and communication with team.
            </li>
          </ul>
        </Accordion>
        <Accordion title="Subsby" comment="Telegram bot for video subtitles">
          <ul>
            <li>&nbsp;<a href="https://t.me/subsby_bot">Try bot</a></li>
            <li> AI-based subtitles generation</li>
            <li> Created telegram bot from scratch</li>
          </ul>
        </Accordion>
      </div>
      <p>
        Support me:
      </p>
      <a target="_blank" href="https://www.patreon.com/Omega394">Patreon</a> and
      <a target="_blank" href="https://boosty.to/omega_soft">Boosty</a>

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
import Hint from './components/Hint.vue';


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
