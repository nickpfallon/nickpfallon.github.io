<template id="">
  <div>
    <v-app>
      <div class="main">
        <v-container>
          <header>
            <h1>{{ title }}</h1>
          </header>
          <v-layout>
            <v-flex xs12 md8 offset-md2>
              <div v-for="project in projects" :key="project.title">
                <v-card class="my-4">
                  <v-card-media
                    class="white--text"
                    height="400px"
                    :src="project.src"
                  >
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">{{ project.title }}</h3>
                      <div class="description">{{ project.description }}</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <a :href="project.siteUrl" target="
                    _blank"><v-btn icon class="black--text">
                      <v-icon medium>fa-external-link</v-icon>
                    </v-btn></a>
                    <a :href="project.github"><v-btn icon class="black--text">
                      <v-icon medium>fa-github</v-icon>
                    </v-btn></a>
                  </v-card-actions>
                </v-card>
              </div>
            </v-flex>
          </v-layout>
        </v-container>
      </div>
    </v-app>
  </div>
</template>

<script type="text/javascript">
  export default {
    data() {
      return {
        title: 'projects',
        projects: [
          {
            title: 'Plague Nation',
            description: 'A web application that tracks mentions of flu symptoms on Twitter and maps the locations of those Tweets.',
            src: require('../assets/plague-nation.png'),
            siteUrl: 'https://plague-nation-1499461518065.firebaseapp.com/#/',
            github: 'https://github.com/nickpfallon/plague-nation'
          },
          {
            title: 'Pixelaid',
            description: 'A website that provides a creative way for internal collaboration within teams. Team members can answer questions posted by their colleagues and receive points to place colored pixels on a shared pixel canvas.',
            src: require('../assets/pixelaid.png'),
            siteUrl: 'http://pixelaid.herokuapp.com/',
            github: 'https://github.com/Pixelaid-Team/Pixelaid'
          },
          {
            title: 'GrooveBass',
            description: 'A native iOS app that allows users to enter a zip code and see all the shows playing in that week within a chosen radius. Users are able to select a show and are then presented with a playlist of the artist playing that show.',
            src: require('../assets/groovebass.png'),
            siteUrl: 'https://www.youtube.com/watch?v=pY8IAGtAmU8',
            github: 'https://github.com/Groove-Bass/Groove-Bass-the-Repo'
          },
          {
            title: 'M\u00fcncher',
            description: 'An Tinder-like web application for food recipes that allows users to search an ingredient and click through recipes related to that ingredient.',
            src: require('../assets/muncher.png'),
            siteUrl: 'https://q1-project-943b7.firebaseapp.com/',
            github: 'https://github.com/nickpfallon/project-q1'
          }
        ]
      }
    }
  }
</script>

<style media="screen" scoped>
  .main {
    background-color: #fafafa;
    height: 100%;
  }
  h1 {
    color: #006064;
    font-size: 4em;
    margin-top: 1em;
    margin-bottom: .5em;
  }
  h3 {
    font-weight: bold;
  }
  header {
    display: flex;
    justify-content: center;
  }
  a {
    text-decoration: none;
  }
  .description {
    font-size: 1.25em;
  }
</style>
