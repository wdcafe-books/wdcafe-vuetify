# CH1. Vuetify 설치

  

  

## 1\. Vuetify 설치하기 - 첫번째 방법 (권장)

Vue.js 3에 대한 **\[Default\]**  프로젝트를 생성한 상태라고 가정하겠습니다. 이어서, 아래 명령어를 통해 Vuetify를 설치합니다:

  

### 템플릿 다운로드

  
1)  Vuetify Router 포함 템플릿  :     [다운로드](http://naver.me/FQR7DYgJ "http://naver.me/FQR7DYgJ")

2)   Vuetify Vuex 포함 템플릿     :    [다운로드](http://naver.me/G0ld4ssy "http://naver.me/G0ld4ssy")   
  

  

  

- Vue 설치 

```
vue create 프로젝트명
```

  

  

→  옵션 중 아래 옵션 선택  :

```
Manually select features     
```

  

```
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, CSS Pre-processors, Linter
? Choose a version of Vue.js that you want to start the project with 3.x
? Use history mode for router? (Requires proper server setup for index fallback in production) Yes
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by default): Sass/SCSS (with dart-sass)
? Pick a linter / formatter config: Basic
? Pick additional lint features: Lint on save
? Where do you prefer placing config for Babel, ESLint, etc.? In package.json
? Save this as a preset for future projects? (y/N) n
```

  

  

- NPM 패키지 설치하기

```
vue add vuetify
```

  

→  옵션 중 아래 옵션 선택

```
Vuetify 3 - Vue CLI (preview)
```

  

  

- src/plugins/vuetify.js   수정

```
// Styles
import '@fortawesome/fontawesome-free/css/all.css'
import '@mdi/font/css/materialdesignicons.css'
import { fa } from 'vuetify/iconsets/fa'
import { mdi } from 'vuetify/iconsets/mdi'
import 'vuetify/styles'

// Vuetify
import { createVuetify } from 'vuetify'
import * as components from 'vuetify/components'
import * as directives from 'vuetify/directives'

export default createVuetify(
  {
    icons: {
      defaultSet: 'mdi',
      sets: {
        fa,
        mdi
      },
    },
    components,
    directives,
  }
)
```

  

  

- router/index.js  수정

```
import { createRouter, createWebHistory } from 'vue-router'
import HomeView from '../views/HomeView.vue'
import AboutView from '../views/AboutView.vue'
import GridView from '../views/GridView.vue'
import SpacingView from '../views/SpacingView.vue'
import DisplayView from '../views/DisplayView.vue'
import FontView from '../views/FontView.vue'
import IconButton from '../views/IconButton.vue'
import CardView from '../views/CardView.vue'
import ExpansionPanels from '../views/ExpansionPanels.vue'
import DialogModal from '../views/DialogModal.vue'
import ListsView from '../views/ListsView.vue'
import VsheetMenu from '../views/VsheetMenu.vue'
import TabsView from '../views/TabsView.vue'
import LoadingView from '../views/LoadingView.vue'
import PaginationView from '../views/PagenationView.vue'
import TableView from '../views/TableView.vue'
import CarouselView from '../views/CarouselView.vue'

const routes = [
  { path: '/', name: 'home', component: HomeView },
  { path: '/about', name: 'about', component: AboutView },
  { path: '/grid',  name: 'grid',  component: GridView  },
  { path: '/spacing', name: 'spacing', component: SpacingView },
  { path: '/display', name: 'display', component: DisplayView },
  { path: '/font', name: 'font', component: FontView },
  { path: '/iconbtn', name: 'iconbtn', component: IconButton },
  { path: '/cards', name: 'cards', component: CardView },
  { path: '/panels', name: 'panels', component: ExpansionPanels },
  { path: '/dialog', name: 'dialog', component: DialogModal },
  { path: '/lists', name: 'lists', component: ListsView },
  { path: '/vsheet', name: 'vsheet', component: VsheetMenu },
  { path: '/tabs', name: 'tabs', component: TabsView },
  { path: '/loading', name: 'loading', component: LoadingView },
  { path: '/pagination', name: 'pagination', component: PaginationView },
  { path: '/table', name: 'pagination', component: TableView },
  { path: '/carousel', name: 'carousel', component: CarouselView },
]

const router = createRouter({
  history: createWebHistory(process.env.BASE_URL),
  routes
})

export default router
```

  

  

- App.vue  수정

```
<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

nav {
  padding: 30px;
  text-align: center;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #42b983;
}

/* .v-toolbar-title__placeholder{
  width: fit-content;
} */
.v-layout{
  height: 200px;
}
.v-container{
  margin-bottom: 200px;
}
.menu-items .v-list-item:hover{
  background-color: #fc0;
}
</style>
```

  

  

- HomeView.vue  수정

```
<template>
  <h1>Home Page</h1>
</template>

<script>
// Components
// import HelloWorld from '../components/HelloWorld.vue';

export default ({
  name: 'HomeView',
});
</script>

<style scoped lang="scss">
  .v-container{
    margin-bottom: 50px;
    >.v-row{
      margin-bottom: 20px;
    }

    .v-col{
      border: 1px solid #000;
    }

    .box{
      border: 1px solid #000;
    }
  }
</style>
```

  

  

  

  

  

## 2\. Vuetify 설치하기 - 두번째 방법

Vue.js 3에 대한  **\[Router\]** 포함한 프로젝트를 생성한 상태라고 가정하겠습니다. 이어서, 아래 명령어를 통해 Vuetify를 설치합니다:

  

- NPM 패키지 설치하기

```
npm install vuetify@next
npm i -D vuetify vite-plugin-vuetify
npm i @mdi/font
```

  

  

위의 명령어 실행 후 다음과 같은 경로에 파일을 추가해줍니다:

  

1. `src/plugins/vuetify.js` 파일을 생성합니다:

```
import '@mdi/font/css/materialdesignicons.css'
import 'vuetify/styles'
import { createVuetify } from 'vuetify'
import * as components from 'vuetify/components'
import * as directives from 'vuetify/directives'

export default createVuetify({
  components,
  directives,
})
```

##   

1. `src/main.js` 파일을 다음과 같이 수정합니다:

```
import { createApp } from 'vue'
import App from './App.vue'
import router from './router'
import vuetify from './plugins/vuetify'

createApp(App).use(router).use(vuetify).mount('#app')
```

  

  
이제 모든 준비가 완료되었습니다.`views/Homeview.vue`  파일에 간단한 Vuetify 3 버튼을 추가해 보겠습니다:  

  

```
<template>
  <h1>Home page</h1>

  <p><v-btn color="primary">Click Me</v-btn></p>
</template>

<script>
export default {
  name: 'HomeView',
  components: {
    
  }
}
</script>

<style>
  p{
    margin: 20px 0;
  }
</style>
```